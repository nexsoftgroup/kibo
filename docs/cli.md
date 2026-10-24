# Claude Code en Kibo

Kibo no es un agente de IA: es el lugar donde trabajan los tuyos. Cada sesión es **Claude Code de verdad**, corriendo en su consola, con tu cuenta y sus permisos de siempre.

> **Beta, probada al 100 % con Claude Code**
>
> Kibo está hecho y probado con Claude Code: Agent Hub, la conversación con la hora de cada mensaje, las consultas al costado, el historial y los avisos de «terminó / te espera» leen los archivos de sesión de Claude Code. La idea es que más adelante funcione con más agentes de IA.

<a name="sesion"></a>
## Antes de abrir sesiones: instalado y con tu sesión iniciada

Para abrir sesiones (y agentes, peers, Agent Hub o consultas) hace falta Claude Code **instalado y con tu sesión iniciada**. Sin eso puedes crear y abrir proyectos. Kibo te muestra un cuadro, **Antes de empezar** (también en el menú **Kibo → Plataformas de IA…**), con su estado: **no instalado**, **sin sesión** o **listo**, el comando oficial para instalarlo, con **Copiar**, y un botón para **iniciar sesión**, que abre una consola donde el login lo haces tú.

| Sistema | Comando oficial para instalar Claude Code |
|---|---|
| Windows | `irm https://claude.ai/install.ps1 \| iex` |
| Linux y macOS | `curl -fsSL https://claude.ai/install.sh \| bash` |

En Windows, Claude Code necesita **Git for Windows**. El comando de la terminal de Kibo instala los dos si lo autorizas. Más sobre Claude Code: [su documentación](https://docs.claude.com/claude-code).

**Kibo no lee ni toca tus credenciales:** sólo mira si Claude Code tiene una sesión iniciada.

## Con tu cuenta, bajo sus reglas

- Cada persona usa **su propia cuenta** de Claude Code y acepta los términos de Anthropic.
- Kibo **no incluye, no revende y no guarda** credenciales.
- Lo que Claude Code manda a Anthropic lo manda él, bajo su política de privacidad. Kibo no le agrega nada.

## Qué hace Kibo con Claude Code

- **Lee la conversación** del historial que Claude Code ya guarda en tu PC (`~/.claude/projects`) para mostrarla al costado, con la hora de cada mensaje. No la manda a ningún lado.
- **Arma tu equipo:** en Agent Hub, cada proyecto tiene una MAIN (una sesión de Claude Code) que reparte el trabajo entre los peers.
- **No suma permisos:** las sesiones corren con los permisos normales de Claude Code. Kibo no contesta por ti los pedidos de permiso ni el cartel «¿confías en esta carpeta?»: los marca como «te necesita».
- **Consultas al costado** (💬 y «¿Para qué es esto?») corren sin herramientas: el modelo sólo contesta, no toca archivos.

---

[← Primeros pasos](primeros-pasos.md)[Windows, Linux y macOS →](plataformas.md)
