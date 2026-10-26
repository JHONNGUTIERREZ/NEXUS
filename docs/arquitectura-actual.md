# Arquitectura Actual (H3) - NEXUS

## 1. Clases y Componentes Principales
En el estado actual del Hito 3, NEXUS se compone principalmente de clases en C# diseñadas bajo un enfoque orientado a objetos inicial:
* **Clase Explorador / Tripulante:** Gestiona los atributos básicos (nombre, salud, nivel, energía).
* **Clase Misión / Sector:** Controla las reglas lógicas y los requerimientos de cada expedición.
* **Clase Inventario:** Administra de forma básica los ítems o recursos recolectados en memoria.
* **Consola Principal / Menú (Program.cs):** Interfaz basada en texto (consola de comandos) que orquesta el flujo de interacción mediante menús iterativos (`switch` / `while`).

## 2. Funcionalidades Implementadas
* Registro y simulación de expediciones por medio de consola.
* Gestión en memoria RAM de los objetos creados durante la ejecución del programa.
* Validación de reglas básicas de negocio (energía disponible y éxito/fracaso de misiones según atributos).

## 3. Limitaciones Reales
* **Persistencia Volátil:** Todos los datos (exploradores, inventario y progreso) se pierden al cerrar la consola, ya que no existe conexión a una base de datos.
* **Interfaz Limitada:** Al ser una aplicación de consola, carece de la experiencia visual gráfica (GUI) necesaria para un videojuego inmersivo.
* **Acoplamiento Alto:** La lógica del juego y la interacción con el usuario están fuertemente entrelazadas en el flujo principal de código.
