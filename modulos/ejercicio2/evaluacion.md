Documento de Evaluación

Al finalizar la digitación de los datos de la operación, escriba s, cuando le pregunte si desea registrar otra, haga esto 4 veces, para hacer un total de 5 pruebas.


Prueba 1:

ID: 20
Tipo: Venta
Valor: 500

Se espera que la operación sea aprobada, que el callback muestre el valor ajustado de 550 y que el servidor confirme la conexión exitosa tras 1.5 segundos.


Prueba 2:

ID: 20

Se espera que dé el siguiente mensaje de error: "ID ya registrado." y que pida el ingreso del ID de operación nuevamente.


Prueba 3:

ID: 44
Tipo: Pago123

Se espera que el sistema dé el siguiente mensaje de error: "Error: Solo se permiten letras." y que pida el tipo de operación nuevamente.


Prueba 4:

ID: 101
Tipo: Compra
Valor: 1000

Al terminarse el programa al digitar todos los datos de la última solicitud, se espera que la consola diga lo siguiente: RECHAZADA: Servidor: Fondos insuficientes o error de conexión. (Esto sucede porque el ID es impar).


Prueba 5:

ID: 50
Tipo: Inversion
Valor: 15000

Se espera que el sistema analice la consistencia y para la operación #50 diga lo siguiente: INVÁLIDA: Valor fuera de rango: máximo permitido 10000. Al finalizar, el resumen debe mostrar: Total Procesadas: 4 (si se saltó la inválida o se contó según el flujo), Aprobadas: 2, Rechazadas: 1, Inválidas: 1.