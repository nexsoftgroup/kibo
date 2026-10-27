# Preguntas frecuentes

<a name="smartscreen"></a>
## «Windows protegió tu PC». ¿Es un virus?

Ese aviso es de **SmartScreen**, de Windows. Aparece con programas bajados de internet que **no tienen firma de código** o que todavía tienen **poca reputación** (pocas descargas registradas por Microsoft). Kibo está en los dos casos: es nuevo y **todavía no tiene firma de código de Microsoft**. El aviso no significa que Windows haya encontrado algo malo en el archivo.

**Con el comando de la terminal no aparece:** `irm https://github.com/nexsoftgroup/kibo/releases/latest/download/install.ps1 | iex` baja el instalador de GitHub, comprueba la firma de NexSoft y el SHA-256 y lo abre. [Ver cómo](instalar.md#windows-terminal).

Si prefieres el instalador con doble clic y quieres seguir:

1. antes, [comprueba el SHA-256](https://kibo.nexsoftgroup.com/seguridad#verificar) del archivo contra el de nuestra página de descarga;
2. en el aviso, toca **Más información**;
3. toca **Ejecutar de todas formas**.

Si el SHA-256 no coincide, no lo abras y descárgalo de nuevo desde nuestra página.

<details>
<summary>Mi Windows no me deja seguir: no aparece «Ejecutar de todas formas»</summary>

Puede ser **Control inteligente de aplicaciones** (Smart App Control, en Windows 11). A diferencia de SmartScreen, bloquea los programas sin firma y no ofrece una forma de saltarlo para una sola app. **Si tu PC tiene Smart App Control activo, Windows no deja abrir el instalador hasta que esté firmado (estamos en eso)**, tampoco con el comando de la terminal: el comando evita el aviso de SmartScreen, no este. Viene apagado en la mayoría de las PCs. También puede ser un antivirus o una política de tu empresa.

No te vamos a pedir que apagues una protección de tu equipo. Mientras Kibo no tenga firma, en un equipo con esa protección activa hay que esperar la versión firmada. En una PC de empresa, habla con quien la administra.

</details>

## ¿Kibo es gratis? ¿Tiene cuenta o suscripción?

**Sí, es gratis.** Es una herramienta que hicimos en [NexSoft](https://nexsoftgroup.com) y compartimos. No tiene servidor propio ni cuentas: no te registras en nada.

## ¿Necesito Claude Code?

Sí: Kibo está hecho para **Claude Code**, instalado y con tu sesión iniciada. Sin eso puedes crear y abrir proyectos, pero no sesiones. Kibo te muestra su estado, el comando oficial para instalarlo y un botón para iniciar sesión: el login lo haces tú, y Kibo no lee tus credenciales. Es una beta probada al 100 % con Claude Code; la idea es que más adelante funcione con más agentes de IA. [Más sobre Claude Code en Kibo](cli.md).

## ¿Kibo manda mis conversaciones a algún lado?

No. Kibo lee la conversación del historial que Claude Code ya guarda en tu PC, para mostrártela. No tiene telemetría ni respaldo en la nube. Lo que el CLI manda a su proveedor lo manda el CLI, como si lo usaras sin Kibo. [Ver privacidad](https://kibo.nexsoftgroup.com/privacidad).

## ¿Cómo me entero de una versión nueva?

Kibo te avisa solo: al abrirse y cada 6 horas se fija en GitHub (o, de respaldo, en `kibo.nexsoftgroup.com`) si hay una versión nueva y, si la hay, te muestra «Hay una versión nueva de Kibo: X». Tocándolo, **Actualizar ahora**. Se actualiza encima, sin desinstalar, y tus datos se conservan. [Ver cómo se actualiza](actualizar.md).

## ¿Necesito Git?

Kibo no. Pero **Claude Code en Windows** sí lo necesita: si lo vas a usar, instala [Git for Windows](https://git-scm.com/download/win).

## ¿Si cierro Kibo, se cortan las sesiones?

No, si eliges **Salir de Kibo (las sesiones siguen)**. Las consolas viven en un servicio aparte; al volver, cada pestaña se reengancha y muestra lo que pasó mientras tanto. **Cerrar todo** sí las cierra.

## ¿Kibo aprueba permisos por mí?

No. Ni los pedidos de permiso de los agentes ni el cartel «¿confías en esta carpeta?» de Claude Code. Cuando un agente te necesita, Kibo te lo marca y la decisión es tuya. La MAIN de Agent Hub tampoco puede aprobar permisos de otros.

## ¿Funciona en Mac?

Es **experimental**: el código está escrito, pero todavía no se probó en una Mac de verdad. [Ver el estado por sistema](plataformas.md).

## ¿Dónde quedan mis datos?

En tu PC. Con `install.sh` (Linux y macOS) o instalando desde el código, dentro de la instalación: `~/Kibo/kibo` (en Windows, `%USERPROFILE%\Kibo\kibo`): `config.json`, `Conversaciones/`, `Adjuntos/`, `programadas.json`, `logs/`. Los adjuntos de cada proyecto van en `<proyecto>/Adjuntos/`. Con el instalador de Windows (también si usaste el comando de la terminal), en `%LOCALAPPDATA%\Kibo`.

## ¿Cómo reporto un error?

Manda la versión (primera línea del menú **Kibo**), tu sistema, qué CLI usas, qué hiciste y qué pasó. No mandes conversaciones, credenciales ni archivos de tus proyectos.

---

[← Desinstalar](desinstalar.md)
