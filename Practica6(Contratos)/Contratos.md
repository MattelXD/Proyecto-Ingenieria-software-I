Nombre: LlenarFormularioSolicitudRetiro(info)
Responsabilidades: Esta operacion llena el formulario de solicitud de retiro con los datos requeridos
Referencia: Ingresar solicitud de retiro
Notas: Los datos deben corresponder al tipo de variable que pide el formulario 
Excepciones: Datos no corresponden a tipo de variable, pide que lo corrija
Salida: Formulario lleno
Precondiciones: Sistema reconoce a usuario
Postcondiciones:
-Sistema crea nueva instancia de Solicitud
-Solicitud se compone de Usuario
-z
-Se asigna datos a la Solicitud.info




Nombre: Agregar_nota(desc)
Responsabilidades: 
Referencia: Ingresar solicitud de retiro
Notas:
Excepciones:
Salida: Nota creada
Precondiciones: El formulario debe haber sido completado
Postcondiciones
-Sistema crea una nueva Nota
-Sistema se compone de nota a solicitud
-Se asigna desc a Agregar_nota.descripcion



Nombre: IngresarSolicitudRetiro(solicitud)
Responsabilidades: Esta operacion se encarga de ingresar la solicitud de retiro para que esta sea validada
Referencia: Ingresar solicitud de retiro
Notas:
Excepciones:si hay algun error de conexion, no se ingresa la solicitud y se pide que se haga de nuevo
Salida:--
Precondiciones: El formulario debe haber sido completado
Postcondiciones:
-Se asgina ID_solicitud a Solicitud
-La solicitud se asocia con API geolocalizador


