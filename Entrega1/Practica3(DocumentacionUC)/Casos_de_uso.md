Caso de Uso UC1: Ingresar solicitud de retiro
Actor Principal: Usuario
Actores involucrados e intereses:
-Usuario: El usuario desea ingresar una solicitud de retiro para los recolectores recojan su material de reciclaje.
-API geolocalizador: El API geolocalizador valida los datos ingresados en la solicitud de retiro.

Precondiciones: Usuario debe estar registrado en el sistema
Postcondiciones (garantias de exito): La solicitud de retiro queda registrada en el sistema

Escenario principal de exito (Flujo basico):
1. Usuario accede al sistema 
2. Usuario elige la opcion de ingresar solicitud de retiro
3. El sistema pide la direccion o coordenadas del retiro
4. El usuario ingresa sus coordenadas en la solicitud
5. El sistema hace un llamado a UC2: Validar coordenadas ingresadas
6. Si los datos son correctos el sistema registra la solicitud
7. El sistema muestra que la solictud se registro exitosamente
Extensiones (Flujos Alternativos):
2'. El usuario ya posee una solicitud activa en el dia:
- Entonces el sistema muestra un mensaje indicando que no puede hacer otra solicitud por lo que queda de dia
- El flujo termina y no deja continuar con el registro
4'. El usuario no ha ingreasado sus coordenadas:
- Entonces el sistema pide que se ingresen las coordenadas
5'. Si las coordenadas no son validas:
- Entonces el sistema rechaza la solicitud e informa al usuario de que las coordenadas son invalidas y pide que las vuelva a ingresar 


Caso de Uso UC2: Validar coordenadas ingresadas
Actor Principal: API geolocalizador
Actores involucrados e intereses:
-Usuario: El usuario ingreso sus coordenadas a la solicitud
-API geolocalizadoe: Debe validar los datos ingresados en la solicitud

Precondiciones: Usuario ingresó coordenadas a la solicitud
Postcondiciones (garantias de exito): El sistema devuelve la respuesta de validez de las coordenadas (valido o no valido).
Si es valido el sistema permite continuar con el registro de la solicitud.

Escenario principal de exito (Flujo basico):
1. El sistema recibe las coordenadas ingresadas en el UC1
2. El sistema envia las coordenadas al API
3. El API verifica las coordenadas ingresadas esten dentro del area de trabajo valido
4. El API responde con validacion de ubicacion al sistema
5. El sistema retorna el control a UC1

Extensiones (Flujos Alternativos):
3' Si las coordenadas ingresadas estan fuera del area de trabajo valido:
. Entonces el API responde con invalidacion de la ubicacion al sistema


