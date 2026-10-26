# Diseño del Juego: NEXUS (Versión Final)

## 1. Visión del juego
NEXUS es una experiencia interactiva de estrategia, gestión y exploración de realidades. El jugador asume el rol de un **Comandante de Nexos**, encargado de coordinar expediciones a través de múltiples dimensiones inestables. El objetivo principal es recolectar recursos, estabilizar fallas temporales y gestionar un equipo de exploradores especializados para evitar el colapso sistémico del universo NEXUS. La motivación del jugador radica en la progresión constante: desbloquear nuevos sectores del mapa, mejorar las estadísticas de sus exploradores mediante persistencia de datos y superar misiones cada vez más desafiantes.

## 2. Ciclo principal de juego (Core Loop)
El flujo de una partida se desarrolla de la siguiente manera:
1. **Inicio de sesión y carga:** El jugador ingresa a la aplicación de escritorio y autentica su perfil (recuperando su progreso guardado desde SQL Server).
2. **Menú Principal:** Selección de opciones para iniciar una expedición, gestionar inventario o consultar el estado de los exploradores.
3. **Exploración / Selección de Mapa:** El jugador elige un sector dimensional en el mapa estelar. Cada sector presenta riesgos, costos de energía y recompensas potenciales.
4. **Despliegue y Resolución de Misiones:** Se asignan exploradores según sus habilidades. El sistema procesa los eventos de la misión en función de las reglas de energía y recursos disponibles.
5. **Progresión y Recompensas:** Se obtienen nuevos ítems para el inventario, experiencia para los exploradores y recursos que se registran automáticamente en la base de datos.

## 3. Mecánicas y reglas
- **Exploradores:** Unidades activas con atributos de salud, nivel, especialización y estado (disponible, en misión, fatigado). Su rendimiento define el éxito en las expediciones.
- **Mapas y Sectores:** Entornos dimensionales con niveles de dificultad crecientes. Requieren requisitos mínimos de equipo para ser desbloqueados.
- **Energía:** Recurso crítico consumido al realizar exploraciones o misiones. Si la energía llega a cero, el jugador debe esperar su regeneración o consumir suministros del inventario.
- **Misiones:** Desafíos de tiempo o decisiones que otorgan recompensas basadas en la tirada de éxito o las estadísticas de los exploradores asignados.
- **Inventario:** Almacén de objetos, artefactos y recursos recolectados que pueden ser equipados o vendidos para mejorar la infraestructura del comando.

## 4. Diseño de pantallas (Wireframes conceptuales)

### Pantalla 1: Menú Principal
* **Navegación:** Punto central de entrada.
* **Elementos visibles:** 
  * Logotipo de NEXUS.
  * Botones de acción: *Nueva Expedición*, *Gestión de Exploradores*, *Inventario*, *Configuración* y *Salir*.
  * Indicador de estado del servidor SQL y usuario conectado.

### Pantalla 2: Exploración / Mapa
* **Navegación:** Accesible desde el menú principal; permite volver atrás.
* **Elementos visibles:**
  * Cuadrícula o lista de sectores dimensionales disponibles (Bloqueados / Desbloqueados).
  * Panel de detalles del sector seleccionado (Dificultad, Recompensas estimadas, Costo de energía).
  * Botón de *Iniciar Misión*.

### Pantalla 3: Misiones
* **Navegación:** Ventana emergente o pestaña activa durante el desarrollo de misiones.
* **Elementos visibles:**
  * Estado de la misión actual en curso (barra de progreso o registro de eventos).
  * Listado de exploradores asignados y su estado de salud/energía.
  * Botones de control: *Cancelar*, *Acelerar* o *Recoger Recompensa*.

### Pantalla 4: Exploradores e Inventario
* **Navegación:** Accesible desde el menú principal mediante un panel dual.
* **Elementos visibles:**
  * **Sección Izquierda (Exploradores):** Tarjetas con el avatar, nombre, nivel y atributos de cada miembro del equipo. Opción para subir de nivel o equipar objetos.
  * **Sección Derecha (Inventario):** Cuadrícula tipo grid con los ítems recolectados, descripción detallada al hacer clic y botones de uso/equipar.

## 5. Experiencia de usuario (UX)
* **Legibilidad:** Uso de tipografías claras de alta contraste (estilo futurista/consola, fondo oscuro con acentos en tonos neón).
* **Jerarquía visual:** Los botones de acción principal (como *Iniciar*) destacan visualmente frente a los de navegación secundaria.
* **Consistencia:** Mantener la misma paleta de colores corporativa y disposición de menús en todas las ventanas de Windows Forms.
* **Retroalimentación (Feedback):** Mensajes emergentes (MessageBox) o cambios de color inmediatos al realizar acciones como guardar datos o completar misiones.

## 6. Alcance y restricciones
* **Funcionalidades Prioritarias (MVP):** 
  * Autenticación de usuario conectada a SQL Server.
  * Visualización y navegación funcional entre las 4 pantallas principales en Windows Forms.
  * Operaciones CRUD básicas sobre el inventario y estado de los exploradores.
* **Funcionalidades Opcionales:**
  * Efectos de sonido ambientales y animaciones gráficas avanzadas.
* **Restricciones técnicas:**
  * El proyecto debe construirse sobre la base del código desarrollado en H3 en C#.
  * La persistencia de datos debe realizarse obligatoriamente mediante una base de datos relacional en SQL Server.
