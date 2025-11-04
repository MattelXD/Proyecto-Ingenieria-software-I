Nombre: LlenarFormularioSolicitudRetiro(info)
Responsabilidades: Esta operacion llena el formulario de solicitud de retiro con los datos requeridos e ingresarlo.
Referencia: Ingresar solicitud de retiro
Notas: Los datos deben corresponder al tipo de variable que pide el formulario 
Excepciones: Datos no corresponden a tipo de variable, pide que lo corrija
Salida: Formulario lleno
Precondiciones: Sistema reconoce a usuario
Postcondiciones:
-Sistema crea nueva instancia de Solicitud
-Solicitud se compone de Usuario
-Se asigna datos a la Solicitud.info
-Se asgina ID_solicitud correspondiente a Solicitud
-Se asigna fecha a Solicitud
-La solicitud se asocia con API geolocalizador




Nombre: Agregar_nota(desc)
Responsabilidades: Esta operacion se encarga de agregar una nota con una descipcion a la solicitud
Referencia: Ingresar solicitud de retiro
Notas:
Excepciones:
Salida: Nota creada
Precondiciones: El formulario debe haber sido completado
Postcondiciones
-Sistema crea una nueva instancia de Nota
-Sistema se compone de nota a solicitud
-Se asigna desc a Agregar_nota.descripcion

Nombre: AccederFormulario
Responsabilidades: Esta operacion se encarga de que el usuario acceda al formulario
Referencia: Ingresar solicitud de retiro
Notas:
Excepciones:Si hay un error de interntet no se accede y pide que lo haga de nuevo
Salida: 
Precondiciones: El sistema detecta de que eres un usuario valido
Postcondiciones:
-Se crea una nueva instancia de usuario





