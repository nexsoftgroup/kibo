<p align="center">
  <img src="img/kibo.png" alt="Kibo" width="96">
</p>

<h1 align="center">Kibo</h1>

<p align="center">
  <b>Muchos agentes de IA. Un solo lugar.</b><br>
  Tus agentes de Claude Code trabajando a la vez, como un equipo, con su consola, sus archivos y sus tareas a la vista.
</p>

<p align="center">
  <a href="https://github.com/nexsoftgroup/kibo/releases/latest/download/Kibo-Setup.exe"><img src="https://img.shields.io/badge/Descargar_para_Windows-%C3%BAltima_versi%C3%B3n_%28.exe%29-3346e0?style=for-the-badge" alt="Descargar la última versión de Kibo para Windows (.exe)"></a>
  <a href="https://kibo.nexsoftgroup.com"><img src="https://img.shields.io/badge/Sitio_web-kibo.nexsoftgroup.com-0f2340?style=for-the-badge" alt="Sitio web: kibo.nexsoftgroup.com"></a>
</p>

<p align="center">
  <a href="https://github.com/nexsoftgroup/kibo/releases/latest"><b>Descargar</b></a> ·
  <a href="docs/README.md">Documentación</a> ·
  <a href="https://github.com/nexsoftgroup/kibo/releases">Versiones y novedades</a> ·
  <a href="https://github.com/nexsoftgroup/kibo/issues/new/choose">Reportar un problema o proponer una idea</a>
</p>

<p align="center">
  Gratis · 100 % local · Sin telemetría · No lee tus credenciales · Beta
</p>

<p align="center">
  <b>Español</b> · <a href="README.en.md">English</a> · <a href="README.pt-BR.md">Português (Brasil)</a>
</p>

![Kibo con cuatro sesiones de Claude Code trabajando a la vez, y la tarjeta de un equipo de Agent Hub](img/portada.png)

