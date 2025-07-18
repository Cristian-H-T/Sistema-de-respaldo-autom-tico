# 💾 Respaldo Automático de Ubuntu Server a Google Drive

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
├── script de respaldo.sh   ← El script de respaldo
├── Documentacion              ← capturas de pantalla
├── requirements.txt  ← Lista de dependencias
├── documentacion Ubuntu.md  ← Paso a paso para configurar el ubuntu server
├── documentacion de credenciales para drive.md  ← Paso a paso de como conseguir las credenciales

```

----------------------------------------------------
🛠️ Dependencias
----------------------------------------------------

Instala estas dependencias en tu servidor Ubuntu:
- sudo apt update
- sudo apt install rclone -y

Instala esta dependecia en tu pc local:
- Ve al siguiente link y descarga el archivo zip: https://rclone.org/downloads/

----------------------------------------------------
✅ ¿Qué permite hacer este proyecto?
----------------------------------------------------

- Automatizar respaldos de configuraciones o archivos importantes de tu servidor Ubuntu.
- Comprimir y almacenar esos respaldos de forma eficiente.
- Subir los respaldos directamente a Google Drive usando rclone.
- Programar la ejecución diaria o periódica del respaldo con cron.
- Mantener tu Drive organizado eliminando respaldos antiguos automáticamente.
- Usar tanto entornos locales (VirtualBox) como entornos en la nube (AWS EC2).
