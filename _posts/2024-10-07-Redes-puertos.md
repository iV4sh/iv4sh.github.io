---
title: Redes y Puertos
author: iv4sh
date: 2024-10-26 14:00:00 +0800
categories: [Teoría, Redes]
tags: [Redes, Concepto]
render_with_liquid: false
description: Teoría sobre redes, puertos y servicios populares para protocolos TCP/IP y UDP
---

## **Redes**

>Las redes son fundamentales en el hacking porque sirven como el medio principal a través del cual los atacantes acceden, exploran, y explotan sistemas y datos. A través de técnicas como el escaneo de **puertos**, la sniffing de paquetes, y la inyección de comandos, los hackers pueden identificar vulnerabilidades en la infraestructura de red, interceptar comunicaciones, y comprometer sistemas enteros.


Las redes tienen una estructura básica, esta estructura es conocida como el modelo OSI, modelo que consta las siguientes 7 capas:

| Capa | Nombre          | Descripción                                                   |
| ---- | --------------- | ------------------------------------------------------------- |
| 7    | Aplicación      | La parte grafica, interfaz de control del usuario             |
| 6    | Presentación    | Traduce los datos cifrados para que sean humanamente legibles |
| 5    | Sesión          | Establece la conexión entre hosts                             |
| 4    | Transporte      | Garantiza el envió y la recepción de datos                    |
| 3    | Red             | Se encarga del direccionamiento y enrutamiento                |
| 2    | Enlace de Datos | Verifica errores y controla el flujo de la comunicación       |
| 1    | Física          | Dispositivos fisicos (cables, pcs, switches, routers)         |

### **Protocolos de conexión**

Existen dos protocolos básicos encargados de la conexión en las redes, estos son UDP y UTP cada uno con sus características ventajas y desventajas. Estos protocolos suelen operar bajo **puertos** y cada uno tiene sus puertos correspondientes. algunas de las características principales de los protocolos son las siguientes:

- **TCP (Transmission Control Protocol)**
	  -Es un protocolo orientado a conexión, pues establece una pre-conexión con el host de destino para garantizar la comunicación
	  -Enlazado al punto anterior al garantizar la comunicación asegura el envió y la recepción de datos, reduciendo las perdidas en la medida de los posible.
	  -Es el mas utilizado en internet dado la existencia del modelo de red TCP/IP
	  -Se encarga de la corrección de errores y reenvió de paquetes dañados
	  
- **UDP (User Datagram Protocol)**
	 -Es un modo de conexión muy rápido, notablemente mas rápido el protocolo TCP
	 -No es orientado a conexión, es decir no establece una conexión previa con el host lo que no garantiza una comunicación
	 -Gran riesgo de que haya perdida de paquetes

---

## **Puertos**

>En Redes, un **puerto** es un punto de comunicación dentro de una dirección IP que permite que diferentes servicios y aplicaciones envíen y reciban datos a través de una red. Los puertos actúan como canales de entrada y salida para el tráfico de datos y son fundamentales para la identificación y gestión de servicios específicos que se ejecutan en un servidor o dispositivo de red.


### Tipos de Puertos

1. **Puertos de Usuario (User Ports) o Puertos Dinámicos/Privados (49152-65535)**:
    - Estos puertos son utilizados por aplicaciones y servicios que no tienen un puerto estándar asignado. Se suelen usar para conexiones efímeras y asignaciones temporales.
2. **Puertos Registrados (1024-49151)**:
    - Estos puertos están registrados con la Internet Assigned Numbers Authority (IANA) para servicios y aplicaciones específicas. Son utilizados por aplicaciones que necesitan un puerto fijo pero no están reservados como puertos bien conocidos.
3. **Puertos Bien Conocidos (Well-Known Ports) o Puertos Estándar (0-1023)**:
    - Estos puertos están reservados para servicios y protocolos estándar, como HTTP, HTTPS, FTP y SSH. Estos puertos están bien definidos y se utilizan comúnmente para aplicaciones específicas.

---------------
### Puertos Populares

