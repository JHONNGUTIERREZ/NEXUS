# Arquitectura Propuesta - NEXUS v2.0 (Windows Forms y SQL Server)

## 1. Principio de Separación de Capas
Para evolucionar hacia una aplicación de escritorio profesional, se estructurará el proyecto bajo una **Arquitectura en Capas**:
* **Capa de Presentación (UI - Windows Forms):** Formularios gráficos (`FormLogin`, `FormMenuPrincipal`, `FormExploracion`, `FormInventario`) encargados exclusivamente de capturar la interacción del usuario y mostrar la información visual.
* **Capa de Lógica de Negocio (BLL):** Clases y métodos en C# que heredan y expanden la lógica desarrollada en H3 (validación de turnos, cálculo de éxito de misiones, gestión de atributos de exploradores).
* **Capa de Acceso a Datos (DAL):** Clases especializadas en la conexión y ejecución de consultas SQL mediante `SqlConnection`, `SqlCommand` y `SqlDataReader` hacia SQL Server.

## 2. Diagrama Conceptual de Arquitectura
