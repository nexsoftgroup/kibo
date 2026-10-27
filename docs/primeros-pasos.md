# Primeros pasos

De Kibo recién instalado a varias sesiones trabajando a la vez.

## 1. Abre o crea un proyecto

Un proyecto es una carpeta de trabajo. Puedes tener varios abiertos a la vez, como en VS Code. Siempre hay uno: la primera vez, Kibo crea y abre **Default** en tu carpeta de proyectos (`%USERPROFILE%\Kibo` en Windows, `~/Kibo` en Linux y macOS), y el último proyecto abierto no se cierra.

> **Para abrir sesiones, Claude Code con tu sesión iniciada**
>
> Si todavía no tienes Claude Code listo, Kibo te muestra su estado, el comando oficial para instalarlo (con **Copiar**) y un botón para iniciar sesión: se abre una consola y el login lo haces tú. Kibo no lee tus credenciales. Lo vuelves a abrir cuando quieras en **Kibo → Plataformas de IA…**. [Más sobre Claude Code en Kibo](cli.md).

- **Proyecto → Abrir proyecto…** abre el selector de carpetas del sistema; debajo, **Recientes** (hasta 8 proyectos y servidores que cerraste).
- **＋ Proyecto → En esta PC** crea uno nuevo, con su `CLAUDE.md`, su `README.md` y una **Wiki** lista para documentar.
- **＋ Proyecto → En un servidor (VPS)** para un proyecto cuyas sesiones corren en otra máquina, por SSH.

![El panel de proyectos con sus agentes, skills y tareas](img/02-proyectos.png)

## 2. Comprueba que Claude Code esté listo

Abajo a la derecha, en la barra de estado, ves el CLI del proyecto: **Claude Code**. Si falta o no iniciaste sesión, **Kibo → Plataformas de IA…** te guía.

## 3. Abre una sesión

**＋** en la fila del proyecto (o <kbd>Ctrl+Alt+N</kbd>) abre una sesión nueva. Por defecto ves su consola, con los controles de siempre del CLI. Con Claude Code, cada sesión lleva además un robot del color de su estado: cian trabajando, ámbar te espera, verde libre, gris inactiva.

## 4. Mira la conversación (Claude Code)

Con Claude Code, **💬** en la barra del área de trabajo (o <kbd>Ctrl+Alt+H</kbd>; en Mac <kbd>⌘⌥J</kbd>) muestra al costado la conversación, con la hora de cada mensaje. Con cualquier CLI, para pasarle un documento o una captura: pégalo (<kbd>Ctrl+V</kbd>), arrástralo o usa **📎 Adjuntar**.

## 5. Varias sesiones a la vez

**⊞** en la barra de pestañas trae cuadrículas armadas (2 columnas, 2 × 2, 3 × 2…). Arrastra una pestaña a un lugar para llenarlo.

![Cuadrícula de 2 × 2 con cuatro sesiones](img/04-cuadricula.png)

## 6. Agent Hub: tus equipos (Claude Code)

Con varios proyectos y varios agentes, **Agent Hub** (la tarjeta de arriba del panel izquierdo, o <kbd>Ctrl+Shift+T</kbd>) muestra **una tarjeta por equipo**: cada proyecto con su MAIN, sus agentes, cuántos trabajan o te esperan, y lo último que pasó. **Ver más** abre el detalle del equipo: cómo va hoy, cada agente con lo que hizo y una línea de tiempo. A la derecha, el **chat del equipo**: eliges **Para** (todos, un agente o varios equipos) y mandas una **orden** o una **consulta**.

Elige una MAIN con clic derecho en una sesión → **Hacer MAIN del proyecto**, o con el botón **Sin MAIN** de la tarjeta del equipo en Agent Hub. La MAIN y sus peers son siempre sesiones de Claude Code; la MAIN reparte el trabajo a los demás agentes del proyecto. Los permisos los sigues aprobando tú.

![Agent Hub: una tarjeta por equipo, el mapa de equipos y el chat del equipo](img/17-agent-hub.png)

## 7. Programa una tarea

**Tareas** (arriba, o <kbd>Ctrl+Shift+A</kbd>): a tal hora, Kibo abre la sesión y le escribe la instrucción, aunque Kibo esté cerrado. También desde una consola:

```
programar nueva --sesion wiki --cada 30m "Revisa los logs nuevos y anotá lo raro"
```

## Atajos que conviene saber

| Acción | Tecla |
|---|---|
| Buscar en proyectos, agentes, skills, tareas y conversaciones | <kbd>Ctrl+K</kbd> |
| Mostrar u ocultar la conversación | <kbd>Ctrl+Alt+H</kbd> (Mac <kbd>⌘⌥J</kbd>) |
| Chat de consultas 💬 | <kbd>Ctrl+Shift+Espacio</kbd> |
| Agent Hub · Tareas · Navegador | <kbd>Ctrl+Shift+T</kbd> · <kbd>Ctrl+Shift+A</kbd> · <kbd>Ctrl+Shift+B</kbd> |
| Sesión nueva · cerrar la pestaña | <kbd>Ctrl+Alt+N</kbd> · <kbd>Ctrl+Alt+W</kbd> |
| Cambiar de tema | <kbd>Ctrl+Alt+K</kbd> |
| Configuración | <kbd>Ctrl+,</kbd> |
| Atajos de teclado | <kbd>Ctrl+Alt+S</kbd> (Mac <kbd>⌘⌥S</kbd>) |

Todos se cambian en su propia ventana: **Ajustes → Atajos de teclado…** (<kbd>Ctrl+Alt+S</kbd>). En macOS, donde dice Ctrl es ⌘.

## Al cerrar

Las sesiones viven en un servicio aparte. Desde el menú **Kibo** eliges:

| Opción | La ventana | Las sesiones |
|---|---|---|
| **Salir de Kibo (las sesiones siguen)** · `kibo --salir` | se cierra | siguen |
| **Cerrar todo (también las sesiones)** · `kibo --cerrar-todo` | se cierra | se cierran |
| **Forzar cierre** · `kibo --forzar` | se corta ya | siguen |

---

[← Instalar](instalar.md)[Claude Code →](cli.md)
