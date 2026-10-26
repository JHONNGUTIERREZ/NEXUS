# NEXUS
# NEXUS - Sistema de Gestión y Expediciones Multidimensionales

## 📋 Descripción del Proyecto
**NEXUS** es una aplicación de escritorio desarrollada en **C# con Windows Forms y SQL Server**, concebida como un videojuego de estrategia, gestión y exploración de realidades. El proyecto evoluciona desde una arquitectura basada en consola (Hito 3) hacia una interfaz gráfica robusta y orientada a objetos, implementando persistencia relacional segura de datos.

---

## 🚀 Funcionalidades Implementadas
* **Autenticación de Usuarios:** Conexión segura a base de datos relacional para validación de perfiles y sesiones.
* **Gestión de Exploradores:** Administración de atributos (salud, nivel, energía y estado operativo).
* **Módulos de Expedición y Misiones:** Selección de sectores dimensionales con reglas de progreso y recompensas.
* **Control de Inventario:** Almacenamiento y gestión en tiempo real de recursos y artefactos recolectados.

---

## 🛠️ Tecnologías y Arquitectura
* **Lenguaje:** C# (.NET / Windows Forms)
* **Base de Datos:** Microsoft SQL Server (ADO.NET)
* **Arquitectura:** Patrón en capas (Presentación - UI, Lógica de Negocio - BLL, Acceso a Datos - DAL)

---

## ⚙️ Cómo Ejecutar el Proyecto
1. Clona este repositorio en tu equipo local.
2. Abre la solución en **Visual Studio**.
3. Configura la cadena de conexión (`connectionString`) hacia tu instancia local de SQL Server en el archivo de configuración.
4. Ejecuta el script de creación de base de datos provisto en el proyecto y compila la solución en Visual Studio (`F5`).

---

## 📁 Documentación del Proyecto
Toda la documentación técnica, de diseño y arquitectura se encuentra disponible en la carpeta [docs/](docs/):
* [Diseño del Juego](docs/diseno-del-juego.md)
* [Arquitectura Actual (H3)](docs/arquitectura-actual.md)
* [Arquitectura Propuesta](docs/arquitectura-propuesta.md)
* [Modelo de Datos Propuesto](docs/modelo-de-datos-propuesto.md)
* [Análisis Técnico](docs/analisis-tecnico.md)
