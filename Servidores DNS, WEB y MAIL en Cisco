
# Simulación de Infraestructura de Red: Servidores DNS, WEB y MAIL en Cisco Packet Tracer

Este repositorio contiene el diseño, configuración y validación de una arquitectura de red empresarial distribuida simulada en **Cisco Packet Tracer**. El proyecto demuestra la integración de dos subredes locales interconectadas mediante un enlace troncal de fibra óptica y la implementación de servicios críticos en la capa de aplicación.

---

## 🌐 Arquitectura y Topología de la Red

La topología está diseñada para segmentar el tráfico local y simular un entorno corporativo con conectividad de extremo a extremo (*End-to-End*):

*   **Subred A (`192.168.10.0/24`):** Alberga las estaciones de trabajo del área principal (incluyendo la estación de administración `PC0 - Guadalupe` y `PC1 - Sasha`) y el cluster de servidores de la organización.
*   **Subred B (`192.168.20.0/24`):** Representa el segmento remoto de la organización, donde se ubican los nodos de trabajo `PC2` y `PC3`.
*   **Enlace Backbone (`10.10.10.0/24`):** Conexión de alta velocidad y baja latencia mediante fibra óptica que interconecta los enrutadores centrales (`Router0` y `Router1`).

---

## 📊 Matriz de Direccionamiento IP

| Dispositivo | Interfaz | Dirección IP | Máscara de Subred | Puerta de Enlace (Gateway) | Descripción / Rol |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Router0** | Gig0/0/1 | `192.168.10.1` | `255.255.255.0` | N/A | Gateway de la Subred A |
| **Router0** | Gig0/0/0 | `10.10.10.1` | `255.255.255.0` | N/A | Interfaz de Enlace Troncal (Fibra) |
| **Router1** | Gig0/0/1 | `192.168.20.1` | `255.255.255.0` | N/A | Gateway de la Subred B |
| **Router1** | Gig0/0/0 | `10.10.10.2` | `255.255.255.0` | N/A | Interfaz de Enlace Troncal (Fibra) |
| **www.itsx.edu.mx**| Fa0 | `192.168.10.254`| `255.255.255.0` | `192.168.10.1` | Servidor Web y DNS Institucional |
| **Server-PT S** | Fa0 | `192.168.10.250`| `255.255.255.0` | `192.168.10.1` | Servidor de Correo (MAIL) |
| **PC0 (Guadalupe)**| Fa0 | `192.168.10.2` | `255.255.255.0` | `192.168.10.1` | Estación de Trabajo (Cliente) |
| **PC1 (Sasha)** | Fa0 | `192.168.10.3` | `255.255.255.0` | `192.168.10.1` | Estación de Trabajo (Cliente) |
| **PC3** | Fa0 | `192.168.20.3` | `255.255.255.0` | `192.168.20.1` | Estación de Trabajo Remota (Cliente) |

---

## 🚀 Implementación y Validación de Servicios

### 1. Sistema de Nombres de Dominio (DNS) y Servidor WEB (HTTP)
Se configuró un servidor DNS centralizado para resolver los nombres de dominio de la infraestructura local:
*   **Dominio registrado:** `www.itsx.edu.mx` apuntando a la dirección IP del servidor web correspondiente.
*   **Validación:** Resolución mediante consultas directas en la consola (`nslookup`) y carga exitosa de la interfaz gráfica a través del navegador web incorporado desde múltiples clientes de la red.

```bash
nslookup www.itsx.edu.mx

```

### 2. Servicio de Mensajería Electrónica (MAIL - SMTP/POP3)

Configuración de una plataforma de correo corporativo bajo el dominio `@itsx.edu.mx` utilizando los protocolos **SMTP** para el envío y **POP3** para el almacenamiento/recuperación de correspondencia:

* **Cuentas activas en la simulación:**
* `guadalupe@itsx.edu.mx` (Asignada a `PC0`)
* `sasha@itsx.edu.mx` (Asignada a `PC1`)


* **Evidencia de Funcionamiento:**
* Transmisión exitosa del mensaje *"Que tal amiga, como has estado?"* originado en la cuenta de Guadalupe hacia el buzón de Sasha.
* Control de respuestas síncronas reflejado directamente en los registros del *Mail Browser* de los terminales simulados.



### 3. Conectividad End-to-End (ICMP)

Prueba de enrutamiento estático/dinámico a través de la infraestructura troncal:

```bash
ping 192.168.20.3

```

*Garantiza que las políticas de enrutamiento permiten el flujo correcto de datos entre subredes distantes.*

---

## 🛠️ Requisitos de Ejecución

* **Cisco Packet Tracer v8.0** o superior.
* Para visualizar la simulación, clona este repositorio y abre el archivo `Unidad 1_Actividad 5.pkt`.

```

```
