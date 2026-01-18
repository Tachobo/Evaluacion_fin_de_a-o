Documentación Técnica

Datos de Entrada

Identificador: Número entero único. Se valida que no esté repetido para no cruzar información.

Tipo de operación: Texto (solo letras). No puede estar vacío.

Valor asociado: Número decimal o entero. Tiene un tope máximo de 10,000.

Prioridad: Número del 1 al 5. Se genera de forma aleatoria.

Estado (booleano): true (activo).


Procesos

Captura de información y validación: Se usa un bucle while y varios bloques try/catch, para cada dato ingresado, con el fin de que, no existan identificadores duplicados (para esto se uso .some), los datos ingresados sean correctos según las reglas anteriormente mencionadas y que no se permitan datos vacíos.

Aplicación de tasa mediante el uso de callback: Se implementó una función llamada aplicarTasaConCallback para procesar el valor recibido, dicha función realiza un cálculo del 10% de tasa fija, y ejecuta otra función que informa el resultado final del valor ajustado.

Verificación por medio de promesa: Se usó la promesa llamada verificarServidorConPromesa, esto simula la verificación externa con un retardo de 1.5 segundos, en este caso se usó como regla el ID de la operación, para ser resuelta la promesa con éxito en base a esta regla, el ID debe ser un número par, si no se cumple con esto (ID impar), la promesa se rechaza, caso contrario, se resuelve con éxito.

Control de flujo y procesamiento en secuencia: El sistema recorre el conjunto de solicitudes con un bloque for of, se usó await para que cada solicitud se procese de manera ordenada.

Manejo de errores

Validación: Se lanzan errores con throw new error, si los datos no cumplen los requisitos estipulados (como superar el valor máximo).

Protección del ciclo: Cada iteración del proceso está envuelto en un bloque try catch, con el fin de que, si una solicitud falla, ya sea por validación o porque la promesa fue rechazada (ID impar), el error sea capturado y mostrado en consola, así el sistema puede continuar con la siguiente solicitud sin detenerse.


Datos de salida

Confirmación de registro de cada ID.

Visualización del valor ajustado con la tasa (vía callback).

Resultado de Aprobación: Mensaje de éxito si la promesa se resuelve (fondos verificados).

Resultado de Fallo: Mensaje detallado si es rechazada por el servidor o marcada como inválida.

Resumen Final: Conteo total de procesadas, aprobadas, rechazadas e inválidas.


Justificación técnica
Uso de async/await: Permite manejar la simulación de red o procesos pesados de forma legible, evitando el uso del triángulo infernal de las callback.

Desestructuración de Objetos: Se utiliza para acceder a las propiedades de la solicitud de forma limpia y eficiente en las validaciones.

Modularización: La separación de lógica (validación, captura, procesamiento) facilita la escalabilidad del código.

Robustez: El uso intensivo de try/catch garantiza que el sistema sea tolerante a fallos y que un dato corrupto no rompa toda la ejecución.