> **Este repositorio es la casa pública de Kibo:** un resumen, las novedades y el lugar para dejar tus comentarios.
> La **[documentación completa](docs/README.md)**, con todas las capturas, está en este repo, y cada versión con sus novedades, en **[Releases](https://github.com/nexsoftgroup/kibo/releases)**.
> El código fuente no se publica acá.

---

## Qué es Kibo

Los agentes de IA ya escriben código, investigan y documentan. Lo difícil es coordinarlos. Kibo es una app de
escritorio que convierte sesiones sueltas de **Claude Code** en **un equipo que trabaja junto**, a la vista y en tu PC.

- **Un equipo, no pestañas sueltas.** Cada proyecto tiene su MAIN, que reparte el trabajo entre los agentes y te
  contesta corto. Tú le hablas al equipo; no tienes que ir sesión por sesión.
- **Muchos agentes, a la vista.** Mientras uno escribe el código, otro corre las pruebas y otro documenta. Ves si cada
  uno trabaja, te espera o pide permiso.
- **Nada se pierde.** Cada conversación, captura y decisión queda en tu PC, y una Wiki que se escribe sola hace que el
  próximo agente empiece sabiendo lo que el anterior averiguó.

## Lo que hace

### Agent Hub: tus equipos de agentes, de un vistazo

![Agent Hub: una tarjeta por equipo, el mapa de equipos y el chat del equipo](img/agent-hub.png)

- **Una tarjeta por equipo:** cada proyecto con su MAIN, sus agentes y cuántos trabajan o te esperan.
- **El chat del equipo:** le hablas a todos, a un agente o a varios equipos, con **Ordenar** o **Consultar**.
- **Los permisos los sigues aprobando tú.**

### Muchos agentes, todos a la vez

![Una cuadrícula de 2 × 2 con cuatro sesiones de Claude Code a la vez](img/cuadricula.png)

- Varias sesiones de Claude Code en la misma pantalla, cada una en lo suyo.
- Divides el área como la necesites (2 columnas, 2 filas, 2 × 2, 3 × 2) o arrastras una pestaña a un borde.
- Cada sesión es Claude Code de verdad, con tu cuenta y sus permisos de siempre.

### La historia de la conversación y una Wiki que se escribe sola

![La conversación de la sesión, cada mensaje con su hora, al costado de su consola](img/conversacion.png)

- **Vuelves a lo hablado por fecha** («lo que hablamos ayer entre las 14 y las 18») y el agente se pone en contexto.
- **Una Wiki por proyecto**, en Markdown: lo que los agentes averiguan queda en notas, separando lo confirmado de lo
  que falta verificar. Se lee en Kibo, en cualquier editor o en Obsidian.
- **Ctrl+K** busca en proyectos, agentes, tareas y en todo lo que se habló.

### Tareas programadas: trabaja aunque no estés

![El panel de tareas programadas y el formulario para programar una](img/tareas.png)

- A la hora que digas, Kibo abre la sesión y **le escribe la instrucción**, como si la escribieras tú.
- Con Kibo cerrado corre igual: programador de tareas de Windows, systemd o cron en Linux, y launchd en macOS.

### Y además

| | |
|---|---|
| **Señala en la web** | Con la extensión para Chrome y Edge marcas un elemento o un área, y a la sesión le llega la captura, el HTML y los errores de la consola. |
| **Capturas al instante** | Pegas o arrastras una captura, la marcas con flechas y recuadros, y le llega al agente. |
| **Editor y VS Code** | Los archivos con el editor de VS Code, y VS Code completo en una pestaña si lo quieres. |
| **Atajos para todo** | En su propia ventana (Ctrl+Alt+S), con buscador. |
| **Servidores por SSH** | Sesiones que corren en otra máquina. Sólo con llave SSH: las contraseñas no se guardan. |
| **Temas e idiomas** | Kibo, Oscuro y Claro. En español, inglés y portugués (Brasil). |
| **Avisos de escritorio** | Opcionales: cuando un agente termina o te necesita. |

👉 **[Todas las funciones, con capturas](docs/funciones.md)**

## Instalar

Kibo se instala para tu usuario, dentro de tu perfil. El instalador de doble clic se baja de
[Releases](https://github.com/nexsoftgroup/kibo/releases/latest), y los comandos de la terminal, de kibo.nexsoftgroup.com.

### Windows

**Recomendado: desde la terminal, en una línea.** Abre PowerShell (tecla Windows, escribe «PowerShell» y Enter), pega
esto y presiona Enter:

```powershell
irm https://kibo.nexsoftgroup.com/install.ps1 | iex
```

**Qué va a pasar:** te pregunta con qué IA vas a trabajar, te pide permiso antes de instalar cada cosa que falte, baja
Kibo del sitio, **comprueba que es el nuestro (SHA-256)** y abre su instalador. Así no aparece el aviso de Windows. El
instalador te muestra los [Términos de uso](https://kibo.nexsoftgroup.com/terminos) antes de instalar.
[Paso a paso](docs/instalar.md).

**¿Prefieres el instalador con doble clic?**

[![Descargar la última versión de Kibo para Windows (.exe)](https://img.shields.io/badge/Descargar-Kibo--Setup.exe_%28%C3%BAltima_versi%C3%B3n%29-3346e0?style=for-the-badge)](https://github.com/nexsoftgroup/kibo/releases/latest/download/Kibo-Setup.exe)

Baja siempre la última versión. Su número, sus novedades y su SHA-256 están en [Releases](https://github.com/nexsoftgroup/kibo/releases/latest). Windows va a mostrar un aviso porque
todavía no está firmado: **Más información → Ejecutar de todas formas**.
[Por qué pasa](docs/preguntas.md#smartscreen) ·
[Cómo comprobar el SHA-256](https://kibo.nexsoftgroup.com/seguridad#verificar) (el comando de la terminal lo hace solo).

### Linux y macOS

Abre una terminal, pega esto y presiona Enter:

```sh
curl -fsSL https://kibo.nexsoftgroup.com/install.sh | sh
```

Hace las mismas preguntas, baja Kibo del sitio, comprueba su SHA-256 y lo instala para tu usuario en `~/Kibo/kibo`,
sin `sudo`. En macOS es **experimental**: el código está escrito, pero todavía no se probó en una Mac de verdad. Si lo
pruebas, nos sirve saber qué pasó.

### Qué necesitas

| Sistema | Estado | Necesita |
|---|---|---|
| **Windows 10 / 11** (64 bits) | Soportado | WebView2 (viene con Windows; si falta, el instalador lo baja), Git for Windows (lo necesita Claude Code) y Claude Code. No hace falta Python: el instalador lo trae. El comando de la terminal instala lo que falte, si lo autorizas. |
| **Linux** | Probado en Ubuntu 24.04 (WSL) | Python 3.11+, GTK, WebKit2GTK y PyGObject del sistema (o Qt con `--qt`) y Claude Code. El comando de la terminal instala Claude Code, si lo autorizas. |
| **macOS** | Experimental | Python 3.11+ y Claude Code. El comando de la terminal instala Claude Code, si lo autorizas. |

**Claude Code**, instalado y con **tu propia sesión iniciada**. Sin eso puedes crear y abrir proyectos, pero no
sesiones: Kibo te muestra su estado, el comando oficial para instalarlo y un botón para iniciar sesión, donde el login
lo haces tú. Kibo no lo incluye ni lo revende, y no lee tus credenciales.
[Más sobre Claude Code en Kibo](docs/cli.md).

> **Beta: pruébalo con Claude Code.** Kibo está hecho y probado al 100 % con Claude Code. La idea es que más adelante
> funcione con más agentes de IA.

## Privacidad

Kibo no tiene servidor propio, cuentas, telemetría ni respaldo en la nube, y no lee tus credenciales. Las
conversaciones, los adjuntos y la configuración quedan en tu PC. Lo que sale a internet es lo que Claude Code ya manda a
Anthropic, y lo que tú actives (buscar versiones nuevas, bajar VS Code).

[Política de privacidad](https://kibo.nexsoftgroup.com/privacidad) ·
[Seguridad y verificación](https://kibo.nexsoftgroup.com/seguridad) ·
[Términos de uso](https://kibo.nexsoftgroup.com/terminos)

## Comentarios, problemas e ideas

Kibo está en beta y tus comentarios nos sirven muchísimo.

- **¿Algo no funciona?** [Reporta un problema](https://github.com/nexsoftgroup/kibo/issues/new?template=problema.yml).
  Cuéntanos tu versión de Kibo, tu sistema y los pasos para que pase.
- **¿Se te ocurre algo?** [Propón una idea](https://github.com/nexsoftgroup/kibo/issues/new?template=idea.yml).
- **¿Una pregunta?** Mira primero las [preguntas frecuentes](docs/preguntas.md).

Antes de pegar registros o capturas, revisa que no tengan contraseñas, tokens ni datos de clientes.

---

<p align="center">
  Kibo es una herramienta que hicimos en <a href="https://nexsoftgroup.com"><b>NexSoft</b></a> y compartimos gratis.<br>
  <sub>Claude Code es una marca de Anthropic. Kibo no es un producto de Anthropic.</sub>
</p>
