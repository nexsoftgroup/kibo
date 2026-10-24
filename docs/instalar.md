# Instalar Kibo

En **Windows**, con un comando en la terminal (recomendado) o con el instalador. En **Linux y macOS**, con otro comando en la terminal.

> **Antes de empezar**
>
> En cualquier sistema necesitas **Claude Code instalado y con tu sesión iniciada**. Sin eso puedes crear y abrir proyectos, pero no sesiones. Kibo te guía: te muestra su estado, el comando oficial para instalarlo y un botón para iniciar sesión, donde el login lo haces tú. **Kibo no lee tus credenciales.** El comando de la terminal instala Claude Code si lo autorizas; el login lo haces tú al abrir Kibo. [Más sobre Claude Code en Kibo](cli.md).

<a name="windows-terminal"></a>
## Windows: desde la terminal (recomendado)

Abre **PowerShell** (tecla Windows, escribe «PowerShell» y Enter), pega esto y presiona Enter:

```
irm https://kibo.nexsoftgroup.com/install.ps1 | iex
```

1. **Revisa lo que necesita Claude Code:** Git for Windows y el propio Claude Code. **Por cada cosa que falta** te dice qué es y para qué, te avisa que al instalarlo se acepta en tu nombre su licencia (con el enlace para leerla) y pregunta «¿Autorizas que lo instale ahora? (s/n)». Lo instala con `winget` o con el instalador oficial de cada empresa; para Git, Windows puede pedirte permiso de administrador.
2. **Si contestas que no, la instalación se cancela** y Kibo no se instala. Lo que ya se había instalado queda. Puedes instalar eso tú y volver a correr el comando.
3. **Baja el instalador de Kibo** de kibo.nexsoftgroup.com, **comprueba su SHA-256** contra el publicado y, si no coincide, no lo abre. Si coincide, lo abre con sus pantallas de siempre: la bienvenida, los [Términos de uso](https://kibo.nexsoftgroup.com/terminos) y, si ya tenías Kibo, **Actualizar**. Por este camino no aparece el aviso «Windows protegió tu PC».
4. **Al terminar** te recuerda que, al abrir Kibo, te guía para iniciar sesión en tu IA. El login lo haces tú, en la herramienta de cada empresa.

Habla en español, inglés o portugués según el idioma de Windows, y **no manda nada a ningún lado**: sólo descarga. Funciona con Windows PowerShell 5.1 (el que viene con Windows) y con PowerShell 7.

<a name="windows-exe"></a>
## Windows: con el instalador (doble clic)

Si prefieres no usar la terminal. Por este camino, Git for Windows y Claude Code los instalas tú; Kibo te guía en **Antes de empezar**.

1. Descarga el instalador `Kibo-<versión>-Setup.exe` de la [última versión en Releases](https://github.com/nexsoftgroup/kibo/releases/latest).
2. **Comprueba el SHA-256** (opcional, recomendado). En PowerShell, en la carpeta de descargas:
   ```
   Get-FileHash .\Kibo-<versión>-Setup.exe -Algorithm SHA256
   ```
   Tiene que dar exactamente el SHA-256 publicado en ese Release (en sus notas y en `SHA256SUMS.txt`). Si no coincide, no lo abras. [Más sobre la verificación](https://kibo.nexsoftgroup.com/seguridad#verificar).
3. Ábrelo. Windows va a mostrar **«Windows protegió tu PC»**: toca **Más información → Ejecutar de todas formas**. Pasa porque Kibo todavía no tiene firma de código de Microsoft. [Por qué](preguntas.md#smartscreen).
4. Sigue el asistente. Se instala **para tu usuario, sin pedir permisos de administrador**.

| Qué | Dónde queda (con los dos caminos) |
|---|---|
| El programa | `%LOCALAPPDATA%\Programs\Kibo` |
| Tus datos (configuración, conversaciones, adjuntos) | `%LOCALAPPDATA%\Kibo` |

**Requisitos:** Windows 10 u 11 de 64 bits · WebView2 (viene con Windows; si falta, el instalador lo baja) · **Git for Windows** (Claude Code lo necesita en Windows) · Claude Code con tu sesión iniciada. No hace falta Python: el instalador lo trae adentro. Con el comando de la terminal, lo que falte se instala si lo autorizas.

<a name="linux"></a>
## Linux: desde la terminal

Abre una terminal, pega esto y presiona Enter:

```
curl -fsSL https://kibo.nexsoftgroup.com/install.sh | sh
```

1. **Revisa Python 3.11 o más nuevo.** Si falta, te dice cómo instalarlo con el gestor de paquetes de tu sistema y se cancela.
2. **Revisa lo que necesita la ventana** (GTK, WebKit2GTK y PyGObject). Si falta algo, te muestra el comando para `apt`, `dnf`, `pacman` o `zypper` y se cancela; con `--dependencias` te pide permiso y lo instala él, con `sudo` (puede pedirte tu contraseña).
3. **Revisa Claude Code.** Si falta, te dice qué es y para qué, te avisa de su licencia (con el enlace para leerla) y pregunta si autorizas que lo instale. Todo va para tu usuario, sin `sudo`. **Si contestas que no, la instalación se cancela** y Kibo no se instala.
4. **Baja el paquete de Kibo** de kibo.nexsoftgroup.com y **comprueba su SHA-256** contra el publicado; si no coincide, no lo instala.
5. **Lo instala en `~/Kibo/kibo`** (tus proyectos van en `~/Kibo`), con un entorno de Python propio (`.venv`), el comando `kibo` en `~/.local/bin` y el acceso en el menú de aplicaciones.
6. **Al terminar** te recuerda que, al abrir Kibo, te guía para iniciar sesión en tu IA.

Habla en español, inglés o portugués según el idioma del sistema, y no manda nada a ningún lado: sólo descarga. **Correrlo de nuevo actualiza:** reemplaza sólo el programa y conserva tus datos.

Con opciones, se agregan después de `sh -s --`:

```
curl -fsSL https://kibo.nexsoftgroup.com/install.sh | sh -s -- --qt
```

| Opción | Qué hace |
|---|---|
| `--qt` | La ventana con Qt (PyQt6 por pip, unos 200 MB) en vez de GTK del sistema |
| `--dependencias` | Instala con `sudo`, con tu permiso, los paquetes del sistema que falten (si no, sólo te dice el comando) |
| `--destino <carpeta>` | Dónde instalar (por defecto `~/Kibo/kibo`) |
| `--sin-accesos` | No crea el comando `kibo` ni el acceso del menú |

Probado en Ubuntu 24.04 dentro de WSL (22 casos, 22/10).

<a name="macos"></a>
## macOS experimental

> **Todavía no se probó en una Mac de verdad**
>
> El código para macOS está escrito (ventana nativa con WebKit, menús del sistema, tareas con launchd, ⌘ en los atajos), pero no corrió en una Mac ni en las pruebas automáticas. Tampoco el instalador. Úsalo sabiendo que puede fallar.

Es el mismo comando que en Linux, con las mismas preguntas. Abre **Terminal** y pega:

```
curl -fsSL https://kibo.nexsoftgroup.com/install.sh | sh
```

Necesita Python 3.11 o más nuevo (si falta, te sugiere `brew install python@3.13` o python.org). Si tienes Homebrew, Node.js se instala con él. Deja el comando `kibo` en `~/.local/bin` y la app en `~/Applications/Kibo.app`.

<a name="abrir"></a>
## Abrirlo

Con el acceso directo **Kibo** o escribiendo `kibo` en una consola nueva. Si ya estaba abierto, trae su ventana. También puede arrancar solo, escondido junto al reloj: **⚙ Configuración → arranque con el sistema** (⚙ Configuración se abre desde el menú **Ajustes**).

**Para comprobar que quedó bien:** la primera línea del menú **Kibo** dice la versión, por ejemplo «Kibo 1.0.2».

<a name="extension"></a>
## La extensión del navegador (opcional)

Para señalar cosas de una página web y mandárselas a una sesión, en Chrome o Edge. En Kibo, el botón **Navegador** te guía:

1. abre `chrome://extensions` o `edge://extensions`;
2. activa el **Modo de desarrollador**;
3. **Cargar descomprimida** → la carpeta `app/extension` de tu instalación.

La extensión no hace nada hasta que la activas en una página, y pide permiso sitio por sitio.

---

[← Inicio de la documentación](README.md)[Primeros pasos →](primeros-pasos.md)
