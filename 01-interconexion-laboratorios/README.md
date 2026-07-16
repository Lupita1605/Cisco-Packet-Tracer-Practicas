# 📁 Práctica 1: Interconexión de Laboratorios LAN

### 📝 Descripción
Esta práctica consiste en el diseño, segmentación e interconexión de dos redes de área local (LAN) denominadas **Lab Gestión** y **Lab Civil**. Ambas redes se comunican de forma remota a través de un enlace WAN punto a punto que conecta los routers principales. El sistema incluye la integración de un servidor centralizado en el Laboratorio de Gestión encargado de proveer servicios a las terminales locales.

---

### 📊 Tabla de Direccionamiento Lógico

| Dispositivo | Interfaz | Dirección IP | Máscara de Subred | Puerta de Enlace (Gateway) |
| :--- | :--- | :--- | :--- | :--- |
| **PC0** | Fa0 | 172.16.10.2 | 255.255.255.0 | 172.16.10.1 |
| **Server0** | Fa0 | 172.16.10.50 | 255.255.255.0 | 172.16.10.1 |
| **Router4** | Gig0/1 (LAN) | 172.16.10.1 | 255.255.255.0 | N/A |

---

### 🛠️ Detalles Técnicos
* **Segmentos LAN:** 2 subredes independientes operando bajo prefijos `/24`.
* **Pruebas de Conectividad:** Validada mediante comandos `ping` exitosos bajo el protocolo ICMP de extremo a extremo.
