# Guia Practica Odoo 3er Parcial  
**Nombre**: Angel Fernando Cordova Montoya  
**Cuenta**: 0824200600869  

## Preguntas  
1. ¿Qué pasa con un equipo cuando se desmarca el campo Activo? ¿Por qué es mejor que 
borrarlo? 
2. ¿Para qué sirve copy=False en el campo codigo?

## Respuestas  
1. Se oculta el registro de las vistas normales y las búsquedas por defecto, pero este sigue existiendo en la base de datos. Es mejor archivarlo que borrarlo por dos razones: Se mantiene el historial, si se borra un equipo que ya tuvo movimientos, los datos se pueden perder si se borra el equipo o pueden surgir errores por integridad de datos. La otra razón viene siendo que archivarlo es reversible, ya que se puede volver a activar el registro sin tener que crearlo desde 0.  
2. Sirve para evitar que el valor del codigo se copie cuando un usuario usa la función "Duplicar" en un registro. Ayuda a prevenir codigos duplicados y se obliga a que el nuevo registro genere o reciba su propio nuevo codigo.