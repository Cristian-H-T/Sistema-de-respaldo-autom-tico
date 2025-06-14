En este apartado se vera como conseguir las credenciales necesarioas para conectar su ubuntu a su drive.

1.- Debe ir a la pagina de su google cloud e iniciar sesion con su correro en el cual suponemos que tambien estara su drive.
- aqui se le dejara u link para que vaya a la pagina directamente: https://console.cloud.google.com/

2.- Despues de ingresar con su correo cree un nuevo proyecto.

![image](https://github.com/user-attachments/assets/975e50e1-8a79-4b79-82e5-f8cee62b328c)

2.1.-Unicamente se coloca el nombre al proyecto ya que no es necesario colocar nada en la opcion de ubicacion.

![image](https://github.com/user-attachments/assets/8fd5bbc5-f9d1-41d1-acc0-504a278a6ee3)

2.2.-Despues de crear su nuevo proyecto le aparecera asi.

![image](https://github.com/user-attachments/assets/5460f713-ab17-4d69-8991-07d3839e6faf)

3.- Ahora debe de ir a apis y servicios para habilitar las api.

![image](https://github.com/user-attachments/assets/ade92ccb-38bd-4abb-83e5-e11c32ce58ff)

![image](https://github.com/user-attachments/assets/8190080a-5af0-4be8-8a4c-bda933d1d818)

3.1.- Busque la api de google drive y le deberia de aparecer el resultado de la segunda imagen.

![image](https://github.com/user-attachments/assets/50656073-777a-4413-a6ff-78ba38e5e16b)

![image](https://github.com/user-attachments/assets/5c670e03-3b2a-4765-9c70-c5fcb395036e)

4.- Una vez llegados a este punto se crearan las dos credenciales necesarias para este proyecto.

4.1.- Vaya donde dice credenciales y cree una clave API (esa sera la primera credencial que usaremos).

![image](https://github.com/user-attachments/assets/f2509692-887a-4f5c-946f-1ab5ec9e2457)

5.- Ahora crearemos la segunda credencial (OAuth 2.0).

5.1.- Vaya a pantalla de consentimiento OAuth y pulse donde dice cliente para crear uno nuevo, le saldra un recuadro en donde le pide ingresar el tipo de aplicacion y aqui debera de colocar App de escritorio y en nombre ponga el que prefiera.

![image](https://github.com/user-attachments/assets/adb11591-841c-48b7-b667-1a6856a3c0f1)

![image](https://github.com/user-attachments/assets/076e3b17-79f8-4504-89bc-41f983dd82b4)

![image](https://github.com/user-attachments/assets/2a450056-e56b-413d-bcd4-a9dd81eb42d7)

6.- Ahora nos adelantaremos un poco ya que aun estamos en google cloud.

6.1.- Encima del recuadro de clientes esta publico, una vez ahi nos iremos a usuarios de prueba y añadiremos uno, luego de eso colocaremos nuestro correo que estara vinculado al drive.

![image](https://github.com/user-attachments/assets/db7fd674-5c8c-4c70-baa0-d82572db5753)

![image](https://github.com/user-attachments/assets/a02af4b3-b798-48d4-b99f-b777c66cf0e8)
