# prestamos
# 0801200601010 Jesus Fernando Moreno Martinez 

# ¿Qué pasa con un equipo cuando se desmarca el campo Activo? ¿Por qué es mejor que borrarlo?
# r/ si no se marca el campo activo no aparecera el objeto que coloquemos, asi es mas sencillo debido a que no afectara el stock 
# ¿Para qué sirve copy=False en el campo codigo?
# r/ hacemos que el campo no se copie o duplique logrando un error de ingreso como este articulo existe ejemplos asi 

# Este modelo usa _name y _inherit al mismo tiempo. ¿Qué hace cada uno aquí?
# r/ primero define un nuevo modelo y una nueva tabla en la base de datos y tambien usando una herencia con el inherit de algun otro modelo existente asi seria una reutilizacion de codigo con diferentes datos y caracteristicas

# ¿Qué hace tracking=True en el campo state? Lo verá funcionar en el paso 4




# En fields.One2many("prestamo.linea", "prestamo_id"), ¿qué indica cada parámetro?
# r/ El primer parametro muestra prestamos de linea en modelo mostrara lso resgistro del modelo y el segundo parametro muestra que es many2one el cual bsuca en prestamo.linea que si en todos los resgistros encuentre el id que es exatamente ese

# ¿Qué pasa con las líneas cuando se borra un préstamo? ¿Qué parte del código lo define?
# r/ primero borrara todo relacionado a eso como sus detales en prestamo.linea evitan que los registros queden sin algun id o datos cuyo caso en vez de solo flotar seran borrados automaticamente sin prestamo no hay detalle

# Los botones ya se ocultan según el estado. ¿Por qué los métodos vuelven a validar el estado?
# r/ Es como volver a validar el estado dentro de un metodo podemos garantizar funcion logrando que un usuario lo tome un exito silencioso que un mensaje diciendo listo y enviado 

# ¿Qué hace prestamo.linea_ids.equipo_id.write(...) y por qué no necesita un for?
# r/ el cambio se puede aplicar automaticamente si y a los equipos seleccionados, con eso se vita un error de recorrer registro por registro de por si tedioso y tardio, logranod asi un ahorro de tiempo y no ver la pantalla llena de registro por registro

# El campo equipo_id ya filtra los equipos disponibles. ¿Por qué hace falta el TODO 5?
# r/ el momento en que se selecciona el equipo y el momento en que se pulsa prestar, otro usuario podría haber prestado ese mismo equipo y cambiar su estado y todo eso va en el  5 logrando asi volver a verificar el estador del servidor antes de confirmar el prestamo 

# ¿En qué momento se ejecuta un método con @api.constrains? ¿Y la validación de action_prestar?
# r/ vañidar por si  falla sino lanzando una excepción y el registro no se guarda en la base de datos en cambio las validaciones de action_prestar solo se ejecutan cuando el usuario pulsa el botón de prestar ya que forman parte de una acción específica sin cambio
