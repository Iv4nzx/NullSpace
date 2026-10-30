# NULLSPACE

*Una experiencia de terror psicológico en primera persona, ambientada en un inquietante edificio comercial interconectado.*

> Despiertas sobre una alfombra húmeda bajo luces fluorescentes parpadeantes. En algún lugar de un edificio imposible, hay una salida esperándote. Restablece la energía, explora las habitaciones y encuentra el camino de regreso. Pero recuerda algo: hay otra cosa que está aprendiendo la distribución del edificio junto contigo.

**NULLSPACE** es un juego de terror atmosférico en primera persona que se centra en la exploración, el sonido, la orientación y la supervivencia. Tu objetivo es sencillo: restablecer los circuitos necesarios y escapar. El edificio, naturalmente, tiene otros planes.

---

## 📜 Historia del proyecto

**NULLSPACE anteriormente  Forgotten Memories.**

El proyecto comenzó su desarrollo bajo el nombre de **Forgotten Memories** y evolucionó con el tiempo hasta convertirse en la experiencia de terror que es hoy.

El cambio de nombre representa una nueva etapa en el desarrollo del juego, conservando la esencia, el concepto y la visión original del proyecto.

Forgotten Memories forma parte de la historia de NULLSPACE y de su evolución como proyecto independiente.

---

*Renderizado inicial del entorno creado en Blender utilizando recursos originales del proyecto. Desarrollo en progreso.*

## 🎮 La experiencia

- **Una amenaza persistente:** El Oyente es una criatura original que rastrea pistas visuales y auditivas, busca tu ubicación y puede perder tu rastro.
- **Cada disparo tiene un precio:** Una pistola semiautomática compacta puede darte tiempo para escapar, pero el ruido revela tu posición.
- **Un entorno interconectado:** Explora aproximadamente entre 8 y 12 habitaciones funcionales, incluyendo oficinas, áreas de servicio y rutas que conducen de regreso a la salida.
- **Una arquitectura inquietante:** Las aberturas descentradas, la escasez de puntos de referencia y las puertas estratégicas convierten la orientación en parte del desafío.
- **Varios niveles de dificultad:** Fácil, Medio, Difícil y Pesadilla modifican los requisitos para restablecer los circuitos sin introducir niveles separados.
- **Más que combate:** Las puertas, la cobertura, la elección de rutas y la administración de munición influyen en tus posibilidades de sobrevivir.

La experiencia descrita todavía está en desarrollo. Algunas características y mecánicas podrían no estar completamente implementadas en la versión actual.

## 👁️ La amenaza

### El Oyente

Algo se mueve por el edificio y reacciona a las pistas que dejas a tu paso.

El Oyente está diseñado para detectar señales visuales y auditivas. Puede seguir pistas, buscar tu ubicación y perderte de vista.

Sobrevivir depende de comprender tu entorno, controlar el ruido y saber cuándo avanzar.

## ⚡ Jugabilidad

Tu objetivo principal es restablecer los circuitos eléctricos necesarios y llegar a la salida.

La cantidad de interacciones necesarias depende de la dificultad seleccionada:

| Dificultad | Objetivo |
|---|---|
| Fácil | Activar un interruptor |
| Medio | Restablecer el sistema básico de dos interruptores |
| Difícil | Restablecer los circuitos necesarios y un circuito local adicional |
| Pesadilla | Restablecer los circuitos necesarios y completar un objetivo local adicional |

Las dificultades Difícil y Pesadilla incorporan un circuito local adicional que requiere accionar un pestillo durante un breve intervalo o encontrar un fusible marcado.

Todas las dificultades conducen a la misma salida. Se pretende que sea posible completar el juego incluso sin munición.

## 🛠️ Tecnología

| Componente | Tecnología |
|---|---|
| Motor de videojuegos | Godot 4.7.2 |
| Renderizado | Forward+ |
| Recursos 3D | Blender 5.2.1 LTS |
| Modelado y animación | Recursos originales del proyecto |
| Plataforma principal de desarrollo | Linux |
| Plataforma adicional | Windows x86-64 |
| Android | Versión preliminar experimental |

La versión para Windows se genera mediante una compilación cruzada desde el entorno de desarrollo y todavía no ha sido validada mediante pruebas nativas en Windows.

Los requisitos mínimos del sistema aún no están establecidos.

Los informes de rendimiento deben interpretarse teniendo en cuenta el hardware probado, la resolución y la configuración gráfica utilizada.

## 🚧 Estado del desarrollo

