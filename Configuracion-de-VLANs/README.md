# Configuración de VLANs con Cisco Packet Tracer

## Descripción

Este proyecto consiste en el diseño y la configuración de una topología de red en Cisco Packet Tracer. Se utilizan routers, switches y equipos finales para practicar la segmentación de una red mediante VLANs y el direccionamiento IPv4.

## Objetivo

Implementar una topología de red segmentada por VLAN, configurar sus puertas de enlace y preparar la comunicación entre diferentes redes.

## Tecnologías y herramientas

- Cisco Packet Tracer
- VLAN (Virtual Local Area Network)
- IPv4 y subnetting
- Router-on-a-Stick
- Troncales 802.1Q
- DHCP
- Enrutamiento entre routers

## Topología

La práctica está compuesta por dos routers conectados entre sí, switches de acceso y computadoras distribuidas en distintas VLAN.

![Topología de la red](topologia.png)

## Plan de direccionamiento

### Lado izquierdo

| VLAN | Red | Máscara | Puerta de enlace |
|---|---|---|---|
| 50 | 192.83.50.0/24 | 255.255.255.0 | 192.83.50.1 |
| 60 | 192.83.60.0/24 | 255.255.255.0 | 192.83.60.1 |
| 70 | 192.83.70.0/24 | 255.255.255.0 | 192.83.70.1 |

### Lado derecho

| VLAN | Red | Máscara | Puerta de enlace |
|---|---|---|---|
| 10 | 192.83.10.0/23 | 255.255.254.0 | 192.83.10.1 |
| 20 | 192.83.20.0/22 | 255.255.252.0 | 192.83.20.1 |
| 30 | 192.83.24.0/21 | 255.255.248.0 | 192.83.30.1 |

Nota: La red de la VLAN 30 se expresa como 192.83.24.0/21 porque esa es la dirección de red correspondiente a la máscara /21.

## Configuraciones realizadas

- Creación y asignación de VLANs en los switches.
- Configuración de puertos de acceso para las computadoras.
- Configuración de enlaces troncales entre los switches y los routers.
- Configuración de subinterfaces con encapsulación IEEE 802.1Q.
- Asignación de direcciones IP a las puertas de enlace.
- Configuración de pools DHCP para la asignación automática de direcciones IP.

## Verificación

Se pueden utilizar los siguientes comandos para comprobar la configuración:

```text
show vlan brief
show interfaces trunk
show ip interface brief
show ip dhcp pool
show ip dhcp binding
show ip route
```

## Aprendizajes

Esta práctica permite reforzar los conocimientos de segmentación de redes, direccionamiento IPv4, configuración de switches y routers, asignación automática de direcciones IP y diagnóstico de conectividad.

## Archivos del proyecto

- `Configuracion-de-VLANs.pkt`: archivo editable de Cisco Packet Tracer.
- `topologia.png`: captura de la topología implementada.

## Autor

Estudiante de Ingeniería en Sistemas Computacionales.

## Estado del proyecto

Práctica académica en desarrollo. La conectividad entre todas las VLAN debe verificarse mediante pruebas de comunicación.
