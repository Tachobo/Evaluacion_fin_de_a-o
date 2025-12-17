Ejercicios
1. Sistema de Validación y Procesamiento de Solicitudes
Una entidad académica desea automatizar el proceso de validación y procesamiento de
solicitudes internas realizadas por sus aprendices.
Cada solicitud contiene información diversa y no siempre confiable, por lo que el sistema
debe analizar, validar, clasificar y responder de manera controlada.
El programa deberá recibir un conjunto de solicitudes, evaluarlas una a una y determinar si
cumplen o no con las condiciones mínimas para ser procesadas.
Dependiendo del análisis lógico de cada solicitud, el sistema podrá:
• Aprobarla y procesarla correctamente.
• Rechazarla indicando el motivo.
• Detener su procesamiento si los datos son inconsistentes, sin bloquear el programa.
El flujo completo debe simular operaciones asincrónicas, ya que en un escenario real estas
validaciones podrían depender de servicios externos.
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
Datos de entrada
El sistema deberá trabajar con:
• Un arreglo de objetos, donde cada objeto representa una solicitud.
• Cada solicitud debe contener, como mínimo:
o Identificador numérico único.
o Nombre del solicitante (string).
o Tipo de solicitud (string).
o Prioridad (número entero).
o Estado inicial (boolean).
o Lista de requisitos cumplidos (arreglo de booleanos).
Los datos pueden estar incompletos, mal tipados o fuera de rango, por lo que deben
validarse explícitamente.
Tipos de datos esperados:
• number, string, boolean, array, object.
Proceso o procesos
El aprendiz deberá diseñar un flujo que contemple, como mínimo, los siguientes procesos:
1. Validación inicial de datos
o Verificar tipos de datos.
o Confirmar que los valores cumplen reglas lógicas (por ejemplo, prioridades
válidas).
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
o Cualquier error debe lanzar una excepción controlada.
2. Análisis lógico de la solicitud
o Uso de operadores lógicos y condicionales para decidir si la solicitud puede
continuar.
o Evaluación del arreglo de requisitos mediante ciclos.
3. Procesamiento asincrónico
o Al menos:
▪ Una función basada en callback.
▪ Una función que retorne una promesa.
▪ Una función principal usando async / await.
o Simular retrasos o dependencias lógicas sin bloquear la ejecución.
4. Control de flujo
o Uso adecuado de ciclos (for, while, o métodos de arreglo).
o Decisiones claras según el estado de cada solicitud.
5. Gestión de errores
o Implementar try / catch.
o Mostrar mensajes personalizados y comprensibles para el usuario.
o El programa no debe detenerse ante errores individuales.
6. Buenas prácticas
o Justificar cuándo una estructura es mutable o inmutable.
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
o Explicar el uso de parámetros, retornos y tipos de funciones.
Datos de salida
El programa deberá mostrar en la terminal:
• El resultado del análisis de cada solicitud.
• Mensajes claros indicando:
o Solicitud aprobada y procesada.
o Solicitud rechazada y motivo del rechazo.
o Error controlado por datos inválidos.
Los mensajes deben permitir que cualquier usuario entienda qué ocurrió y por qué.



2. Sistema de Procesos y Validación de Operaciones
Una organización requiere un programa ejecutado desde la terminal que permita procesar
un conjunto de solicitudes operativas registradas durante una jornada laboral.
Cada solicitud representa una acción que debe ser evaluada antes de ser aprobada o
rechazada, considerando múltiples condiciones relacionadas con su contenido, su estado y
las reglas definidas por el sistema.
El programa debe analizar cada solicitud de manera secuencial, garantizando que:
• Las reglas de validación se respeten en todo momento.
• El flujo de ejecución no se vea interrumpido ante errores de entrada o de proceso.
• Cada decisión tomada por el sistema pueda ser explicada y justificada técnicamente.
Al finalizar la ejecución, el sistema debe presentar un resumen claro de los resultados
obtenidos y del comportamiento del programa ante escenarios válidos e inválidos.
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
Datos de entrada
El programa deberá recibir o definir un arreglo de objetos, donde cada objeto represente
una solicitud con la siguiente información mínima:
• Identificador único (numérico).
• Tipo de operación (cadena de texto).
• Valor asociado a la operación (numérico).
• Estado inicial de la solicitud (booleano o cadena controlada).
• Nivel de prioridad (numérico).
Condiciones importantes sobre los datos de entrada:
• Los tipos de datos deben ser validados antes de ser procesados.
• No todos los objetos garantizan información correcta o completa.
• El sistema debe contemplar datos inconsistentes, nulos o fuera de rango.
Proceso o procesos
El aprendiz deberá diseñar la lógica del programa teniendo en cuenta, como mínimo, los
siguientes aspectos:
• Recorrer el arreglo de solicitudes utilizando ciclos adecuados.
• Aplicar operadores lógicos y condicionales para decidir:
o Si una solicitud puede ser procesada.
o Si debe ser aprobada, rechazada o marcada como inválida.
• Implementar funciones que:
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
o Sean reutilizables.
o Usen parámetros correctamente definidos.
o Retornen valores con tipos claros y coherentes.
• Justificar el uso de mutabilidad o inmutabilidad al manipular los datos.
• Implementar al menos:
o Un callback para procesar una acción dependiente.
o Una promesa para simular un proceso asincrónico.
o Una función con async/await para manejar el flujo asincrónico de forma
legible.
• Manejar errores de forma controlada, utilizando try / catch, asegurando:
o Que el programa no se bloquee.
o Que los mensajes de error sean claros y orientados al usuario.
Datos de salida
El programa debe mostrar en terminal, de forma organizada:
• El resultado individual de cada solicitud procesada.
• Mensajes claros cuando una solicitud no cumpla las condiciones esperadas.
• Indicadores explícitos cuando un error haya sido capturado correctamente.
• Un resumen final que incluya:
o Total de solicitudes procesadas.
o Cantidad de solicitudes aprobadas.
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
o Cantidad de solicitudes rechazadas.
o Cantidad de solicitudes inválidas.
Los datos de salida deben permitir evidenciar:
• La correcta ejecución del flujo lógico.
• El manejo adecuado de escenarios de éxito y de falla.
• La coherencia entre los datos de entrada, el proceso aplicado y el resultado
obtenido.



