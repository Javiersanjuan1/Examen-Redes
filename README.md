# Examen-Redes
Pregunta 1: Para dividir la red 172.16.0.0/24 de forma eficiente para los diferentes sectores de la base Eco, se emplea subnetting con VLSM (máscaras de longitud variable):

Departamento	Hosts Necesarios	Subred asignada	Máscara	Rango de hosts
Comando Central	~50	172.16.0.0/26	255.255.255.192	172.16.0.1–62
Defensa Perimetral	~30	172.16.0.64/27	255.255.255.224	172.16.0.65–94
Centro Médico	~20	172.16.0.96/27	255.255.255.224	172.16.0.97–126
Hangar y Taller	~14	172.16.0.128/28	255.255.255.240	172.16.0.129–142
Enlace Troncal	2	172.16.0.144/30	255.255.255.252	172.16.0.145–146
Pregunta 2: El enrutamiento estático se configura manualmente, ideal para redes pequeñas o enlaces simples, con control total del administrador. No se adapta automáticamente a fallos.

El enrutamiento dinámico utiliza protocolos que descubren rutas y se adaptan en tiempo real (como RIP u OSPF). Son más escalables y resilientes ante cambios.

RIP (Routing Information Protocol) es un protocolo de vector de distancia, fácil de configurar pero lento en converger.

OSPF (Open Shortest Path First) es de estado de enlace, más eficiente y rápido, ideal para redes grandes.

Diferencia clave:

Vector de distancia: usa saltos como métrica y comparte tablas completas.

Estado de enlace: tiene vista completa de la red y calcula la ruta más corta mediante Dijkstra.

Pregunta 3: El Sistema de Nombres de Dominio (DNS) traduce nombres fáciles de recordar (como holonet.rebelion.org) en direcciones IP necesarias para la comunicación entre dispositivos.

El proceso de resolución DNS:

El cliente pregunta a su servidor DNS por el nombre.

Si el DNS lo conoce, responde con la IP.

Si no, reenvía la consulta hasta llegar a un servidor que tenga la respuesta.

Un registro A asocia un nombre de dominio a una IP:

Ejemplo: planes.secretos → 192.168.50.100

Si el servidor DNS no está disponible, los dispositivos no pueden traducir nombres, por lo que las comunicaciones que dependen de nombres fallan.

Pregunta 4:TCP (Transmission Control Protocol) es confiable y orientado a conexión. Garantiza entrega, orden y control de errores. Es ideal para:

Transferencias críticas (e.g. planos de la Estrella de la Muerte)

Email, navegación web

UDP (User Datagram Protocol) es rápido pero no garantiza entrega ni orden. Útil para:

Streaming de video (X-Wing en batalla)

Juegos o voz IP (donde la velocidad es prioritaria)

TCP requiere más recursos y tiempo. UDP es liviano y rápido, ideal donde perder algunos paquetes es aceptable.

Pregunta 5:Cifrado simétrico: usa la misma clave para cifrar y descifrar. Es rápido, pero inseguro si la clave se comparte mal.

Ejemplo: Leia y Luke comparten una frase secreta para sus mensajes.

Cifrado asimétrico: usa un par de claves (pública y privada). Permite cifrar sin compartir la clave privada.

Ejemplo: un nuevo aliado recibe la clave pública de la Alianza para enviar mensajes cifrados.

Autenticación y no repudio:

Garantizan que un mensaje proviene de quien dice ser.

Se usa firma digital (clave privada) y verificación (clave pública).

SSH vs Telnet:

SSH cifra toda la sesión (usuario, contraseña, comandos).

Telnet envía todo en texto plano: inseguro.

Usar SSH protege contra espías imperiales en redes sensibles.
