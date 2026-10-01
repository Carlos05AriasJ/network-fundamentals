# Network Fundamentals: Modelos OSI, TCP/IP y Flujo de Peticiones Web

Un desglose técnico detallado de los modelos de red principales, protocolos esenciales y la mecánica paso a paso detrás de una petición web estándar.


## Modelos de Referencia OSI y TCP/IP

Ambos modelos son formas distintas de representar la realización de una comunicación entre dispositivos en una red, organizando la transmisión de datos para que los dispositivos puedan comunicarse de manera correcta.

**Diferencia Principal:** La diferencia más clara es el número de capas que tiene cada modelo; el modelo OSI está compuesto por 7 capas, mientras que el modelo TCP/IP tiene 4 capas.
* **Capas del Modelo OSI:** 
  1. Física
  2. Enlace de datos
  3. Red
  4. Transporte
  5. Sesión
  6. Presentación
  7. Aplicación
* **Capas del Modelo TCP/IP:** 
  1. Acceso a la red
  2. Internet
  3. Transporte
  4. Aplicación

**Enfoque técnico:** El modelo OSI separa en varias capas algunos conceptos que en el modelo TCP/IP están agrupados en una sola (las capas de sesión, presentación y aplicación de OSI se agrupan por completo en la capa de aplicación de TCP/IP). Además, el modelo OSI está más orientado a entender las comunicaciones de red (aprendizaje), mientras que TCP/IP fue desarrollado específicamente para ser utilizado en Internet, siendo este el estándar implementado actualmente.


## Sistema de Nombres de Dominio (DNS) y Dirección IP

* **DNS (Domain Name System):** La principal tarea del DNS es traducir los nombres de dominio que los usuarios pueden recordar y memorizar de una manera sencilla en direcciones IP que los dispositivos utilizan para lograr comunicarse. Por ejemplo, al escribir el dominio `youtube.com`, el DNS traducirá ese dominio a una dirección IP. Si no existiera el DNS, los usuarios deberíamos aprendernos las direcciones IP específicas para cada sitio web.
* **Dirección IP:** Es un número único asignado a cada dispositivo conectado a una red que funciona como un indicador. Su función fundamental es que los datos lleguen a la ubicación deseada utilizando esta información para localizar el servidor al que enviar las solicitudes.


## Mecánica de los Protocolos HTTP y HTTPS

* **HTTP (HyperText Transfer Protocol):** Protocolo usado para transferir información entre el navegador y el servidor web (solicitudes y respuestas). Su vulnerabilidad crítica es que **transmite la información sin cifrar**, lo que significa que cualquier dato puede ser interceptado por otras personas durante el trayecto.
* **HTTPS (HyperText Transfer Protocol Secure):** Es en esencia la versión segura de HTTP. Permite la misma transferencia de datos entre el navegador y el servidor, pero con la diferencia crucial de que **utiliza cifrado de datos** para proteger la información. Es vital para sitios web que manejan información confidencial como contraseñas o datos bancarios.


## Esquema del funcionamiento de una petición web

Cuando un usuario escribe en su navegador una URL (por ejemplo, ://youtube.com), se realizan en pocos segundos los siguientes procesos en Internet:

1. El navegador analiza la URL para identificar el protocolo que debe utilizar y el nombre de la página web.
2. El navegador consulta a un servidor DNS para conocer la dirección IP del servidor donde se encuentra la página.
3. Una vez el servidor DNS responde con la IP correspondiente, el navegador localiza el servidor correcto y establece la conexión (cifrando los datos si se usa HTTPS).
4. El navegador envía la solicitud del protocolo al servidor solicitando la página web.
5. El servidor procesa la petición y responde enviando los datos necesarios para acceder e interpretar la página web.
6. El navegador recibe los datos, los interpreta y muestra la página web en la pantalla del dispositivo del usuario para que este pueda interactuar.


## Principales Conclusiones

* Los modelos en capas (OSI y TCP/IP) son indispensables para estructurar la comunicación de manera que dispositivos de diferentes fabricantes puedan entenderse de forma transparente.

* La resolución DNS actúa como una capa de abstracción necesaria para la usabilidad humana en Internet, evitando la necesidad de recordar cadenas numéricas complejas (IPs).

* La transición global hacia HTTPS es obligatoria para la ciberseguridad moderna, ya que el uso de HTTP expone directamente la privacidad de los datos de los usuarios ante ataques de interceptación (*sniffing*).

