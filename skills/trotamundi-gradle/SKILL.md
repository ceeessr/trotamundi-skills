---
name: trotamundi-gradle
description: Compilar e instalar Trotamundi en una PC con poca RAM y varias terminales. Usar antes de correr Gradle, compilar, correr pruebas o instalar en el celular.
---

# Gradle

La PC tiene poca RAM (≈10 GB). Dos Gradle a la vez la tumban.

## Turno
1. Revisa si hay otro Gradle: `Get-CimInstance Win32_Process -Filter "Name='java.exe'"` y el último aviso de
   cada archivo de sesiones.
2. Si hay otro, espera su «FIN». Nunca `gradlew --stop` ni dos Gradle a la vez.
3. Anota «**Gradle EMPIEZA <nombre>** (qué corres)» en tu archivo de sesiones; al acabar, «**Gradle FIN**».
4. No esperes a que haya RAM libre: compila reusando el daemon y avisa.

## Cómo compilar
- No compiles cada paso chico: una vez antes de instalar o antes de algo grande.
- Usa `--max-workers=1`. Si se cae por memoria o Metaspace, repite solo la tarea que falló.
- Fija `JAVA_HOME` al JBR de Android Studio si no está en el PATH.
- Para el código común (Kotlin Multiplatform) compila también el klib de iOS por separado.
- Los `build/` de muchos worktrees llenan el disco: pide permiso antes de borrarlos.

## Instalar
- Instala la variante de medición (release), no la de depuración: la depuración es lenta y engaña.
- Antes de instalar, revisa que el celular no esté grabando una salida: instalar corta la grabación.
- Después, di qué probar.
