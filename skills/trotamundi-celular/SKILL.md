---
name: trotamundi-celular
description: Conectar el celular Android por adb para instalar y ver la app. Usar cuando el usuario dice «modo USB», «Wi-Fi local», «a distancia», «en la escuela» o «en la calle», o manda una captura del código de vinculación.
---

# Celular

## Modos
- **USB:** `adb devices`. Si el cable solo carga, pasa a Wi-Fi.
- **Wi-Fi local:** Opciones de desarrollador › Depuración inalámbrica › «Vincular con código».
  `adb pair <ip>:<puerto_de_vincular> <código>` y luego `adb connect <ip>:<puerto_de_conexión>`.
  Son dos puertos distintos: el de la ventana de vincular y el de la pantalla principal.
- **A distancia / en la calle:** igual, pero con la IP de una VPN privada (por ejemplo Tailscale) en la PC y el
  celular. La PC no debe suspenderse.
- Si `adb pair` dice «protocol fault» pero ya estaba vinculado, intenta `adb connect` igual.
- El puerto cambia cuando la depuración inalámbrica se apaga: pide la captura nueva.

## Ver la pantalla
- `adb exec-out screencap -p > captura.png` para ver lo que ve el usuario.
- Solo capturar. No toques a ciegas: confirma qué pantalla está al frente, y que el usuario abra la pantalla.
- Captura el error antes de arreglarlo.