| Puerto | TCP | UDP | Nombre        | Descripción                                                                                                  |
| ------ | :-: | :-: | ------------- | ------------------------------------------------------------------------------------------------------------ |
| 1      |  ✅  |  ✅  | tcpmux        | Multiplexor TCP                                                                                              |
| 5      |  ✅  |  ✅  | rje           | Entrada de tarea remota (remote job entry)                                                                   |
| 7      |  ✅  |  ✅  | echo          | Protocolo Echo                                                                                               |
| 9      |  ✅  |  ✅  | discard       | Protocolo Discard (evaluación de conexiones)                                                                 |
| 11     |  ✅  |  ✅  | systat        | Información del sistema (enumera los puertos conectados)                                                     |
| 13     |  ✅  |  ✅  | daytime       | Protocolo Daytime: indica fecha y hora                                                                       |
| 17     |  ✅  |  ✅  | qotd          | Envía la cita del día (quote of the day)                                                                     |
| 18     |  ✅  |  ✅  | msp           | Protocolo de envío de mensajes                                                                               |
| 19     |  ✅  |  ✅  | chargen       | Protocolo Chargen: envía una cadena infinita de caracteres                                                   |
| 20     |  ✅  |     | ftp-data      | Transmisión de datos FTP                                                                                     |
| 21     |  ✅  |  ✅  | ftp           | Conexión FTP                                                                                                 |
| 22     |  ✅  |  ✅  | ssh           | Servicio Secure Shell                                                                                        |
| 23     |  ✅  |     | telnet        | Servicio Telnet                                                                                              |
| 25     |  ✅  |     | smtp          | Simple Mail Transfer Protocol                                                                                |
| 37     |  ✅  |  ✅  | time          | Protocolo de tiempo legible de forma mecanizada                                                              |
| 39     |  ✅  |  ✅  | rlp           | Protocolo de envío de recursos (Resource Location Protocol)                                                  |
| 42     |  ✅  |  ✅  | nameserver    | Servicio de nombres                                                                                          |
| 43     |  ✅  |     | nicname       | Servicio de directorio WHOIS                                                                                 |
| 49     |  ✅  |  ✅  | tacacs        | Terminal Access Controller Access Control System                                                             |
| 50     |  ✅  |  ✅  | re-mail-ck    | Protocolo de verificación de correo remoto (Remote Mail Checking)                                            |
| 53     |  ✅  |  ✅  | domain        | Resolución de nombres por DNS                                                                                |
| 67     |     |  ✅  | bootps        | Protocolo Bootstrap (servidor)                                                                               |
| 68     |     |  ✅  | bootpc        | Protocolo Bootstrap (cliente)                                                                                |
| 69     |     |  ✅  | tftp          | Protocolo Trivial de Transferencia de Ficheros (Trivial File Transfer Protocol)                              |
| 70     |  ✅  |     | gopher        | Búsqueda de documentos                                                                                       |
| 71     |  ✅  |     | genius        | Protocolo Genius                                                                                             |
| 79     |  ✅  |     | finger        | Proporciona información de contacto de usuarios                                                              |
| 80     |  ✅  |     | http          | Protocolo de Transferencia de HiperTexto (Hypertext Transfer Protocol)                                       |
| 81     |  ✅  |     |               | Torpark: Onion-Routing (no oficial)                                                                          |
| 82     |     |  ✅  |               | Torpark: Control (no oficial)                                                                                |
| 88     |  ✅  |  ✅  | kerberos      | Sistema de autenticación de red                                                                              |
| 101    |  ✅  |     | hostname      | Servicios de nombres de host (NIC Host Name)                                                                 |
| 102    |  ✅  |     | Iso-tsap      | Protocolo ISO-TSAP                                                                                           |
| 105    |  ✅  |  ✅  | csnet-ns      | Servidor de correo                                                                                           |
| 107    |  ✅  |     | rtelnet       | Telnet remoto                                                                                                |
| 109    |  ✅  |     | pop2          | Post Office Protocol v2 para comunicación de correo electrónico                                              |
| 110    |  ✅  |     | pop3          | Post Office Protocol v3 para comunicación de correo electrónico                                              |
| 111    |  ✅  |  ✅  | sunrpc        | Protocolo RPC para NFS                                                                                       |
| 113    |     |  ✅  | auth          | (Antiguo) servicio de autenticación                                                                          |
| 115    |  ✅  |     | sftp          | Protocolo de transferencia de archivos seguros o Simple File Transfer Protocol (versión simplificada de FTP) |
| 117    |  ✅  |     | uucp-path     | Transmisión de datos entre sistemas Unix                                                                     |
| 119    |  ✅  |     | nntp          | Transmisión se noticias en Newsgroups                                                                        |
| 123    |     |  ✅  | ntp           | Protocolo de sincronización de tiempo                                                                        |
| 137    |  ✅  |  ✅  | netbios-ns    | NETBIOS Servicio de nombres                                                                                  |
| 138    |  ✅  |  ✅  | netbios-dgm   | NETBIOS Servicio de envío de datagramas                                                                      |
| 139    |  ✅  |  ✅  | netbios-ssn   | NETBIOS Servicio de sesiones                                                                                 |
| 143    |  ✅  |  ✅  | imap          | Internet Message Access Protocol para comunicación de correo electrónico                                     |
| 161    |     |  ✅  | snmp          | Simple Network Management Protocol                                                                           |
| 162    |  ✅  |  ✅  | snmptrap      | Simple Network Management Protocol Trap                                                                      |
| 177    |  ✅  |  ✅  | xdmcp         | X Display Manager                                                                                            |
| 179    |  ✅  |     | bgp           | Border Gateway Protocol                                                                                      |
| 194    |  ✅  |  ✅  | irc           | Internet Relay Chat                                                                                          |
| 199    |  ✅  |  ✅  | smux          | SNMP UNIX Multiplexer                                                                                        |
| 201    |  ✅  |  ✅  | at-rtmp       | Enrutamiento AppleTalk                                                                                       |
| 209    |  ✅  |  ✅  | qmtp          | Quick Mail Transfer Protocol                                                                                 |
| 210    |  ✅  |  ✅  | z39.50        | Sistema de información bibliográfico                                                                         |
| 213    |  ✅  |  ✅  | ipx           | Internetwork Packet Exchange                                                                                 |
| 220    |  ✅  |  ✅  | imap3         | IMAP v3 para comunicación de correo electrónico                                                              |
| 369    |  ✅  |  ✅  | rpc2portmap   | Coda Filesystem Portmapper                                                                                   |
| 370    |  ✅  |  ✅  | codaauth2     | Servicio Coda Filesystem Authentication                                                                      |
| 389    |  ✅  |  ✅  | ldap          | Lightweight Directory Access Protocol                                                                        |
| 427    |  ✅  |  ✅  | svrloc        | Service Location Protocol                                                                                    |
| 443    |  ✅  |     | https         | HTTPS (HTTP a través de SSL/TLS)                                                                             |
| 444    |  ✅  |  ✅  | snpp          | Simple Network Paging Protocol                                                                               |
| 445    |  ✅  |     | microsoft-ds  | SMB a través de TCP/IP                                                                                       |
| 464    |  ✅  |  ✅  | kpasswd       | Modificación de contraseña para Kerberos                                                                     |
| 500    |     |  ✅  | isakmp        | Protocolo de seguridad                                                                                       |
| 512    |  ✅  |     | exec          | Remote Process Execution                                                                                     |
| 512    |     |  ✅  | comsat/biff   | Mail Client y Mail Server                                                                                    |
| 513    |  ✅  |     | login         | Inicio de sesión en ordenador remoto                                                                         |
| 513    |     |  ✅  | who           | Whod User Logging Daemon                                                                                     |
| 514    |  ✅  |     | shell         | Remote Shell                                                                                                 |
| 514    |     |  ✅  | syslog        | Servicio Unix System Logging                                                                                 |
| 515    |  ✅  |     | printer       | Servicios de impresión Line Printer Daemon                                                                   |
| 517    |     |  ✅  | talk          | Talk Remote Calling                                                                                          |
| 518    |     |  ✅  | ntalk         | Network Talk                                                                                                 |
| 520    |  ✅  |     | efs           | Extended Filename Server                                                                                     |
| 520    |     |  ✅  | router        | Routing Information Protocol                                                                                 |
| 521    |     |  ✅  | ripng         | Routing Information Protocol para IPv6                                                                       |
| 525    |     |  ✅  | timed         | Servidor de tiempo                                                                                           |
| 530    |  ✅  |  ✅  | courier       | Courier Remote Procedure Call                                                                                |
| 531    |  ✅  |  ✅  | conference    | Chat a través de AIM y IRC                                                                                   |
| 532    |  ✅  |     | netnews       | Servicio Netnews Newsgroup                                                                                   |
| 533    |     |  ✅  | netwall       | Broadcast de emergencia                                                                                      |
| 540    |  ✅  |     | uucp          | Unix-to-Unix Copy Protocol                                                                                   |
| 543    |  ✅  |     | klogin        | Kerberos v5 Remote Login                                                                                     |
| 544    |  ✅  |     | kshell        | Kerberos v5 Remote Shell                                                                                     |
| 546    |  ✅  |  ✅  | dhcpv6-client | DHCP v6 Client                                                                                               |
| 547    |  ✅  |  ✅  | dhcpv6-server | DHCP v6 Server                                                                                               |
| 548    |  ✅  |     | afpovertcp    | Apple Filing Protocol a través de TCP                                                                        |
| 554    |  ✅  |  ✅  | rtsp          | Control de streams                                                                                           |
| 556    |  ✅  |     | remotefs      | Remote Filesystem                                                                                            |
| 563    |  ✅  |  ✅  | nntps         | NNTP a través de SSL/TLS                                                                                     |
| 587    |  ✅  |     | submission    | Message Submission Agent                                                                                     |
| 631    |  ✅  |  ✅  | ipp           | Internet Printing Protocol                                                                                   |
| 631    |  ✅  |  ✅  |               | Common Unix Printing System (no oficial)                                                                     |
| 636    |  ✅  |  ✅  | ldaps         | LDAP a través de SSL/TLS                                                                                     |
| 674    |  ✅  |     | acap          | Application Configuration Access Protocol                                                                    |
| 694    |  ✅  |  ✅  | ha-cluster    | Servicio Heartbeat                                                                                           |
| 749    |  ✅  |  ✅  | kerberos-adm  | Kerberos v5 Administration                                                                                   |
| 750    |     |  ✅  | kerberos-iv   | Servicios Kerberos v4                                                                                        |
| 873    |  ✅  |     | rsync         | Servicios de transmisión de datos rsync                                                                      |
| 992    |  ✅  |  ✅  | telnets       | Telnet a través de SSL/TLS                                                                                   |
| 993    |  ✅  |     | imaps         | IMAP a través de SSL/TLS                                                                                     |
| 995    |  ✅  |     | pop3s         | POP3 a través de SSL/TLS                                                                                     |

---