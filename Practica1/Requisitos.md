Requisitos funcionales
- El sistema debe permitir que los clientes puedan ingresar solicitudes de retiro
- El sistema debe validar automáticamente que las coordenadas de la solicitud se encuentren dentro de una zona de retiro valida mediante un servicio de geolocalización.
- El sistema debe clasificar las solicitudes válidas en zonas geográficas predeterminadas.
- El sistema debe permitir al Coordinador registrar nuevas zonas de recolección predefinidas. 
- El sistema debe almacenar las zonas de recolección registradas para su uso posterior.
- El sistema debe permitir que el Coordinador genere rutas óptimas de recolección, entendidas como rutas que minimizan la distancia total entre los puntos de retiro dentro de una misma zona geográfica.
- El sistema debe permitir que el Recolector marque una solicitud como completada o no encontrada.
- El sistema debe permitir que los Recolectores generen un comprobante digital por cada retiro completado.
- El sistema debe permitir que el Coordinador de Ruta notifique a los Recolectores a través del módulo interno de mensajería del sistema, las rutas asignadas para su ejecución.
- El sistema debe impedir que un usuario tenga más de una solicitud activa al mismo tiempo. 
- El sistema debe permitir que el Cliente pueda editar una solicitud mientras esta se encuentre en estado Ingresada (es decir, antes de que haya sido asignada a un recolector o marcada como En Retiro).

Requisitos no funcionales
- El sistema permite inicio de sesión mediante contraseña única.
- El sistema debe soportar al menos 500 usuarios concurrentes sin degradación perceptible del rendimiento.
- El perfil Cliente debe acceder al sistema únicamente desde la aplicación móvil Android/iOS.
- El perfil Recolector debe acceder al sistema únicamente desde la aplicación móvil Android/iOS.
- El Coordinador de Ruta debe acceder al sistema únicamente desde la aplicación de escritorio para PC.

