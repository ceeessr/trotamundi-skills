# Trotamundi · skills para Claude Code

**Trotamundi** es una app para correr y entrenar: plan de carrera y gimnasio, grabación con GPS, ruta en 3D,
amigos con chat y citas para salir a correr, Strava y Garmin, y Antonino, el búho que te acompaña en cada escena.

> 🏃 **Próximamente en Google Play y en la App Store.**

Aquí están las skills con las que trabajo con Claude Code mientras la construyo: cómo me gusta que me expliquen,
cómo se reparten varias terminales y chats en la nube, cómo se compila en una PC con poca RAM y cómo se cuidan
los datos. Las comparto por si te sirven para tu propio proyecto.

## Skills

| Skill | Para qué |
|---|---|
| [`trotamundi-forma-de-trabajo`](skills/trotamundi-forma-de-trabajo/SKILL.md) | Español, respuestas cortas, un paso a la vez, explicar cada cambio, maqueta antes de lo visual. |
| [`trotamundi-sesiones`](skills/trotamundi-sesiones/SKILL.md) | Varias sesiones de Claude (PC y nube) coordinadas con una rama `sesiones` en GitHub. |
| [`trotamundi-commit`](skills/trotamundi-commit/SKILL.md) | Un commit por paso lógico, bitácora en GitHub y foto del estado en Obsidian. |
| [`trotamundi-gradle`](skills/trotamundi-gradle/SKILL.md) | Turnos de Gradle entre terminales, compilar por lotes y no instalar mientras se graba. |
| [`trotamundi-datos-seguros`](skills/trotamundi-datos-seguros/SKILL.md) | Nada de SQL de escritura sin permiso, migraciones aditivas, secretos fuera de Git. |
| [`trotamundi-celular`](skills/trotamundi-celular/SKILL.md) | Conectar el celular por adb: USB, Wi-Fi local o a distancia. |

## Cómo usarlas

Copia la carpeta de la skill que quieras a `.claude/skills/` de tu proyecto (o a `~/.claude/skills/` para todos)
y ajusta rutas y nombres a tu caso.

## Autor

César Salazar Moncayo · [@ceeessr](https://github.com/ceeessr)
