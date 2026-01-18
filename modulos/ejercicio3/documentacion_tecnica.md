Documentación Técnica

Datos de Entrada

Identificador (ID): Número entero único. Se valida que no esté repetido para garantizar la integridad de la auditoría.

Nombre del solicitante: Texto. Debe tener al menos 3 caracteres de largo.

Edad: Número entero. Se utiliza para verificar la mayoría de edad.

Rol solicitado: Texto (admin, editor, visitante). Determina los permisos permitidos.

Arreglo de permisos: Lista de textos. Se valida que sean coherentes con el rol asignado.

Aceptación de condiciones (booleano): true (s) o false (n).


Procesos

Captura de información y validación: Se usa un bucle while y validaciones manuales para el ID, con el fin de que no existan identificadores duplicados (para esto se usó .some) y que los datos básicos como la edad y el nombre sean correctos antes de entrar al proceso de auditoría.

Validación de reglas básicas mediante el uso de callback: Se implementó una función llamada validarReglasBasicas para procesar la edad y la aceptación de términos, dicha función verifica que el usuario sea mayor de edad y haya aceptado condiciones, ejecutando un callback que informa si el resultado es "OK" o el motivo del fallo.

Verificación externa por medio de promesa: Se usó la promesa llamada validarAntecedentesExternos, esto simula la verificación en una base de datos externa con un retardo de 1.2 segundos, en este caso se usó como regla la longitud del nombre y una lista negra; si el nombre es muy largo (>15) la promesa falla por error de sistema, y si está en la lista negra, se resuelve como RECHAZADO.

Control de flujo y procesamiento en secuencia: El sistema recorre el conjunto de solicitudes con un bloque for of, se usó await para que la consulta de antecedentes de cada solicitante se procese de manera ordenada y secuencial.


Manejo de errores

Validación: Se lanzan errores con throw new error si los datos no cumplen los requisitos de integridad (edad no numérica, nombre corto) o de coherencia (permisos que no corresponden al rol).

Protección del ciclo: Cada iteración del proceso está envuelto en un bloque try catch, con el fin de que, si una solicitud falla por validación o por un error en la conexión de la promesa, el error sea capturado, se muestre el motivo del rechazo en consola y el sistema pueda continuar con la siguiente auditoría sin detenerse.


Datos de salida

Confirmación de inicio de auditoría para cada ID y nombre.

Mensaje de consulta de antecedentes en tiempo real.

Resultado de Aprobación: Mensaje de éxito si la promesa y las validaciones se cumplen (Datos consistentes).

Resultado de Fallo: Mensaje de "RECHAZADA" detallando el motivo (menor de edad, permisos inválidos o lista negra).

Mensaje de cierre: "Auditoría finalizada".


Justificación técnica
Uso de async/await: Permite manejar la simulación de red de la base de datos de antecedentes de forma legible, evitando el uso del triángulo infernal de las callback.

Inmutabilidad (Constantes): Se utiliza un objeto REGLAS_ROL_PERMISOS para mantener fijas las reglas de negocio y evitar alteraciones durante la ejecución.

Modularización: La separación de lógica entre captura, reglas básicas y validación externa facilita la escalabilidad del sistema de accesos.

Robustez: El uso intensivo de try/catch garantiza que el sistema sea tolerante a fallos de conexión o datos corruptos sin romper el flujo principal.