# Novedades de Kibo

Lo que cambia en cada versión de Kibo. Las versiones siguen
[versionado semántico](https://semver.org/lang/es/): `MAYOR.MENOR.ARREGLO`.


## 1.0.5 · 2026-10-28

Descarga y archivos: [Release v1.0.5](https://github.com/nexsoftgroup/kibo/releases/tag/v1.0.5).

### Corregido

- **Los mensajes entre agentes ya no aparecen como si los hubieras escrito tú:** Kibo escribía en la consola de un
  agente abierto lo que le decía otro agente (o la MAIN) y lo enviaba. El agente lo tomaba como un mensaje tuyo y, si
  estabas escribiendo en esa consola, se mezclaba con tu texto. Ahora Kibo no escribe nada en la consola de un agente
  abierto: los agentes se comunican entre ellos directamente. Kibo sólo despierta, con el mensaje, a un agente que
  está cerrado ([#11](https://github.com/nexsoftgroup/kibo/issues/11)).
- **Tampoco los otros avisos que Kibo escribía en la consola:** el de «el archivo quedó libre» del candado entre
  agentes y el mensaje entre las MAIN de distintos proyectos. Un agente frenado por el candado sigue con otra cosa y
  vuelve a intentarlo, o se coordina con el otro. Kibo sólo despierta, con el mensaje, a una MAIN que está cerrada.

### Cambiado

- **Las actualizaciones se descargan sólo desde GitHub:** Kibo busca la versión nueva y descarga el instalador
  únicamente de los Releases de NexSoft en GitHub. kibo.nexsoftgroup.com ya no es respaldo. «Leer más» y la página de
  descarga también llevan a GitHub.
- **Los comandos de la terminal** (`install.ps1` e `install.sh`) descargan sólo de GitHub. Si GitHub no responde, lo
  dicen y no instalan.
- **Las versiones 1.0.0 a 1.0.2 no se actualizan solas a la 1.0.5:** buscaban sus actualizaciones sólo en
  kibo.nexsoftgroup.com, que ya no aloja instaladores. Si tienes una de ellas, instala la 1.0.5 a mano desde GitHub,
  encima de la que tienes: tus proyectos y conversaciones se conservan.
- **Términos de uso 1.2:** la cláusula 4 nombra sólo a GitHub como el lugar de donde Kibo busca y descarga sus
  actualizaciones.

## 1.0.4 · 2026-10-27

Descarga y archivos: [Release v1.0.4](https://github.com/nexsoftgroup/kibo/releases/tag/v1.0.4).

### Cambiado

- **Lenguaje neutro en los tres idiomas:** en español, «tú» sin voseo ni regionalismos; en inglés, internacional; en
  portugués de Brasil, «você» estándar. Incluye los mensajes que Kibo les escribe a la MAIN y a los peers. También
  cambian algunos nombres: «clave SSH» (antes «llave»), el estado «Inactiva» (antes «Tranquila») y el nombre de la
  extensión en inglés y portugués («Kibo — point out», «Kibo — apontar») ([#10](https://github.com/nexsoftgroup/kibo/issues/10)).
- **La MAIN evita darle el mismo archivo a dos peers a la vez:** lo tiene como norma en su rol.
- **Cada sesión que abre Kibo sabe trabajar en equipo:** al empezar recibe cómo derivar, ver el equipo y no pisarse.
  La MAIN sabe que los peers se derivan tareas sin pasar por ella.
- **Términos de uso 1.1 y política de privacidad:** ahora nombran a GitHub (las versiones publicadas por NexSoft) como
  el lugar donde Kibo busca y descarga sus actualizaciones, con kibo.nexsoftgroup.com de respaldo. Es así desde la 1.0.3.

### Añadido

- **Los agentes ya no se pisan:** si dos peers del mismo proyecto quieren editar el mismo archivo a la vez, Kibo frena
  al segundo, le dice quién lo está editando y lo deja esperando. Cuando el primero termina su turno, Kibo le avisa al
  segundo que ya puede seguir. Un archivo nunca queda bloqueado para siempre: se libera solo a los 15 minutos sin
  cambios. Sólo afecta a las sesiones que abre Kibo ([#2](https://github.com/nexsoftgroup/kibo/issues/2)).
- **Los agentes se derivan tareas entre sí:** cualquier agente puede pasarle una tarea a otro del mismo proyecto,
  aunque esté inactivo: Kibo lo despierta con el mensaje. Antes, si el agente que hacía falta estaba inactivo, la
  tarea se cortaba. Todo queda en el registro del equipo, y cualquier agente puede ver quién está en el equipo y en
  qué estado. Si su trabajo no se cruza, el que tiene un archivo puede cederlo antes. No se despierta una Wiki
  detenida ni una sesión abierta en otra ventana ([#3](https://github.com/nexsoftgroup/kibo/issues/3)).
- **Pestañas agrupadas por proyecto,** como los grupos del navegador. Con pestañas de varios proyectos abiertas, cada
  proyecto tiene su rótulo en la barra, con su color, su nombre y cuántas pestañas tiene. Un clic despliega sus pestañas
  y otro las pliega. La pestaña que estás mirando y las fijadas 📌 quedan siempre a la vista, y Kibo recuerda qué
  proyectos dejaste desplegados ([#4](https://github.com/nexsoftgroup/kibo/issues/4)).
- **Varias capturas de una vez, como en WhatsApp:** con el editor de la captura abierto, Ctrl+V suma otra a la tira de
  abajo. Cada una tiene sus propios dibujos y su comentario; un clic en la miniatura la edita y su ✕ la saca.
  **Adjuntar** las manda todas en orden, cada una con su comentario ([#5](https://github.com/nexsoftgroup/kibo/issues/5)).
- **Arrastrar archivos y carpetas del árbol a la consola:** su referencia queda escrita, sin enviar. Para Claude y
  Gemini va como `@ruta`, que la IA lee como archivo. También funciona en la cuadrícula y en la conversación ([#6](https://github.com/nexsoftgroup/kibo/issues/6)).
- **Un color para cada proyecto:** desde su menú ⋯ → **Color del proyecto…** eliges cian, verde, ámbar, violeta,
  naranja, rojo o automático. Se usa en el panel de proyectos, en Agent Hub, en el mapa de equipos y en los rótulos de
  las pestañas ([#7](https://github.com/nexsoftgroup/kibo/issues/7)).
- **Elegir la MAIN desde Agent Hub:** el aviso «Sin MAIN» de la tarjeta de un equipo (y de su detalle) ahora es un
  botón. Abre las sesiones del proyecto para que elijas cuál es la MAIN, o te deja crear una nueva ([#8](https://github.com/nexsoftgroup/kibo/issues/8)).
- **Pegar capturas y archivos en el chat del equipo:** en el chat de Agent Hub, Ctrl+V con una imagen abre el editor
  de capturas (puedes sumar varias y comentar cada una) y los archivos copiados del Explorador se adjuntan al mensaje.
  Antes no hacía nada ([#9](https://github.com/nexsoftgroup/kibo/issues/9)).

### Corregido

- **El chat del equipo muestra quién está trabajando,** aunque no sea la MAIN.
- **Esc** en el editor de capturas ya no cierra Agent Hub.

## 1.0.3 · 2026-10-25

Descarga y archivos: [Release v1.0.3](https://github.com/nexsoftgroup/kibo/releases/tag/v1.0.3).

### Cambiado

- **Las actualizaciones llegan desde GitHub** (Releases de NexSoft) y, si GitHub no responde, desde
  kibo.nexsoftgroup.com. Siempre con la firma de NexSoft y el SHA-256.

### Corregido

- **El botón Agent Hub contaba de más:** decía, por ejemplo, «10 te esperan» cuando te esperaban 2, porque sumaba
  agentes ya cerrados. Ahora cuenta lo mismo que las tarjetas de los equipos
  ([#1](https://github.com/nexsoftgroup/kibo/issues/1)).
- Se reforzó el control de las direcciones desde las que Kibo baja sus actualizaciones.

## Instalación desde GitHub · 2026-10-25

Sin versión nueva de la app: cambia cómo se instala.

- **Los comandos de la terminal ahora bajan todo de GitHub Releases** y, antes de abrir o instalar nada, comprueban la
  firma de NexSoft y el SHA-256. Si GitHub no responde o algo no pasa esas comprobaciones, lo intentan con
  kibo.nexsoftgroup.com, con las mismas comprobaciones.
  - Windows: `irm https://github.com/nexsoftgroup/kibo/releases/latest/download/install.ps1 | iex`
  - Linux y macOS: `curl -fsSL https://github.com/nexsoftgroup/kibo/releases/latest/download/install.sh | sh`
- Los comandos anteriores, de kibo.nexsoftgroup.com, siguen funcionando y hacen lo mismo.


## 1.0.2 · 2026-10-24

Descarga y archivos: [Release v1.0.2](https://github.com/nexsoftgroup/kibo/releases/tag/v1.0.2).

### Añadido

- **Worktree por peer**, una opción por proyecto que viene apagada y sólo se puede prender en repos de git (menú ⋯ del
  proyecto → **Worktree por peer: activar**). Con la opción prendida, cada peer nuevo trabaja en su propia copia del
  repo (`<proyecto>.kibo-worktrees/<peer>`) y en su rama `kibo/<peer>`, así los peers no se pisan. La MAIN sigue en
  la carpeta principal; para que un peer trabaje ahí, la MAIN lo crea con `peers crear <nombre> --principal`.
- **Integrar el trabajo de un peer** lo decides tú, desde el menú ⋯ → **Integrar «peer» → rama (N commits)…**, y
  nunca la MAIN. Kibo pone la rama al día (rebase) y la suma sin merge commit. Si hay conflicto, no toca nada.
- **Quitar el worktree de un peer:** se quita solo cuando ya está todo integrado y el peer está cerrado. Si queda
  trabajo sin integrar, avisa cuánto se perdería y pide confirmar.

[Cómo funciona el worktree por peer](docs/worktree-por-peer.md).

## 1.0.1 · 2026-10-24

Pequeña mejora sobre la 1.0.0. Descarga y archivos: [Release v1.0.1](https://github.com/nexsoftgroup/kibo/releases/tag/v1.0.1).

### Añadido

- **Menú ⋯ en cada proyecto** de la lista (el mismo del clic derecho, en lugar del lápiz suelto): **Renombrar…**,
  **Cerrar proyecto** y la Wiki del proyecto.
- **Detener o activar la Wiki por proyecto:** **Wiki: detener** cierra su sesión para que no gaste tokens, Kibo deja de
  pasarle conversaciones y la MAIN ya no la ve ni la usa. **Wiki: activar** la retoma donde quedó, con lo que ya había
  documentado. Cada proyecto decide: puedes tenerla apagada en uno y activa en otro.

### Cambiado

- **Sin límite de agentes vivos por proyecto:** creas o despiertas todos los peers que necesites.
- **La MAIN cuida el costo:** sabe que cada peer vivo es una sesión de la IA que gasta de tu plan y memoria de la PC.
  Antes de crear uno nuevo reutiliza uno libre, y si ya hay 5 o más vivos te pregunta antes de crear otro.

### Corregido

- La pantalla de **Términos de uso** del instalador ya no muestra el aviso de borrador.
- **Chat del equipo de Agent Hub:** lo que escribes aparece al instante, con «enviando…», en vez de esperar a que la
  MAIN o el peer lo reciba (con la MAIN dormida tardaba varios segundos). Si no se pudo mandar, el texto vuelve a la
  caja.

## 1.0.0 

Primera versión pública, en **beta**: hecha y probada a fondo con Claude Code. Probada en Windows 11 (pruebas de interfaz y de motor) y en Linux con Ubuntu 24.04 dentro de WSL, con ventana real; macOS experimental: sin probar en una Mac, hasta la primera corrida de las pruebas automáticas en GitHub, que se estrenan con esta versión.

### Añadido

- **Instalar desde la terminal, en Windows** (el comando de hoy está en [Instalar](README.md#instalar)): pide permiso antes de instalar cada cosa que falte (Git for Windows y Claude Code) y cancela si no lo autorizas; después baja el instalador de Kibo, comprueba su SHA-256 y lo abre. En español, inglés o portugués, según el idioma de Windows.

- **Instalar desde la terminal, en Linux y macOS** (el comando de hoy está en [Instalar](README.md#instalar)): hace las mismas preguntas, baja el paquete de Kibo del sitio, comprueba su SHA-256 y lo instala para tu usuario en `~/Kibo/kibo`, sin `sudo`. Probado en Ubuntu 24.04 (WSL); en macOS, experimental.

- **Barra de menús** arriba (Proyecto · Vista · Tema · Idioma · Ajustes · Kibo), con el proyecto activo, **Tareas** y **Navegador**; se maneja también con Alt o F10. En Windows reemplaza la barra de título del sistema sin perder los bordes, Snap, Win+flechas ni Alt+F4; en Linux queda el marco del sistema; en macOS los menús van en la barra de menús del sistema.

- **Barra de estado** abajo: cómo están tus agentes (un clic te lleva al que te necesita) y el CLI del proyecto.

- **Barra del área de trabajo** de lado a lado, con el nombre de la sesión y sus herramientas (renombrar, conversación, adjuntar, captura, adjuntos, copiar, limpiar, ir al final).

- **Cada mensaje de la conversación con su hora con segundos** (y la fecha si no es de hoy), también en el registro de `Conversaciones/`.

- **Pestañas nuevas:** solapas en una sola fila, con ‹ › ⌄ y la rueda para recorrerlas, y **grupos de pestañas** con nombre y color, que se pliegan y se arrastran.

- **Agent Hub:** en el detalle del equipo, buscador de agentes desde 8; hasta 60 por equipo; **Abrir su consola** cuando un agente te necesita.

- **Notificaciones de escritorio** opcionales (⚙ Configuración): qué avisar (terminó, te espera, pide permiso), qué mostrar (nombre y mensaje, sólo el nombre o nada específico) y cuándo; en Windows, tocar el aviso abre la sesión.

- **Atajos de teclado configurables,** en su propia ventana (Ajustes → Atajos de teclado…, o Ctrl+Alt+S; en Mac ⌘⌥S): una combinación de fábrica para cada acción, con buscador, que se cambia, avisa si choca con otra y vuelve a la de fábrica.

- **Cuadro guiado de Claude Code:** su estado (no instalado, sin sesión o listo), el comando oficial para instalarlo con **Copiar**, y un botón para iniciar sesión que abre una consola donde el login lo haces tú. Se vuelve a abrir en **Kibo → Plataformas de IA…**.

- **La barra de estado** dice en el centro «Producto creado por NexSoft · visitanos en nexsoftgroup.com»; un clic abre el sitio.

- **Proyecto «Default»:** si no hay ningún proyecto abierto, Kibo crea y abre «Default» en la carpeta de proyectos. Siempre queda uno abierto.

- **Volver a lo hablado por fecha:** la orden `historial` (`--hoy`, `--ayer`, `--fecha`, `--desde`/`--hasta`, `--sesion`, `--buscar`) para que un agente relea lo hablado, por ejemplo después de que se le comprima la conversación. Los agentes se enteran solos de que existe.

- **macOS y Linux en la interfaz:** ⌘ en los atajos de Mac, «Mostrar en Finder» / «Mostrar en la carpeta», textos de tareas con launchd o systemd/cron, la consola del sistema en lugar de PowerShell.

- **Los mensajes del motor en tres idiomas** (errores y avisos de Kibo, de Agent Hub, de las tareas y de los servidores, y lo que llega desde el navegador).

### Cambiado

- **«Sala de mando» pasa a llamarse «Agent Hub»** en toda la interfaz, en los tres idiomas y sin traducir. Su entrada es una tarjeta, la primera del panel izquierdo, arriba de PROYECTOS, con «N trabajando · N te esperan» y un latido mientras hay agentes trabajando.

- **Agent Hub, rediseñado:** en vez de una columna por proyecto, una **tarjeta por equipo** (proyecto, MAIN, agentes, uso de hoy y lo último que pasó) y **Ver más** con el detalle del equipo (Cómo va, Agentes del equipo, Lo que pasó y sus tareas); pestañas **Agentes · Tareas · Historial · Archivos**; el **chat del equipo** a la derecha con Para, Lidera, Ordenar / Consultar y el menú «…»; un **mapa de equipos**, y un avatar de color por proyecto.

- **Hace falta Claude Code instalado y con sesión iniciada** para abrir sesiones, agentes, peers, Agent Hub y consultas. Sin eso se pueden crear y abrir proyectos.

- **Proyecto → Abrir proyecto…** abre directo el selector de carpetas del sistema, y debajo quedan **Recientes** (hasta 8 proyectos y servidores cerrados).

- **Desinstalar Kibo…** pasa al menú **Kibo**; los **Atajos de teclado**, a su propia ventana.

- **La conversación arranca oculta:** por defecto se ve la consola de la sesión; **💬** (o Ctrl+Alt+H; en Mac ⌘⌥J) la muestra al costado, y se recuerda por sesión. Se fueron los botones ◫ y ⌨.

- **El menú ≡ pasa a la barra de menús,** con los mismos grupos; el CLI del proyecto y el estado de los agentes pasan a la barra de estado.

- **Actualizar ya no pide reinstalar:** una instalación sin git se convierte sola al tocar **Actualizar ahora**, con una copia de lo que reemplaza en `respaldo-actualizacion/<fecha>/`, y vuelve todo atrás si algo falla.

- **Agent Hub despierta a la MAIN sólo con novedades de lo que ella encargó;** lo que le pides tú directo a un peer, o lo que hace la Wiki, ya no lo despierta.

- **Tema Claro:** la consola sube el contraste de los colores pensados para fondo oscuro y los textos atenuados se leen mejor.

### Arreglado

- Desinstalar (`uninstall.sh`, y desde ⚙ en Linux y macOS) se cortaba solo sin desinstalar nada ni avisar.

- Con un `config.json` cortado o roto, Kibo no abría: ahora abre con lo válido y guarda una copia del dañado.

- Las tareas con `cron` fallaban con un `PATH` muy largo (por ejemplo en WSL).

- En Linux se perdían los avisos del chat con muchas letras con tilde.

- Con muchas consolas abiertas, la más vieja podía quedar en blanco.

- Al cerrar lugares de la cuadrícula, la consola de lo que quedaba no se veía.

- El área para escribir de la consola podía quedar cortada abajo al entrar a una sesión.

- «trabajando · 2» con una sola sesión trabajando, y avisos de «te espera» o «parece trabado» que no eran ciertos (sesiones ya cerradas).

- Un bucle de avisos entre la MAIN y la sesión de la Wiki.

- **Despertar** un peer desde Agent Hub dejaba el encargo escrito sin enviar: ahora Kibo comprueba que llegó y, si no, reintenta y avisa a la MAIN.

- En Agent Hub y en la conversación aparecía texto pegado como `<pasted_content …>` en crudo.

- Los resúmenes de Agent Hub borraban los `_` de las palabras.

- Al tocar un aviso de escritorio con Kibo minimizado, la ventana no respondía al mouse.

### Seguridad

- Kibo no lee ni toca las credenciales de Claude Code: el login lo haces tú en su consola, y Kibo sólo mira si hay una sesión iniciada.

- Buscar y aplicar versiones nunca pide usuario ni contraseña (sin red o sin acceso, no hace nada) y «Leer más» sólo abre páginas `https://`.

- `historial` es sólo de lectura, sólo lee sesiones del mismo proyecto y tapa las credenciales que reconoce.

- Kibo no contesta por ti los permisos ni el cartel «¿confías en esta carpeta?» de Claude Code: los marca como «te necesita».

- Los avisos que Kibo le pasa a la MAIN ya no llevan el rótulo de un mensaje tuyo.

- Las notificaciones de escritorio pueden no mostrar ni el nombre ni el mensaje del agente.

## 0.2.0 · 2026-10-21

### Añadido

- **Linux y macOS**, además de Windows: `install.sh` (con Git o en una línea con `curl`), rutas y comando `kibo` para cada sistema, el ícono junto al reloj y el arranque con el sistema. Linux probado en Ubuntu 24.04 (WSL y Docker); macOS escrito, todavía sin probar en una Mac.

- **Tareas programadas con el programador de cada sistema:** el Programador de tareas en Windows, systemd de usuario o `cron` en Linux, y `launchd` en macOS.

- **Idiomas:** la interfaz y la extensión del navegador en español, inglés y portugués (Brasil).

- **Temas:** «Kibo» (el de siempre, por defecto), «Oscuro» y «Claro». Cambian en vivo toda la interfaz, el editor y las consolas (VS Code, adentro, mantiene el suyo), y se recuerda la elección.

- **Menú ≡ por grupos,** con su submenú al costado: Proyecto ▸ · Vista ▸ · Tema ▸ · Idioma ▸ · Ajustes ▸ · Kibo ▸.

- **Desinstalar** desde ⚙ Configuración → Desinstalar Kibo, o con `uninstall.ps1` / `uninstall.sh`. Pregunta si conservas tus datos o borras todo. Los proyectos no se tocan nunca.

- **Versiones:** la versión instalada a la vista; **Buscar versión nueva…** con **Leer más** y **Actualizar ahora**, que no pisa archivos tocados a mano; aviso automático a los 30 s de abrir y cada 6 h, con «No avisarme de esta»; nunca pide usuario ni contraseña.

- **Las sesiones sobreviven al cerrar Kibo:** un servicio de sesiones aparte mantiene vivas las consolas; al volver, cada pestaña se reengancha. Al salir: **Salir de Kibo (las sesiones siguen)**, **Cerrar todo (también las sesiones)** o **Forzar cierre**.

- **Sala de mando** (desde la 1.0.0, **Agent Hub**): una columna por proyecto, cada uno con su **MAIN**; caja **Orden / Consulta**; **Para: … ▾** para mandar a uno, varios o todos los proyectos; con 2 o más, **Lidera: … ▾**; mensajes **MAIN ↔ MAIN** entre proyectos, a la vista.

- **Paneles izquierdo y derecho** fijos, flotantes u ocultos, con ancho ajustable y recordado.

- **Recuadro de abajo con selector:** Equipo en vivo, Proyectos recientes, Mensajes entre agentes u Ocultar.

- **Buscador (Ctrl+K)** de proyectos, agentes, skills, tareas y del texto de las conversaciones.

- **Editor:** al seleccionar texto, **Comentar** y **¿Para qué es esto?**, una consulta aparte con el contexto del agente, sin tocar su conversación, con **Aplicar corrección** y **Enviar al agente actual**.

- **Chat de consultas 💬 (Ctrl+Shift+Espacio):** preguntarle a un agente sin interrumpirlo; las consultas se guardan en `<proyecto>/Conversaciones/Consultas/`.

- **VS Code completo en una pestaña**, con su licencia aceptada por la persona, y **Abrir en VS Code** desde el árbol de archivos.

- **Extensión del navegador 1.7.0, sólo donde la actives:** «Sólo esta pestaña», «Siempre en este sitio» o «En todas las pestañas», con «Sitios activados» para quitarlos y «Desactivar aquí».

### Cambiado

- **Adjuntos por proyecto:** lo que adjuntas en una sesión se guarda en `<proyecto>/Adjuntos/<fecha>/`.

- **Grupo «Agentes»** en el panel de proyectos, con Activos e Inactivos adentro.

- **Barra de pestañas:** ＋, ⊞ y 💬 quedan fijos a la derecha.

- **La extensión del navegador ya no aparece en todas las páginas:** por defecto no está en ninguna, y pide permiso sitio por sitio.

- Cambiar de idioma reinicia Kibo entero, con sus pestañas.

### Arreglado

- «Te espera» ya no se confunde con preguntas citadas en un mensaje ni con agentes que siguen trabajando de fondo.

- Las sesiones que todavía no tienen conversación guardada (por ejemplo, la de la Wiki) ya no se cierran solas al reabrir Kibo.

- La ventana ya no se traba al iniciar después de un cierre forzado.

### Seguridad

- Los nombres y textos que vienen de afuera se limpian y se escapan; política de seguridad de contenido (CSP) en la ventana.

- El servicio de sesiones escucha sólo en `127.0.0.1`, con un token nuevo en cada arranque, y sólo abre una lista cerrada de programas.

## 0.1.0 · 2026-10-20

Primera versión, para Windows 10 y 11: proyectos y sesiones de Claude Code con su conversación y su
consola; documentos y capturas con cada versión guardada; editor de imágenes; árbol de archivos con Monaco; cuadrícula de
sesiones; extensión «Kibo — señalar» para Chrome y Edge; tareas programadas; proyectos en servidores por SSH; el equipo de
agentes; y la Wiki de cada proyecto con su sesión «wiki» autónoma.
