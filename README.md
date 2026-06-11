# Portfolio
Portfolio con capturas de los desarrollos de aplicaciones y webs para empresas de los que he formado parte donde se detalla las partes que realicé.

## Aplicación para gestión de videojuegos.

Este fue mi primer desarrollo en solitario, aunque ya tenía experiencia previa en desarrollos en equipos en otros trabajos de corta duración que tuve.

Se trata de una aplicación de escritorio que sirve para gestionar tus videojuegos, teniendo en un solo software toda la información de toda tu biblioteca de todas tus plataformas. Su objetivo es centralizar la biblioteca de videojuegos del usuario, independientemente de la plataforma o formato (digital o físico). Tiene un log-in con usuario, correo y contraseña, separando así las bibliotecas de los diferentes usuarios que puedan usar la aplicación en una misma casa. Además de algunas estadísticas como el género más repetido en la biblioteca del usuario, consola con más juegos en la colección, además de la posibilidad de generar un pdf con la biblioteca de videojuegos del usuario, por si la quiere en formato físico para imprimir.

La parte técnica es, conectarnos a una Base de Datos alojada en Neon, para poder verificar o registrar las credenciales del usuario, además de recuperar y mostrar los datos del usuario loggeado. Una vez conectados, podremos ver varios datos de nuestra biblioteca de juegos, además de ser la primera pantalla que veremos la de nuestra biblioteca de juegos. Podemos eliminar modificar o añadir videojuegos. Para obtener los datos como nombre género portada etc de un juego que queremos añadir, deberemos hacer una solicitud http a la API que usé para ello, RAWG, el usuario puede buscar por nombre del juego, género, consola... Datos que le pasaremos a la API mediante la solicitud http, la cual es una "plantilla" que se rellenará con los datos que le pase el usuario. Para simplificar el proceso, algunos datos inmutables como la consola o el género se extraen de la API RAWG y se le dan al usuario en un desplegable con todos ellos para que seleccione uno.

## Tecnologías utilizadas:
- Spring Boot para lanzar la aplicación.
- Spring Boot Starter Security para la encriptación de las contraseñas y la seguridad de los datos almacenados en la BBDD.
- Spring Boot Starter Data JPA para la conexión con la BBDD.
- Lombok para la simplificación y legibilidad del código.
- PostgreSQL para el código de los elementos relacionados con la BBDD (tablas, entidades...).
- JavaFX y FXML para las interfaces.
- Jakarta para la persistencia.
- Okhttp3 para simplificar las solicitudes http que realizaremos para obtener los datos de los juegos.
- PDFBox para generar el PDF con el resumen del perfil del usuario.

## Pantalla de inicio de sesión.
