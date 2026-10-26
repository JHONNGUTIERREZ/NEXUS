# Análisis Técnico y Decisiones de Diseño - NEXUS

## 1. Alternativas Evaluadas
* **Alternativa A (Continuar en Consola):** Descartada por no cumplir con la exigencia de crear una experiencia gráfica interactiva orientada a videojuegos de escritorio.
* **Alternativa B (Aplicación Web ASP.NET / Blazor):** Descartada debido a que el ecosistema y la base del curso se centran fuertemente en C# desktop con Windows Forms y conexiones directas a SQL Server.
* **Alternativa C (Windows Forms + SQL Server):** **Seleccionada.** Permite reutilizar de forma directa el código orientado a objetos del Hito 3, facilita el diseño visual mediante el diseñador gráfico de Visual Studio y garantiza persistencia relacional robusta.

## 2. Ventajas y Desventajas
* **Ventajas:** Aprovecha las clases de POO ya creadas en H3, curva de aprendizaje óptima para aplicaciones de escritorio en entornos corporativos y académicos, control total sobre los componentes gráficos.
* **Desventajas:** La interfaz nativa de Windows Forms puede verse anticuada si no se cuida el diseño visual y la paleta de colores.

## 3. Fuentes Técnicas y Verificación
* Documentación oficial de Microsoft sobre ADO.NET (`SqlConnection`, comandos SQL).
* Buenas prácticas de separación de responsabilidades (Clean Architecture / N-Tier aplicada a Windows Forms).
