---
name: trotamundi-sesiones
description: Coordinar varias sesiones de Claude Code (terminales en la PC y chats en la nube) con una rama `sesiones` en GitHub. Usar al empezar cada sesión, antes de editar, compilar, hacer commit/push/merge o asignar trabajo a otra sesión, y cuando el usuario escribe «lees» o «lee sesiones».
---

# Sesiones

Varias sesiones trabajan a la vez en el mismo repo. Se coordinan con archivos en la rama `sesiones`.

## Al empezar (primer paso, siempre)
1. `git fetch origin sesiones` y lee los archivos activos: su «No tocar», sus avisos y sus turnos de Gradle.
2. Crea tu archivo `sesiones/AAAA-MM-DD_HHMM_<nombre>.md` con tipo (terminal/nube), cuenta y cuántas sesiones
   había activas. Súbelo.

## Mientras trabajas
- Anota en tu archivo cada commit (hash y qué cambió), cada compilación y cada encargo.
- Escribe siempre al final del archivo.
- Declara «No tocar (mío): …» con los archivos o worktrees que estás usando.
- Si otro ya está haciendo algo, súmate a lo suyo; no lo dupliques.
- Si dos sesiones comparten el worktree de `sesiones`, usa uno propio desacoplado y haz `push HEAD:sesiones`.
  Un `git commit -a` se lleva el archivo sin commit del otro.

## Cada sesión, su rama y su carpeta
- La nube trabaja en una rama nueva y hace push solo ahí. En la PC, cada terminal en su worktree.
- Nadie hace merge ni push a `main` sin que el dueño lo pida.

## «lees» / «lee sesiones»
Deja lo que haces en un punto seguro, haz pull de `sesiones`, lee lo activo («PIDO» con tu nombre, avisos,
turnos) y actúa sobre lo que te toca. Anótalo.

## Asignar a otra sesión o a la nube
- Antes: lee las sesiones activas y revisa `git status` de los worktrees. Si alguien toca los mismos archivos,
  cambia la tarea o coordina.
- El prompt va completo y listo para copiar: contexto, rama, qué NO tocar y por qué, cómo verificar.
- La nube no ve archivos locales ni llaves: el prompt trae todo lo necesario.
- Termina pidiendo: «Al final, dame un bloque de código listo para copiar con: rama, hashes, qué cambió, pruebas
  corridas con números exactos, qué falta y qué no se probó».
