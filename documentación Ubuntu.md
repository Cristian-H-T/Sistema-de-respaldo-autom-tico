Aqui se vera el paso a paso para configurar su ubuntu server
1.- Primero en su maquina virtual de ubuntu server debe de colocar los comandos puestos en las dependencias aunque se las pondremos aqui de todas formas

- sudo apt update
- sudo apt install rclone -y

2.- Luego configuraremos rclone

- coloque este comando: sudo rclone config
  
2.1.- Luego del comando anterior siga estos pasos

- n → Nuevo remoto
- Nombre: gdrive (puedes cambiarlo)
- Tipo: drive
- client_id: copia el Client ID desde tu archivo JSON
- client_secret: copia el Client Secret
- Scope: 1 → acceso completo
- Root folder ID: dejar vacío
- Service Account: n
- Autenticación: n para no usar autoconfig en el servidor
2.2.- Una vez que llegue aqui descargue el archivo zip que se le pidio en 









