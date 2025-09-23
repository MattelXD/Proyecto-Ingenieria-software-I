Caso de Uso UC1: Ingresar solicitud de retiro
Actor Principal: Usuario y Usuario Registrado
Actores involucrados e intereses:
-Usuario: El usuario desea ingresar una solicitud de retiro para los recolectores recojan su material de reciclaje.

Precondiciones: Usuario tiene material de reciclaje que quiere que sea retirado 
Postcondiciones (garantias de exito): La solicitud de retiro es ingresada correctamente

Escenario principal de exito (Flujo basico):
1. Usuario abre aplicacion
2. Usuario elige la opcion de ingresar solicitud de retiro
3. Usuario crea su solicitud de retiro
4. Si el usuario lo desea, puede agregar una nota o comentario en su solicitud de retiro
5. Usuario ingresa su solicitud de retiro al sistema.
6. La solicitud de retiro es ingresada correctamente.

Extensiones (Flujos Alternativos):
5'. Si hay un problema en el sistema o hay algun problema de conexion:
- Entonces no se ingresa la solicitud de retiro y el sistema pide que lo vuelva a intentar.


Caso de Uso UC2: Agregar nota o comentario
Actor Principal: Usuario y Usuario Registrado
Actores involucrados e intereses:
-Usuario: Quiere agregar un nota o comentario en su solicitud de retiro.

Precondiciones: Usuario ha hecho su solicitud de retiro y ahora quiere agregar una nota o comentario a este. 
Postcondiciones (garantias de exito): La nota o comentario se agrega correctamente a la solicitud de retiro

Escenario principal de exito (Flujo basico):
1. Usuario agrega una nota o comentario a su solicitud de retiro
2. Usuario envia su nota o comentario junto con la solicitud de retiro.

Extensiones (Flujos Alternativos):



