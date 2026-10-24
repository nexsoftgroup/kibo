# Windows, Linux y macOS

Qué funciona en cada sistema, dicho sin adornos. Estado a la versión 1.0.1 (24/10/2026).

| Sistema | Estado | Cómo se probó |
|---|---|---|
| **Windows 10 / 11** | soportado | Uso diario y pruebas de pantalla y del motor en Windows 11. |
| **Linux** | probado | Ubuntu 24.04, probado dentro de WSL con su ventana real: la app instalada con `install.sh` (y en Docker). |
| **macOS** | experimental | Código escrito; sin prueba en una Mac de verdad ni corrida de las pruebas automáticas en Mac. |

## Qué cambia según el sistema

|  | Windows | Linux | macOS |
|---|---|---|---|
| Ventana | WebView2 | GTK + WebKit2GTK (o Qt) | WebKit nativo |
| Barra de menús | Reemplaza la barra de título (sigue andando Snap, Win+flechas, Alt+F4) | Marco del sistema y la barra de Kibo debajo | En la barra de menús del sistema |
| Tareas programadas | Programador de tareas (carpeta `\Kibo\`) | Timer de systemd de usuario, o `cron` | `launchd` |
| Avisos de escritorio | Notificación del sistema; tocarla abre la sesión | `notify-send` | Notificaciones del sistema; tocarla no abre la sesión |
| Consola del sistema | PowerShell | La consola del sistema (`zsh` o `bash`) |  |
| Atajos | Ctrl | Ctrl | ⌘ |

## Diferencias conocidas

- **Linux en WSL:** no hay ícono junto al reloj (WSLg no tiene bandeja). Kibo lo detecta y lo maneja.
- **Linux, captura de pantalla:** necesita una herramienta de captura del sistema; si falta, Kibo dice qué instalar.
- **macOS:** todo lo anterior está escrito pero sin probar en una Mac.

## Reportar un problema de un sistema

Manda: la versión (primera línea del menú **Kibo**), el sistema y su versión, qué hiciste y qué esperabas. No mandes conversaciones ni archivos de tus proyectos.

---

[← Claude Code](cli.md)[Actualizar →](actualizar.md)
