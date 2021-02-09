# Introducción a bases de datos

Una base de datos es un programa que **se está ejecutando en todo momento en nuestro servidor**, ya sea nuestro servidor local de desarrollo o el servidor de producción donde subiremos nuestro código.

Cuando reiniciamos nuestro ordenador, si volvemos a arrancar una aplicación de **Node JS se ejecuta como si fuera la primera vez**. Es decir no guarda nada de una ejecución a otra.

Cuando trabajamos con una base de datos, los cambios que hacemos sobre ella se guardan en un fichero. Por ello si reiniciamos el ordenador y volvemos a abrir la base de datos, esta mantiene los datos que tenía la última vez que se ejecutó. **Por ello las bases de datos nos permiten guardar datos de forma permanente.**

En la base de datos vamos a almacenar **todos los datos de nuestra aplicación y de nuestros usuarios** como por ejemplo:

- Email, contraseña, nombre... de nuestras usuarias registrados.
- Tweets de Twitter.
- Comentarios de los vídeos de Youtube.
- Artículos de un blog.
- En resumen, todos los datos que no tenemos a la hora de programar.

Vamos a charlar un poquito sobre bases de datos:

- Qué es un base de datos
   - Una base de datos es el programa que gestiona y almacena los datos de un servidor.
   - ¿Qué datos? Pues todo tipo de datos de nuestros usuarios:
      - El email y password de los usuarios registrados
      - Los productos, pedidos, métodos de pago y direcciones de una tienda online
      - Los tweets de twitter, los posts de un blog...
   - Por así decirlo toda la información de una página que no esté escrita en el código fuente de JS, HTML o lo que sea
- Dónde se ejecuta
   - Hemos visto que Node JS es un programa que se ejecuta en la terminal de un ordenador
   - Una base de datos también es otro programa que se ejecuta en un ordenador
   - También está conectado a Internet en todo momento y también está encendido en todo momento.
   - Desde Node JS vamos a ejecutar instrucciones de código que nos permiten leer y escribir en las bases de datos.
- Dónde se guardan los datos
   - Los datos de la base de datos se guardan en unos ficheros del ordenador. Por ello si el ordenador se apaga por la razón que sea, cuando se vuelve a guardar conserva los datos que tenía.
   - Esto no pasa con Node, si el servidor se apaga, al encenderse, Node se arranca desde el principio como si fuera la primera vez.
   - Con esto podemos entender que la finalidad de una base de datos es guardar datos de forma permanente.

# Tipos de bases de datos

- Tipos de bases de datos
  - Hay muchos, al igual que lenguajes de programación
     - Por ejemplo hay bases de datos que están pensadas para guardar poca información pero es muy rápido guardar información en ella.
     - Hay otras que están pensadas para guardar muchísima información y poder hacer búsquedas muy complejas dentro de esos datos, pero claro esas búsquedas son lentas.
  - De todos los tipos de bases de datos que hay los más importantes son dos:
     - Los que estructuran sus datos en tablas:
        - Es como si quisieramos guardar los datos en un excel donde las columnas son los campos que guardamos y las filas cada registro
        - Todos los registros de una tabla tienen los mismos campos
        - La base de datos más famosa que guarda datos en formato tabla es SQL.
     - Los que estructuran sus datos en JSON:
        - En vez de tablas se llaman colecciones
        - Son Arrays de objetos, y los datos que hay dentro de un objeto son los que quieras
        - A este tipo de bases de datos se les llama NoSQL (Not only SQL)
        - La más famosa es MongoDb