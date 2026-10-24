# Worktree por peer

*Desde la versión 1.0.2.*

Cuando varios peers trabajan a la vez en el mismo repositorio, pueden pisarse: uno cambia un archivo mientras otro lo
está editando. Con **worktree por peer**, cada peer nuevo trabaja en **su propia copia del repo y en su propia rama**,
y tú decides cuándo su trabajo vuelve a la rama principal.

## Cómo se prende

En la lista de proyectos, abre el menú **⋯** del proyecto (o haz clic derecho) y toca
**Worktree por peer: activar**. Para apagarlo, el mismo menú: **Worktree por peer: apagar**.

- Viene **apagado** en todos los proyectos.
- Sólo se puede prender si la carpeta del proyecto es la **raíz de un repositorio de git** y está en una rama. Si no,
  la opción aparece deshabilitada y te dice por qué.
- Se decide **por proyecto**: puedes tenerlo prendido en uno y apagado en otro.

## Dónde trabaja cada peer

Con la opción prendida, cada peer nuevo, lo cree la MAIN o lo crees tú desde Agent Hub:

- trabaja en `<carpeta padre>/<proyecto>.kibo-worktrees/<peer>`;
- en la rama `kibo/<peer>`, que sale de la rama en la que está el proyecto (la «base»);
- commitea en su rama, sin tocar la carpeta principal.

La **MAIN sigue en la carpeta principal**. Si quieres que un peer en particular trabaje ahí, la MAIN lo crea con
`peers crear <nombre> --principal`. En `peers lista`, los peers con worktree aparecen marcados con su rama.

## Integrar el trabajo de un peer

**Lo decides tú, nunca la MAIN.** En el menú ⋯ del proyecto aparece
**Integrar «peer» → base (N commits)…**, y Kibo te pide confirmar.

1. El worktree del peer tiene que estar **limpio**: lo que no está commiteado no se integra.
2. Kibo pone la rama del peer **al día con la base** (rebase). Si hay un conflicto, **no toca nada** y te avisa: no
   queda nada a medias.
3. Después la suma a la base **sin merge commit** (fast-forward), así la historia queda lineal.

Si el peer sigue vivo, continúa trabajando en su worktree, ya al día con la base.

## Quitar el worktree de un peer

- Al integrar, si quedó **todo integrado y el peer está cerrado**, su worktree y su rama se quitan solos.
- También puedes quitarlo a mano: **Quitar el worktree de «peer»…** en el menú ⋯. Si está limpio e integrado, se quita
  sin preguntar. Si queda trabajo sin integrar, te dice **cuántos commits y archivos se perderían** y tienes que
  confirmar con **Quitar igual**.
- Con el peer **vivo** no se quita.
- Apagar la opción no borra los worktrees que ya existen.

---

Ver también: [Agent Hub y la MAIN](funciones.md#agent-hub-tus-equipos-de-agentes) ·
[Todo lo que hace Kibo](funciones.md)
