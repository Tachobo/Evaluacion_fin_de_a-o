Documento de Evaluación

 Al finalizar la digitación de los datos de la solicitud, escriba s, cuando le pregunte si desea ingresar otra, haga esto 4 veces, para hacer un total de 5 pruebas.

Prueba 1:

ID: 1
Nombre: Nem
Edad: 25
Rol: visitante
Permisos: lectura
¿Acepta condiciones?: s

Se espera que la solicitud sea APROBADA después de la consulta de antecedentes, indicando que los datos son consistentes.


Prueba 2:

ID: 1

Se espera que dé el siguiente mensaje de error: "ID inválido o repetido." y que pida el ingreso de un nuevo ID para la solicitud.


Prueba 3:

ID: 2
Nombre: Alex
Edad: 20
Rol: editor
Permisos: lectura, escritura, borrado

Se espera que el sistema dé el siguiente mensaje de error: "Resultado: RECHAZADA. Motivo: El rol 'editor' no tiene autorización para los permisos solicitados." ya que el editor no puede borrar.


Prueba 4:

ID: 3
Nombre: Admin123
Edad: 30
Rol: admin
Permisos: lectura, escritura, borrado
¿Acepta condiciones?: s

Al procesarse la auditoría, se espera que la consola diga lo siguiente: Resultado: RECHAZADA. Motivo: RECHAZADO: El solicitante se encuentra en la lista de restricción.


Prueba 5:

ID: 4
Nombre: Mel
Edad: 15
Rol: visitante
Permisos: lectura
¿Acepta condiciones?: s

Se espera que el sistema analice las reglas básicas y para la solicitud #4 diga lo siguiente: Resultado: RECHAZADA. Motivo: Reglas básicas no cumplidas: Menor de edad. Al finalizar, se debe mostrar el mensaje "Auditoría finalizada".