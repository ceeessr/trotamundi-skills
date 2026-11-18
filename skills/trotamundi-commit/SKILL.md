---
name: trotamundi-commit
description: Reglas de commit en Trotamundi. Usar en cada git commit o push de código. Un commit por paso lógico, bitácora en la rama sesiones y foto del estado en Obsidian.
---

# Commit

## Antes
- Un commit por paso lógico. Compila y corre las pruebas que tocan.
- Agrega los archivos por nombre. Con `git add -A` entran logs de errores (`hs_err_*.log`) y basura.
- Después de `git mv`, revisa `git status`: si no, el commit lleva solo los renombres.
- En PowerShell, pasa el mensaje con `git commit -F archivo.txt`, no con here-strings en la misma línea.

## Después (en la misma respuesta)
1. **Bitácora:** una línea en tu archivo de la rama `sesiones` con el hash y qué cambió. La historia vive solo ahí.
2. **Obsidian:** en `ESTADO_ACTUAL.md` cambia solo la fila de tu rama (sin agregar historia). Actualiza la nota de
   la tarea si existe, y `DECISIONES`/`PENDIENTES` si cambiaron.
3. Dile al usuario qué probar y espera su confirmación.

Los commits de la rama `sesiones` no piden tocar Obsidian.

## Al cerrar la sesión
Reescribe `RELEVO_ACTUAL.md` (qué hiciste, qué falta, qué aprendiste) para el siguiente Claude.