3. Sistema de Gestión y Validación de Solicitudes de Acceso
Una organización gestiona solicitudes de acceso a un sistema interno a través de la
terminal.
Cada solicitud es registrada con información básica del solicitante y con un conjunto de
condiciones que determinan si el acceso puede ser aprobado, rechazado o dejado en
estado de revisión.
El sistema no debe asumir que los datos son correctos.
Antes de tomar cualquier decisión, es necesario verificar la integridad, coherencia y
consistencia de la información, considerando que una misma persona puede realizar
más de una solicitud y que algunas reglas dependen de la relación entre varios datos, no
de un único valor aislado.
Adicionalmente, el sistema debe simular un proceso asincrónico de validación externa (por
ejemplo, verificación de antecedentes o validación de permisos), el cual puede responder
correctamente o fallar, y cuyo resultado influye directamente en la decisión final.
El programa debe ejecutarse completamente desde la terminal, sin bloquear su flujo
ante errores y proporcionando mensajes claros al usuario en cada escenario posible.
Datos de entrada
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
Los datos deben ser ingresados o definidos en el programa y organizados en arreglos y
objetos.
Cada solicitud debe contener, como mínimo:
• Identificador único de la solicitud (número).
• Nombre del solicitante (string).
• Edad del solicitante (number).
• Rol solicitado dentro del sistema (string).
• Lista de permisos solicitados (arreglo de strings).
• Estado actual de la solicitud (string).
• Indicador de si aceptó o no las condiciones del sistema (boolean).
Consideraciones importantes sobre los datos:
• Los tipos de datos deben ser validados.
• Los valores no válidos o incompletos deben generar errores controlados.
• Se deben contemplar escenarios donde:
o La edad no sea un número válido.
o El arreglo de permisos esté vacío.
o El rol no corresponda con los permisos solicitados.
o El usuario no haya aceptado las condiciones.
Proceso o procesos
El aprendiz deberá implementar un flujo lógico que incluya, como mínimo:
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
• Uso de condicionales para:
o Validar datos de entrada.
o Determinar si una solicitud puede continuar en evaluación.
• Uso de ciclos para:
o Recorrer el arreglo de solicitudes.
o Analizar los permisos solicitados.
• Aplicación de operadores lógicos y matemáticos para establecer reglas de
decisión.
• Manejo de inmutabilidad, evitando modificar directamente las estructuras
originales.
• Implementación de:
o Una función con callback para validar reglas básicas.
o Una función que retorne una promesa para simular la validación externa.
o Una función principal usando async / await para coordinar todo el proceso.
• Uso obligatorio de try / catch para:
o Capturar errores de validación.
o Manejar fallos en procesos asincrónicos.
o Evitar bloqueos del programa.
Cada función debe estar justificada:
por qué fue creada, qué recibe, qué retorna y qué tipo de dato maneja.
Datos de salida
Centro Industrial de Mantenimiento Integral
INSTRUMENTO DE EVALUACIÓN
Versión: 04
El programa debe mostrar en la terminal, de forma clara y estructurada:
• El resultado final de cada solicitud:
o Aprobada
o Rechazada
o En revisión
• Los motivos de la decisión tomada.
• Mensajes personalizados en caso de:
o Datos inválidos.
o Fallos en la validación asincrónica.
o Reglas no cumplidas.
Resultados esperados:
• Una solicitud solo puede ser aprobada si todas las condiciones se cumplen
correctamente.
• Una solicitud debe ser rechazada si los datos son incorrectos o las reglas lógicas no
se cumplen.
• El sistema nunca debe detenerse abruptamente, incluso ante errores.