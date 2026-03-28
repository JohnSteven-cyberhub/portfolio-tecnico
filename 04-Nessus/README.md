# 🛡️ Escaneo de Vulnerabilidades con Nessus Essentials

## Descripción

Demostración del uso de **Nessus Essentials** de Tenable, una de las herramientas más populares para identificar vulnerabilidades de seguridad en sistemas y redes.

> ⚠️ **Aviso legal**: Todos los escaneos fueron realizados en entornos propios, máquinas virtuales o laboratorios controlados. Nunca en sistemas de terceros sin autorización.

---

## ¿Qué es Nessus Essentials?

Nessus Essentials es la versión gratuita de Nessus, que permite escanear hasta **16 IPs** y detectar miles de vulnerabilidades conocidas (CVEs), configuraciones incorrectas y problemas de seguridad.

---

## 🧪 Proceso de Escaneo

### Paso 1 — Instalación y configuración
1. Descargar Nessus Essentials desde [tenable.com](https://www.tenable.com/products/nessus/nessus-essentials)
2. Registrarse para obtener el código de activación gratuito
3. Acceder a la interfaz web: `https://localhost:8834`

### Paso 2 — Crear un nuevo escaneo
1. Ir a **New Scan**
2. Seleccionar tipo: *Basic Network Scan*
3. Configurar:
   - **Nombre**: Identificador del escaneo
   - **Targets**: IP o rango (ej. `192.168.1.0/24`)
4. Iniciar escaneo

### Paso 3 — Interpretar resultados

Los hallazgos se clasifican por severidad:

| Nivel | Color | Descripción |
|-------|-------|-------------|
| Critical | 🔴 Rojo oscuro | Vulnerabilidad explotable de inmediato |
| High | 🟠 Naranja | Alto riesgo, requiere atención urgente |
| Medium | 🟡 Amarillo | Riesgo moderado |
| Low | 🔵 Azul | Riesgo bajo |
| Info | ⚪ Gris | Información general, sin riesgo directo |

### Paso 4 — Acciones recomendadas
- Revisar cada hallazgo con su **CVE** asociado
- Aplicar parches del sistema operativo
- Deshabilitar servicios innecesarios
- Cambiar configuraciones inseguras por defecto

---

## 📊 Ejemplo de Hallazgo

```
Vulnerability: SSL/TLS Certificate Signed Using Weak Hashing Algorithm
Severity: Medium
CVE: CVE-2004-2761
Plugin ID: 35291

Description:
The remote host has an SSL/TLS certificate signed using a cryptographically
weak hashing algorithm (MD5 or SHA-1).

Solution:
Contact the Certificate Authority to have the certificate reissued using
a stronger hashing algorithm such as SHA-256.
```

---

## 🛠️ Entorno utilizado

- **Nessus Essentials** (versión gratuita)
- **Sistema escaneado**: Máquina virtual con Metasploitable2 (entorno de práctica)
- **Host**: Windows 10 / Kali Linux

---

## 📸 Capturas

> *(Agrega aquí capturas de pantalla del dashboard de Nessus con los resultados)*

---

## 📚 Lo que aprendí

- Configuración y uso de Nessus Essentials desde cero
- Interpretación de reportes de vulnerabilidades (CVEs)
- Priorización de vulnerabilidades por nivel de riesgo
- Relación entre resultados de Nessus y medidas de remediación
