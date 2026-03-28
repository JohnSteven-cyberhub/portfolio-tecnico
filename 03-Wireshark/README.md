# 📡 Análisis de Tráfico con Wireshark

## Descripción

Demostración del uso de **Wireshark**, la herramienta más utilizada para captura y análisis de paquetes de red en tiempo real.

> ⚠️ **Aviso legal**: La captura de tráfico fue realizada únicamente en redes propias o con autorización explícita.

---

## 🧪 Casos de Uso Demostrados

### 1. Captura básica de tráfico
- Selección de interfaz de red (eth0, wlan0)
- Inicio y detención de captura
- Guardado de capturas en formato `.pcap`

### 2. Filtros de captura más usados

| Filtro | Descripción |
|--------|-------------|
| `http` | Solo tráfico HTTP |
| `dns` | Consultas DNS |
| `tcp.port == 80` | Tráfico en puerto 80 |
| `ip.addr == 192.168.1.1` | Tráfico de una IP específica |
| `tcp.flags.syn == 1` | Paquetes SYN (inicio de conexión) |
| `!(arp)` | Excluir tráfico ARP |
| `http.request.method == "POST"` | Solo peticiones POST |

### 3. Análisis de protocolos

```
Protocolos analizados:
- TCP/IP — handshake de 3 vías
- HTTP  — peticiones y respuestas web
- DNS   — resolución de nombres de dominio
- ARP   — resolución de direcciones MAC
- ICMP  — ping y mensajes de error
```

### 4. Seguimiento de flujo TCP
- Clic derecho en paquete → *Follow TCP Stream*
- Permite ver la conversación completa entre cliente y servidor

### 5. Estadísticas útiles
- `Statistics > Protocol Hierarchy` — distribución de protocolos
- `Statistics > Conversations` — conexiones activas
- `Statistics > IO Graph` — gráfico de tráfico en el tiempo

---

## 📊 Ejemplo de Análisis

```
Frame 1: 74 bytes on wire
Ethernet II: src 00:1A:2B:3C:4D:5E, dst ff:ff:ff:ff:ff:ff
Internet Protocol: src 192.168.1.10, dst 192.168.1.1
Transmission Control Protocol: src port 52341, dst port 80
Hypertext Transfer Protocol: GET /index.html HTTP/1.1
```

---

## 🛠️ Entorno utilizado

- **Wireshark** versión 4.x
- **Sistema Operativo**: Windows / Kali Linux
- **Red analizada**: Red local propia

---

## 📸 Capturas

> *(Agrega aquí capturas de pantalla de tus análisis en Wireshark)*

---

## 📚 Lo que aprendí

- Captura e interpretación de paquetes de red en tiempo real
- Uso de filtros para aislar tráfico de interés
- Identificación de patrones de tráfico sospechosos
- Análisis del modelo OSI aplicado a tráfico real
