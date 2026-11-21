# Guia Practica Odoo 3er Parcial  
**Nombre**: Angel Fernando Cordova Montoya  
**Cuenta**: 0824200600869  

## Preguntas  
1. ¿Qué pasa con un equipo cuando se desmarca el campo Activo? ¿Por qué es mejor que 
borrarlo? 
2. ¿Para qué sirve copy=False en el campo codigo?
3. Este modelo usa _name y _inherit al mismo tiempo. ¿Qué hace cada uno aquí? 
4. ¿Qué hace tracking=True en el campo state? Lo verá funcionar en el paso 4. 

## Respuestas  
1. Se oculta el registro de las vistas normales y las búsquedas por defecto, pero este sigue existiendo en la base de datos. Es mejor archivarlo que borrarlo por dos razones: Se mantiene el historial, si se borra un equipo que ya tuvo movimientos, los datos se pueden perder si se borra el equipo o pueden surgir errores por integridad de datos. La otra razón viene siendo que archivarlo es reversible, ya que se puede volver a activar el registro sin tener que crearlo desde 0.  
2. Sirve para evitar que el valor del codigo se copie cuando un usuario usa la función "Duplicar" en un registro. Ayuda a prevenir codigos duplicados y se obliga a que el nuevo registro genere o reciba su propio nuevo codigo.  
3. En este caso, _name = "prestamo.prestamo" crea un modelo nuevo y su propia tabla en la base de datos. El _inherit = ["mail.thread"] hereda las funciones y los campos de mail.thread para agregar el chatter al modelo nuevo.  
4. tracking=True registra de manera automatica en el chatter cada vez que el campo state cambia de valor, mostrando las acciones que hizo el usuario, la hora y la fecha, el estado anterior y el nuevo estado.