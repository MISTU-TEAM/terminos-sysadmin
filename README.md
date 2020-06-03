

<p align="center">
   <!--<img src="https://user-images.githubusercontent.com/48721794/78295480-834b9180-752c-11ea-946d-2b890ad6adf3.png" alt="FULL PING logo" width="72" height="72">-->
   <img src="https://user-images.githubusercontent.com/48721794/81127936-1454c480-8f40-11ea-825c-93b0c6fb8582.png">
</p>
<br>

<div align="center">
   <h1>Indice</h1>
   <h3><a href="https://github.com/MISTU-TEAM/terminos-sysadmin#firewall">Firewall</a></h3>
   <h3><a href="https://github.com/MISTU-TEAM/terminos-sysadmin#dns">DNS</a></h3>
   <h3><a href="https://github.com/MISTU-TEAM/terminos-sysadmin#protocolos">Protocolos</a></h3>
</div>

<br>
<br>
<br>

# Firewall

El **Firewall** establece una barrera entre las redes internas seguras, controladas y fiables y las redes externas poco fiables como Internet, según sus reglas establecidas.
> Recursos Firewall:
> [Vídeo](https://www.youtube.com/watch?v=kDEX1HXybrU), [web](https://www.cisco.com/c/es_es/products/security/firewalls/what-is-a-firewall.html)

**Firewall de próxima generación:** Los Firewalls convencionales trastrea los dominios que proviene el tráfico, pero este tipo de Firewall supervisa el contenido del mensaje en busca de malware y la filtración de datos

**Firewall proxy:** Se trata de un dispositivo que filtra paquetes provenientes de redes exteriores, y posteriormente lo envia al servidor Proxy, para restringir con sus propias reglas.
> Recursos Firewall proxy:
> [Diagrama](https://www.computertechreviews.com/wp-content/uploads/2019/12/New-Project-14.jpg)

**Packet Filtering Firewall:** Los firewalls de filtrado de paquetes operan en la Capa 3 "Networking" (IP, ARP, IPsec, ICMP,...) del modelo OSI. Los firewalls de filtrado de paquetes toman decisiones de procesamiento basadas en direcciones de red, puertos o protocolos. No son seguros.
> Recursos Packet Filtering Firewall:
> [Diagrama](https://etutorials.org/shared/images/tutorials/tutorial_102/bssl_0205.gif), [web](https://www.sciencedirect.com/topics/computer-science/packet-filtering-firewall)

**SMLI** (Stateful Multilayer Inspection Firewall)**:** Almacena los atributos (IP, puerto,...) de cada conexión entrante en una base de datos llamado "stateful database", i en la que establece una sessión abierta. Cada paquete que se envia y recibe de esa sessión se comprueba que este registrada en la base de datos, y las reglas que se han configurado.
> Recursos SML:
> [Diagrama](https://www.researchgate.net/profile/Baha_Rababah/publication/324546844/figure/fig1/AS:616176103211009@1523919239568/Proxy-filtering-3-Stateful-Inspection-Firewall-A-Stateful-inspection-packet-creates-a.png), [web](https://es.wikipedia.org/wiki/Cortafuegos_stateful)

<br>
<hr>
<br>

# DNS:

**DNS** (Domain Name System)**:** Es un tipo de servidor que traduce una dirección IP a una serie de caracteres faciles de recordar, y a la inversa. Para ello utiliza la Base de datos que almacena el dominio, y la dirección IP a la que se asocia.
> Recursos DNS:
> [Vídeo](https://www.youtube.com/watch?v=mpQZVYPuDGU), [diagrama](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/05/02_07.png), [web](https://hacks.mozilla.org/2018/05/a-cartoon-intro-to-dns-over-https/)

**DoH** (DNS over HTTPS)**:**  DNS sobre HTTPS, su sistema hará una conexión (túnel) segura y encriptada a su servidor DNS y transferirá la solicitud y la respuesta a través de esa conexión. Cualquier ISP y/o operador de red en el medio no podrá ver qué nombres de dominio está buscando ni alterar la respuesta.

> Recursos DoH:
> [Vídeo](https://www.youtube.com/watch?v=mYUqkGY85zo), [vídeo2](https://youtu.be/hExRDVZHhig?t=241), [diagrama](https://www.menandmice.com/wp-content/uploads/2019/11/doh.jpg), [web](https://www.howtogeek.com/448629/how-dns-over-https-doh-will-boost-privacy-online/)

**DoT** (DNS over TLS)**:** DNS sobre TLS, autentica el servidor, el cliente y cifra los datos. DoT comunica por el puerto 853, lo que facilita a los administradores de red la capacidad de monitorear y bloquear consultas DNS, lo cual es importante para identificar y detener el tráfico malicioso. Mientras tanto, las consultas de DoH al utilizar el mismo puerto que el trafico HTTPS, esto brinda a los administradores de red menos visibilidad, a cambio brinda a los usuarios más privacidad.

> Recursos DoT:
> [Diagrama](https://www.menandmice.com/wp-content/uploads/2019/11/doh.jpg), 
[web](https://www.cloudflare.com/learning/dns/dns-over-tls/)

**DNSSEC** (Domain Name System Security Extensions)**:** DNSSEC certifica que el servidor DNS esta chequeando fuentes certificadas/de confianza/autentificadas, para que ningún intruso pueda falsificar una dirección o IP. Con el objetivo de tener una respuesta de "fuentes oficiales", pero no cifradas.

> Recursos DNSSEC:
> [Vídeo](https://www.youtube.com/watch?v=MrtsKTC3KDM), [diagrama](https://www.incibe.es/sites/default/files/contenidos/blog/20190604_dnssec/dnssec.jpg), 
[web](https://www.dominios.es/dominios/sites/dominios/files/1318333648229_0.pdf)


## Como puedo ver si tengo: DoH, DoT, DNS, DNSSEC?

Visita esta [pagina](https://www.cloudflare.com/ssl/encrypted-sni/) y comprueba que tipos de DNS tienes habilitado en tu navegador.

<br>
<hr>
<hr>
<br>

# Protocolos:

**SNMP** (Simple Network Management Protocol)**:** Este es un protocolo orientado a datagramas. Cualquiera de los dispositivos gestionados tendrá un agente que se comunica con el dispositivo central, el cual los gestiona. Dicho agente enviará información al mencionado dispositivo central, cuyo contenido será almacenado en una base de datos que se denomina MIB (Management Information Base). (SNMPv3, es la versión actual y estable)

> Recursos SNMP: [Habilitar SNMP](https://blog.paessler.com/how-to-enable-snmp-on-your-operating-system), [explición SNMP](https://www.redeszone.net/tutoriales/internet/protocolo-snmp-que-es/)

**FTP** (File Transfer Protocol)**:** Es un protocolo de transferència archivos, multimedia,... Existen diferentes tipos de FTP que lo hacen más seguro, i modos.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Modos:**

- <u>Modo Activo:</u> En este modo de funcionamiento el servidor FTP crea el canal de datos en el puerto TCP 20, mientras que en el lado del cliente se elige un puerto aleatorio superior al puerto TCP 1024. Esto es inseguro ya que abre un puerto aleatorio, este modo no se usa actualmente.
- <u>Modo Pasivo:</u> en este modo se hace a través del puerto 21 de control, el servidor FTP le dice al cliente FTP a qué puerto externo debe conectarse para transferir la información. De esta forma, el cliente establecerá una conexión desde el puerto que le haya indicado.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Tipos:** (De más seguro a menos)

- <u>SFTP:</u> Es un mètodo que usa SSH para connectarse al servidor FTP mediante SSH. Pero esto no encripta ----
- <u>FTPS:</u> Antes de intercambiar ninguna información con el servidor FTP, se realiza una negociación TLS/SSL para asegurar todo el canal de comunicación, por tanto, la autenticación y la transferencia de archivos está asegurada con TLS.
- <u>FTPES:</u> El cliente FTPS debe pedir explícitamente seguridad en el servidor, y luego pasar a un método de cifrado compatible por ambos. La diferencia principal es que FTPES negocia la comunicación encriptada, en cambio FTPS no.

> Recursos FTP: [Cliente FTP](https://www.smartftp.com/es-es/), [Servidor FTP](https://www.wftpserver.com)