# 🔍 Escaneo de Redes con Nmap

## Descripción

Demostración del uso de **Nmap (Network Mapper)**, una herramienta esencial en ciberseguridad para descubrimiento de hosts y auditoría de redes.

> ⚠️ **Aviso legal**: Todos los escaneos mostrados fueron realizados en entornos controlados y/o con autorización. El uso de Nmap en redes sin permiso es ilegal.

---

## 🧪 Comandos Utilizados

### Escaneo básico de host
```bash
nmap 192.168.1.1
```

### Escaneo de rango de IPs
```bash
nmap 192.168.1.0/24
```

### Detectar sistema operativo y versión de servicios
```bash
nmap -A -T4 192.168.1.1
```

### Escaneo de puertos específicos
```bash
nmap -p 22,80,443,3306 192.168.1.1
```

### Escaneo sigiloso (SYN scan)
```bash
nmap -sS 192.168.1.1
```

### Guardar resultados en archivo
```bash
nmap -oN resultado.txt 192.168.1.1
nmap -oX resultado.xml 192.168.1.1
```

### Escaneo de vulnerabilidades con scripts NSE
```bash
nmap --script vuln 192.168.1.1
```

---

## 📊 Ejemplo de Resultado

```
Starting Nmap 7.94 ( https://nmap.org )
Nmap scan report for 192.168.1.1
Host is up (0.0023s latency).
Not shown: 995 closed ports
PORT     STATE SERVICE    VERSION
22/tcp   open  ssh        OpenSSH 8.9
80/tcp   open  http       Apache httpd 2.4.52
443/tcp  open  https      Apache httpd 2.4.52
3306/tcp open  mysql      MySQL 8.0.32
```

---

## 🛠️ Entorno de práctica

- **Sistema Operativo**: Kali Linux / Parrot OS
- **Versión de Nmap**: 7.x
- **Red de prueba**: Red local controlada / TryHackMe / HackTheBox

---

## 📸 Capturas

> *(Agrega aquí capturas de pantalla de tus escaneos reales)*

---

## 📚 Lo que aprendí

- Identificación de hosts activos en una red
- Reconocimiento de puertos abiertos y servicios activos
- Detección de versiones de software para análisis de vulnerabilidades
- Uso de scripts NSE para auditoría automatizada
