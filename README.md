# 💾 Respaldo Automático de Ubuntu Server a Google Drive
=========================================

Este proyecto permite realizar respaldos automáticos de tu servidor Ubuntu (en AWS, VirtualBox u otro entorno) y subirlos directamente a tu Google Drive personal, usando rclone y tareas programadas con cron.

----------------------------------------------------
🌐 Requisitos previos
----------------------------------------------------

Cuenta de Google.
- Cuenta en Google Cloud Console para crear credenciales OAuth 2.0.
- Una instancia Ubuntu Server:
- En AWS (EC2) o
- En VirtualBox / Local.


----------------------------------------------------
📂 Estructura del proyecto (para GitHub)
----------------------------------------------------

```text
respaldo-gdrive-ubuntu/
├── README.md         ← Este archivo que acabamos de generar
├── script/
│   └── respaldo.sh   ← El script de respaldo
├── img/              ← Carpeta para subir tus capturas de pantalla
├── requirements.txt  ← Lista de dependencias

```

----------------------------------------------------
🛠️ Dependencias
----------------------------------------------------

Instala estas dependencias en tu servidor Ubuntu:
sudo apt update && sudo apt install -y rclone cron tar

✅ ¿Qué permite hacer este proyecto?

- Automatizar respaldos de configuraciones o archivos importantes de tu servidor Ubuntu.
- Comprimir y almacenar esos respaldos de forma eficiente.
- Subir los respaldos directamente a Google Drive usando rclone.
- Programar la ejecución diaria o periódica del respaldo con cron.
- Mantener tu Drive organizado eliminando respaldos antiguos automáticamente.
- Usar tanto entornos locales (VirtualBox) como entornos en la nube (AWS EC2).
