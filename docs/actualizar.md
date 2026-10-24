# Actualizar Kibo

Kibo te avisa cuando hay una versión nueva y se actualiza encima de la que tienes: **no hace falta desinstalar**, y tus proyectos, conversaciones y configuración se conservan.

## Qué versión tienes

La primera línea del menú **Kibo** dice qué versión tienes, por ejemplo «Kibo 1.0.0». También está en **⚙ Configuración → Versión**.

## Cómo se actualiza

1. **Kibo se fija si hay una versión nueva** en `kibo.nexsoftgroup.com`, al abrirse y cada 6 horas. El sitio publica cuál es la última versión: su número, su fecha, sus novedades y la huella SHA-256 de su instalador. Se apaga en **⚙ Configuración**.
2. **Si hay una nueva, te avisa:** «Hay una versión nueva de Kibo: X», con **Leer más** (sus [novedades](https://github.com/nexsoftgroup/kibo/releases)) y **No avisarme de esta**. Tocando el aviso, o en **Kibo → Buscar versión nueva…**, está **Actualizar ahora**.
3. **Actualizar ahora** descarga el instalador nuevo desde `kibo.nexsoftgroup.com`, comprueba con su SHA-256 que no esté alterado y lo abre.
4. **El instalador ve que Kibo ya está instalado** y te lo dice: «Kibo 1.0.0 está instalado en esta PC. Se va a actualizar a la 1.1.0; tus proyectos, conversaciones y configuración se conservan». El botón dice **Actualizar**.

> **Antes de actualizar, el instalador cierra Kibo y sus sesiones**
>
> Si algún agente está trabajando, espera a que termine. Al abrir Kibo de nuevo, vuelven tus proyectos y pestañas, y las conversaciones de Claude se pueden retomar donde quedaron.
>
> Que las sesiones sigan trabajando mientras Kibo se reinicia vale para **⟳ Reiniciar** o para cerrar la ventana, no para actualizar.

## Actualizar a mano

Descarga el instalador desde [kibo.nexsoftgroup.com](https://kibo.nexsoftgroup.com/#descargar) y ábrelo: detecta la versión que tienes y la actualiza. Tampoco hace falta desinstalar antes.

## Linux y macOS

Por ahora, descarga el paquete desde [kibo.nexsoftgroup.com](https://kibo.nexsoftgroup.com/#descargar) y ejecuta `install.sh`. Para actualizar, lo mismo: se instala encima y tus datos se conservan.

## Lo que nunca hace

- No te pide usuario ni contraseña, y no manda datos tuyos: ni siquiera la versión que tienes. Sólo pide cuál es la última.
- No se actualiza sin que tú toques **Actualizar ahora**.
- No abre un instalador cuya huella SHA-256 no coincida con la publicada.

---

[← Windows, Linux y macOS](plataformas.md)[Desinstalar →](desinstalar.md)
