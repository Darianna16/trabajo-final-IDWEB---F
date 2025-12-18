
# BobbleTea – Aplicación Web Empresarial (Bubble Tea)

BubbleTea es una aplicación web empresarial orientada a la presentación y venta de bebidas **Bubble Tea**, desarrollada como proyecto final del curso **Aplicaciones Web Empresariales**.  
El sistema integra frontend interactivo, backend en Python (Flask) y base de datos MySQL para la gestión de mensajes enviados por los clientes.

---

## Características Principales

- Navegación web completa mediante menú principal.
- Página de inicio con bebida destacada y productos en tendencia.
- Catálogo de productos y promociones.
- Carrito de compras interactivo con JavaScript.
- Formulario de contacto con almacenamiento en base de datos.
- Módulo administrador con autenticación.
- Backend desarrollado con Python (Flask).
- Base de datos MySQL.

---

## Tecnologías Utilizadas

- **Frontend:** HTML5, CSS3, JavaScript
- **Backend:** Python 3
- **Base de datos:** MySQL
- **Control de versiones:** Git y GitHub

---

## 📥 Clonar el Repositorio

```bash
git clone (https://github.com/Darianna16/trabajo-final-IDWEB---F)
cd NOMBRE-DEL-REPOSITORIO
````

---

## Crear y Activar el Entorno Virtual (venv)

### En Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### En Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 📦 Instalar Dependencias

```bash
pip install pymysql
```

(Opcional: usar `requirements.txt` si existe)

```bash
pip install -r requirements.txt
```

---

## Configuración de la Base de Datos (MySQL)

### 1. Crear la base de datos

```sql
CREATE DATABASE IF NOT EXISTS bubluetea 
CHARACTER SET utf8mb4 
COLLATE utf8mb4_general_ci;

USE bubluetea;
```

---

### 2. Crear las tablas

```sql
-- Tabla de usuarios (login administrador)
CREATE TABLE IF NOT EXISTS usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    usuario VARCHAR(50) UNIQUE NOT NULL,
    contrasena VARCHAR(255) NOT NULL
);

-- Tabla del formulario de contacto
CREATE TABLE IF NOT EXISTS formulario_contacto (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre_cliente VARCHAR(100) NOT NULL,
    correo_cliente VARCHAR(100) NOT NULL,
    telefono_cliente VARCHAR(20),
    mensaje_cliente TEXT NOT NULL,
    fecha_envio TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

### 3. Insertar usuario administrador (ejemplo)

```sql
INSERT INTO usuarios (usuario, contrasena)
VALUES ('admin', 'admin123');
```

> Nota: En un entorno real, la contraseña debe almacenarse cifrada.

---

## ▶ Ejecutar el Servidor

Con el entorno virtual activado:

```bash
python servidor.py
```

El sistema se ejecutará en:

```
http://localhost:8000
```

---

## Acceso al Administrador

* **Usuario:** admin
* **Contraseña:** admin123

Desde el panel administrador se pueden visualizar los mensajes enviados desde el formulario de contacto.

---

## Trabajo Futuro

* Registro e inicio de sesión de usuarios.
* Conexión completa de la página Cuenta a la base de datos.
* Implementación de pagos en línea.
* Control de roles más avanzado.
* Contenerización del proyecto.
* Mejoras de seguridad.

---

## Equipo de Desarrollo

**BobaTech Studio**
Proyecto académico – Aplicaciones Web Empresariales
- Valeria Abigai Ticona Nina
- Pamela Greis Cruz Kana
- Delaney Dariana Mendoza Larico 

---