**Versión actual:** [v0.3.1, corrección del inicio en Windows](https://github.com/marius4lui/NULLSPACE/releases/tag/v0.3.1)

Esta versión corrige un problema relacionado con la creación de nuevas partidas desde la pantalla de reanudación en Windows e incluye el juego completo de la versión v0.3.

El proyecto continúa siendo una versión preliminar inestable.

### Limitaciones actuales

- La dificultad Fácil cuenta con una partida completa probada mediante una exportación nativa del juego.
- Los demás niveles de dificultad se han completado mediante pruebas automatizadas en escenas reales, pero todavía requieren partidas completas adicionales en versiones nativas y pruebas auditivas.
- La versión para Windows se ha generado mediante compilación cruzada, pero no se ha probado de forma nativa.
- La compatibilidad con Android continúa siendo experimental.
- La instalación en Android, los controles táctiles, el audio, el rendimiento en dispositivos físicos y las partidas completas todavía no han sido verificados.

La rama pública `main` contiene la versión integrada del juego con dos interruptores.

La rama `feat/difficulty-room1` incorpora cuatro modos de dificultad predefinidos sin añadir nuevos niveles, enemigos, armas ni un sistema de inventario.

### 📱 Versión preliminar para Android

La versión experimental para Android incorpora:

- Controles táctiles para el movimiento y la cámara.
- Acciones táctiles para disparar e interactuar.
- Perfiles gráficos adaptados a dispositivos móviles.
- Gestión de pausas y reanudaciones.

La versión de depuración firmada utiliza la plantilla local sin conexión. No se trata de una versión definitiva para Android.

Consulta la [documentación de compilación y las limitaciones de Android](https://github.com/marius4lui/NULLSPACE/blob/main/tools/android/README.md) para obtener más información.

## 🚀 Instalación y ejecución

### Requisitos

- Godot 4.7.2 estable.
- Las plantillas de exportación correspondientes de Godot para generar compilaciones.
- Git.
- Bash para utilizar el script de compilación proporcionado.

### 1. Clonar el repositorio

```bash
git clone https://github.com/marius4lui/NULLSPACE.git
cd NULLSPACE
```

### 2. Importar el proyecto

```bash
godot --editor --path game --import --quit
```

### 3. Ejecutar el juego

```bash
godot --path game
```

### 4. Compilar para Linux

```bash
bash tools/build.sh linux
```

Después de completar la compilación, ejecuta el archivo generado:

```bash
./build/linux/nullspace.x86_64
```

### Compilaciones para otras plataformas

Utiliza `windows` en lugar de `linux` para generar una compilación para Windows, o utiliza `all` para compilar todos los destinos compatibles configurados en el proyecto.

Si utilizas una versión portátil del ejecutable de Godot, configura la variable de entorno `NULLSPACE_GODOT_BIN` con la ruta de ese ejecutable antes de iniciar el script de compilación.

No necesitas Blender para ejecutar una versión ya compilada del juego. Los recursos de producción y sus generadores se mantienen en los directorios de código fuente del proyecto.

## 🎮 Controles

| Acción | Control |
|---|---|
| Moverse | WASD |
| Mirar alrededor | Ratón |
| Correr | Shift |
| Agacharse | Ctrl |
| Encender o apagar la linterna | F |
| Interactuar | E |
| Disparar | Botón izquierdo del ratón |
| Recargar | R |
| Pausar | Escape |

Las opciones de configuración incluyen audio, sensibilidad e inversión del ratón, campo de visión, opciones de pantalla, VSync, límites de FPS y reducción del movimiento o de los destellos.

Consulta también la [guía de pruebas del juego](https://github.com/marius4lui/NULLSPACE/blob/main/docs/PLAYTEST.md).

## 📚 Documentación del proyecto

Explora el diseño del juego, las decisiones técnicas, el progreso del desarrollo y las pautas para contribuir.

| Recurso | Descripción |
|---|---|
| [Diseño del juego](https://github.com/marius4lui/NULLSPACE/blob/main/GAME_DESIGN.md) | Jugabilidad, mundo, criaturas y combate |
| [Dirección artística](https://github.com/marius4lui/NULLSPACE/blob/main/ART_DIRECTION.md) | Estilo visual y objetivos artísticos |
| [Arquitectura](https://github.com/marius4lui/NULLSPACE/blob/main/ARCHITECTURE.md) | Arquitectura técnica |
| [Registro de decisiones](https://github.com/marius4lui/NULLSPACE/blob/main/DECISIONS.md) | Decisiones técnicas documentadas |
| [Estado del proyecto](https://github.com/marius4lui/NULLSPACE/blob/main/STATUS.md) | Progreso actual del desarrollo |
| [Registro de incidencias](https://github.com/marius4lui/NULLSPACE/blob/main/ISSUES.md) | Problemas conocidos y limitaciones |
| [Plan de producción](https://github.com/marius4lui/NULLSPACE/blob/main/docs/NEXT_PRODUCTION_ACCEPTANCE.md) | Próximas tareas de desarrollo |
| [Documentación del sitio web](https://github.com/marius4lui/NULLSPACE/blob/main/docs/WEBSITE.md) | Código del sitio y vista previa local |
| [Créditos](https://github.com/marius4lui/NULLSPACE/blob/main/CREDITS.md) | Créditos del proyecto |
| [Licencias](https://github.com/marius4lui/NULLSPACE/blob/main/LICENSES.md) | Licencias y avisos legales |

## 🤝 Contribuciones

Los informes de errores, las sugerencias y las contribuciones técnicas ayudan a mejorar el proyecto.

- [Informar de un error o sugerir una mejora](https://github.com/marius4lui/NULLSPACE/issues/new/choose)
- [Participar en las discusiones del proyecto](https://github.com/marius4lui/NULLSPACE/discussions)
- [Consultar las pautas de contribución](https://github.com/marius4lui/NULLSPACE/blob/main/CONTRIBUTING.md)
- [Consultar la política de seguridad](https://github.com/marius4lui/NULLSPACE/blob/main/SECURITY.md)

## 🎨 Recursos originales

NULLSPACE utiliza recursos de producción originales. Los archivos fuente editables y los registros de generación y exportación se mantienen como parte del proyecto.

No se utilizan paquetes de contenido descargados.

## 📌 Información sobre el lanzamiento

NULLSPACE está disponible actualmente como una versión preliminar inestable.

Todavía no se ha anunciado una fecha de lanzamiento definitiva. Las características, la compatibilidad con plataformas, el rendimiento y los sistemas de juego pueden cambiar durante el desarrollo.

---

**Restablece la energía. Aprende cómo funciona el edificio. Encuentra la salida.**
