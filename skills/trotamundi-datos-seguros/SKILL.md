---
name: trotamundi-datos-seguros
description: Reglas para tocar datos en Trotamundi (Room, Supabase, Google Sheets) y secretos. Usar antes de cambiar esquemas, migraciones, SQL, políticas RLS o cualquier dato real.
---

# Datos seguros

La app ya tiene datos reales en el celular y en la nube.

## Base de datos
- Nunca SQL de escritura, migraciones ni cambios de datos reales sin permiso expreso. Primero muestra el SQL y
  una vista previa.
- Nunca borrar datos ni usar `fallbackToDestructiveMigration`. Cambios de esquema: migración versionada,
  aditiva y probada.
- Antes de tocar estructuras: revisa esquema, constraints, RLS, migraciones, DAOs y el flujo completo.
- La app no borra directo en las tablas: pasa por funciones que revisan quién pregunta.
- Guarda en el repo cada migración aplicada, con la fecha y quién la aplicó.
- Prueba con una cuenta de prueba, no con la cuenta principal.

## Secretos
- Nunca guardes ni imprimas tokens, contraseñas, llaves privadas ni secretos.
- `local.properties` y las llaves quedan fuera de Git. En CI van como secretos del repo.
- Un secreto pegado en un chat se cambia.
- Contactos, correos y datos de testers: solo en archivos locales ignorados por Git.
