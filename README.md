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
