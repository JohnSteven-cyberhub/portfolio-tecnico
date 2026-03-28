# 🗄️ Base de Datos en MySQL

## Descripción

Demostración de habilidades en diseño y administración de bases de datos relacionales usando **MySQL**.

---

## 📋 Contenido de este proyecto

- Creación de base de datos y tablas
- Inserción y consulta de datos (CRUD)
- Uso de JOINs, índices y relaciones entre tablas
- Exportación/importación de bases de datos

---

## 🧪 Ejemplo Práctico — Sistema de Gestión de Empleados

### 1. Crear la base de datos

```sql
CREATE DATABASE empresa_db;
USE empresa_db;
```

### 2. Crear tablas

```sql
CREATE TABLE departamentos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL
);

CREATE TABLE empleados (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    apellido VARCHAR(100) NOT NULL,
    correo VARCHAR(150) UNIQUE,
    salario DECIMAL(10, 2),
    id_departamento INT,
    fecha_ingreso DATE,
    FOREIGN KEY (id_departamento) REFERENCES departamentos(id)
);
```

### 3. Insertar datos

```sql
INSERT INTO departamentos (nombre) VALUES
('Tecnología'),
('Recursos Humanos'),
('Finanzas');

INSERT INTO empleados (nombre, apellido, correo, salario, id_departamento, fecha_ingreso) VALUES
('John', 'Estrella', 'john@empresa.com', 45000.00, 1, '2023-01-15'),
('María', 'López', 'maria@empresa.com', 38000.00, 2, '2022-06-10'),
('Carlos', 'Pérez', 'carlos@empresa.com', 52000.00, 3, '2021-03-22');
```

### 4. Consultas (SELECT + JOIN)

```sql
-- Ver todos los empleados con su departamento
SELECT 
    e.nombre,
    e.apellido,
    e.salario,
    d.nombre AS departamento
FROM empleados e
JOIN departamentos d ON e.id_departamento = d.id
ORDER BY e.salario DESC;

-- Salario promedio por departamento
SELECT 
    d.nombre AS departamento,
    AVG(e.salario) AS salario_promedio
FROM empleados e
JOIN departamentos d ON e.id_departamento = d.id
GROUP BY d.nombre;
```

### 5. Actualizar y eliminar

```sql
-- Actualizar salario
UPDATE empleados SET salario = 48000.00 WHERE id = 1;

-- Eliminar un registro
DELETE FROM empleados WHERE id = 3;
```

---

## 🛠️ Herramientas utilizadas

- **MySQL 8.x**
- **MySQL Workbench** (interfaz gráfica)
- Terminal / línea de comandos

---

## 📸 Capturas

> *(Agrega aquí capturas de pantalla de tu base de datos en MySQL Workbench)*

---

## 📚 Lo que aprendí

- Diseño de esquemas relacionales con llaves foráneas
- Consultas complejas con JOINs y funciones de agregación
- Buenas prácticas en nomenclatura y estructura de bases de datos
