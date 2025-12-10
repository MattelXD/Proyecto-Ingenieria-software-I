Caso de Uso UC1: Ingresar solicitud de retiro:
- Actor Principal: Cliente
Actores involucrados e intereses:
- Usuario: El cliente desea ingresar una solicitud de retiro para que los recolectores recojan su material de reciclaje.
- API geolocalizador: El API geolocalizador valida que la ubicación ingresada en la solicitud de retiro esté dentro de alguna zona de recolección válida.
Precondiciones: Cliente debe estar registrado en el sistema
Postcondiciones (garantías de éxito): La solicitud de retiro queda registrada en el sistema
Escenario principal de éxito (Flujo básico):
 1. Cliente accede al sistema 
 2. Cliente elige la opción de ingresar solicitud de retiro
 3. El sistema pide la ubicación del retiro
 4. El cliente ingresa su ubicación en la solicitud
 5. El sistema hace un llamado a UC2: Validar ubicación ingresada
 6. Si los datos son correctos el sistema registra la solicitud
 7. El sistema muestra que la solicitud se registró exitosamente
Extensiones (Flujos Alternativos):
 2'. El cliente ya posee una solicitud activa:
 Entonces el sistema muestra un mensaje indicando que no puede hacer otra solicitud.
 El flujo termina y no deja continuar con el registro.
 4'. El cliente no ha ingresado su ubicación:
 Entonces el sistema pide que se ingrese la ubicación.
 5'. Si la ubicación no es válida:
 Entonces el sistema rechaza la solicitud e informa al cliente de que la ubicación es inválida y pide que se vuelva a ingresar .

Caso de Uso UC2: Validar ubicacion ingresada
- Actor Principal: API geolocalizador
Actores involucrados e intereses:
- Usuario: El cliente ingreso su ubicación en la solicitud
- API geolocalizador: Debe validar que la ubicación ingresada en la solicitud esté dentro de alguna de las zonas de recolección válida
Precondiciones: Cliente ingresó coordenadas a la solicitud
Postcondiciones (garantías de éxito): El sistema devuelve la respuesta de validez de la ubicación (válido o no válido).
Si es válido el sistema permite continuar con el registro de la solicitud.

Escenario principal de éxito (Flujo básico):
 1. El sistema recibe la ubicación ingresada en el UC1
 2. El sistema envía la ubicación a la API
 3. El API verifica que la ubicación ingresada esté dentro de alguna zona de recolección válida 
 4. El API responde con validación de ubicación al sistema
 5. El sistema retorna el control a UC1
Extensiones (Flujos Alternativos):
 3' Si la ubicación ingresada está fuera de alguna zona de recolección válida:
 Entonces el API responde con invalidación de la ubicación al sistema



