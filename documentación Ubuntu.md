# Aqui se vera el paso a paso para configurar su ubuntu server

1.- Primero en su maquina virtual de ubuntu server debe de colocar los comandos puestos en las dependencias aunque se las pondremos aqui de todas formas

- sudo apt update
- sudo apt install rclone -y

![image](https://github.com/user-attachments/assets/d0118e8f-2d4e-4932-bd37-34a50272e4b8)

![image](https://github.com/user-attachments/assets/0a3444b3-c555-4984-8f58-fc4b12f0e2b8)



2.- Luego configuraremos rclone

- coloque este comando: rclone config
  
2.1.- Luego del comando anterior siga estos pasos

- n → Nuevo remoto

![image](https://github.com/user-attachments/assets/f96208ad-1158-42a0-8527-1264914da965)

- Nombre: (el que prefiera)

![image](https://github.com/user-attachments/assets/894e7ab0-8163-49a0-b291-a3967512d847)

- Tipo: drive

![image](https://github.com/user-attachments/assets/313f5d33-28d3-46df-b150-43418e9b5d5d)

- client_id: descargue y copie el Client ID desde tu archivo JSON de su AOuth 2.0

![image](https://github.com/user-attachments/assets/bd560e8b-4889-414c-a9fd-43f4a36f6cc9)

![image](https://github.com/user-attachments/assets/105c0c77-5e2f-4c6d-a0e4-f7d5c925690e)

![image](https://github.com/user-attachments/assets/f7ddd595-01eb-4910-9662-5b49d1a251ce)

- client_secret: copia el Client Secret

![image](https://github.com/user-attachments/assets/d7121ae1-4fa1-411b-afa3-b8a7718d4644)

- Scope: 1 → acceso completo

![image](https://github.com/user-attachments/assets/6c3bc9fa-9e65-4e8c-9ddd-6404db3114f8)

- Root folder ID: dejar vacío

![image](https://github.com/user-attachments/assets/9309e1a0-f902-4385-b6c7-4df3f0c6557c)

- Service Account: n

![image](https://github.com/user-attachments/assets/bebb5833-ee17-499e-8066-d1438be50212)

- Autenticación: n para no usar autoconfig en el servidor

![image](https://github.com/user-attachments/assets/5ef6990c-7e11-4a8d-89ed-0ecde9e62d8d)

2.2.- Una vez que llegue aqui va a ver algo como esto:

![image](https://github.com/user-attachments/assets/71c82ad4-6952-4b6a-a246-9a1da81d75bd)

2.3.- Lo que debe de hacer ahora es descargar el archivo .zip de la dependecia local

- Haz clic en Windows AMD64 ZIP
- Extrae el ZIP en una carpeta (por ejemplo: C:\rclone)
- Abre una terminal (CMD o PowerShell)
- Entra a la carpeta extraída: cd C:\rclone

2.4.- Una opcion que funciona si es que no le abre la carpeta extraida es agregar rclone al PATH:

Para usarlo desde cualquier carpeta:

- Presiona Win + S, busca “Editar las variables de entorno del sistema”
- Haz clic en Variables de entorno
- En “Path”, haz clic en Editar > Nuevo
- Agrega la ruta a la carpeta donde está rclone.exe
- ✅ Luego abre una nueva terminal y ejecuta: rclone version

Una vez instalado el rclone en su pc debe de volver a la ultima imagen donde se ve lo que debe de copiar en el cmd algo como;

- rclone authorize "drive" "eyJjbGllbn... (etc.)"

![image](https://github.com/user-attachments/assets/74db7338-53de-415c-b401-4b16c86d71ca)

- Se le deberia de abrir una pagina en su navegador el cual les pedira colocar su correo

![image](https://github.com/user-attachments/assets/da878565-3795-4e06-b52e-0272fbce173e)

- Ya colocado su correo donde estara el drive saldra un mensaje de: Success! All done. Please go back to rclone
- Vuelva al cmd donde ya le dara el codigo a colocar en su Ubuntu server

3.- ✅ ¿Qué pasará después? rclone lo descodificará automáticamente

- Le preguntará: Configure this as a team drive? y colocara n
- Luego mostrará el resumen de la configuración.
- Y finalmente usted pondra y/n> y para guardar.

3.1.- Verifica que todo funciona:

Ya puedes probar que rclone está conectado a tu Google Drive ejecutando:

- rclone ls (el nombre que le puso al configurar rclone)

o tambien:

- rclone lsd el (nombre que le puso al configurar rclone)

Y su ubuntu ya estaria conectado con su google drive

4.- Ahora debe de crear correctamente el archivo respaldo.sh

4.1.- En su ubuntu coloque el siguiente comando:

- nano ~/respaldo.sh

4.2.- Dentro de esa carpeta debera de pegar el script que se encuentra en este proyecto

![image](https://github.com/user-attachments/assets/8b548182-89db-4221-abf7-a3200ba3cf5d)

4.3.- Debe de darle permisos de ejecución con: 

- chmod +x ~/respaldo.sh

4.4.- y ya por ultimo para ejecutar este script de forma manual use:

- sudo ~/respaldo.sh

Y ya estaria funcionando sin problemas

![image](https://github.com/user-attachments/assets/e65f2173-1eda-4ff5-85cd-b5169a4be71c)

5.- Programar el respaldo automático con cron

- Abre el editor de tareas programadas (como el crontab del usuario root): sudo crontab -e

5.1.- Y por ultimo agrega una línea como esta al final del archivo para que el respaldo se ejecute todos los días a la hora que desee (en el ejemplo esta puesta a las 9 am)

- 0 9 * * * /home/ubuntu/respaldo.sh >> /var/log/respaldo.log 2>&1

![image](https://github.com/user-attachments/assets/a6a27076-ec12-493f-b1cd-9a9920779b25)
