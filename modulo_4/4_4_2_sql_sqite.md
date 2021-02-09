# SQL / SQLite

## La gran familia SQL

Ya sabemos que hay muchos tipos bases de datos:

- Bases de datos que guardan los datos en **colecciones de tipo JSON**.
- Bases de datos que guardan los datos en **tablas tipo excel**.
- Otros tipos de bases de datos.

En Adalab os vamos a enseñar a trabajar con bases de datos **tipo tabla**. Dentro de este tipo, hay muchas bases de datos. La más famosa y usada por más empresas es **SQL** (Structured Query Language).

Dentro de SQL a su vez hay muchas versiones de bases de datos, porque en programación cada uno coge algo que ya está existe, lo cambia un poquito, dice que ha reinventado la rueda y pide dinero a cambio ;)

Por ejemplo dentro de la familia **SQL** está:

- MySQL
- Microsoft SQL
- SQLite
- ...

Lo bueno es que si aprendes a usar una de estas familias, ya sabes usar el 99% del resto de familias.

En Adalab concretamente os vamos a enseñar a trabajar con **SQL + SQLite**, ya que SQLite está muy bien para aprender y para ser usada en proyectos pequeños.

## Instalación de SQLite Browser

Para usar una base de datos SQLite dentro de nuestros proyectos de Node JS no necesitamos nada más que instalar un paquete de NPM. Ya veremos cuál.

Pero para trabajar de una forma cómoda necesitamos un programa que tenga un entorno gráfico amigable. Vamos a instalar en nuestro ordenador [**SQLite Browser**](https://sqlitebrowser.org/), que podemos decir que es el devtools de la base de datos. Para ello:

### Instalación desde Windows

Entra en la [página de descargas de SQLite browser](https://sqlitebrowser.org/dl/) y descarla e instala la última versión. Seguramente sea la que pone **DB Browser for SQLite - Standard installer for 64-bit Windows**.

### Instalación desde Mac

Entra en la [página de descargas de SQLite browser](https://sqlitebrowser.org/dl/) y descarla e instala la última versión. Puedes hacerlo:

- Descargando e instalando la aplicación o...
- Ejecutando `brew install --cask db-browser-for-sqlite` desde una terminal de tu Mac.

> **Nota:** a lo mejor tienes que usar `sudo`.

### Instalación desde Ubuntu

Entra en la [página de descargas de SQLite browser](https://sqlitebrowser.org/dl/), apartado **Ubuntu and Derivatives** y verás que te pide que ejecutes los siguientes comandos en una terminal:

```bash
sudo add-apt-repository -y ppa:linuxgndu/sqlitebrowser
```

```bash
sudo apt-get update
```

```bash
sudo apt-get install sqlitebrowser
```

> **Nota:** a lo mejor tienes que usar `sudo`.

## Nuestra primera base de datos

Ahora que ya tenemos instalado SQLite browser abre la aplicación desde tu ordenador para que puedas seguir perfectamente los pasos que damos en este vídeo:

- Partiendo del ejercicio intro a SQL vamos a ver cómo funciona
- Ya tenemos instalado SQLite Browser, lo abrimos
- Tengo aquí preparado un ejercicio
   - Con este ejercicio vamos a gestionar una base de datos de usuarios registrados
   - Creo una base de datos
      - Creo la tabla
      - Creo los campos
         - Añadimos el id, más tarde explicaremos lo que es, más tarde explicaremos los que son el resto de campos de la configuración
         - Añadimos los campos y el tipo
      - Aquí puedo ver los registros que tiene la base de datos
      - Puedo añadir uno
      - Después de hacer cualquier cambio tengo que guardar
   - Por cierto la tabla sqlite_sequence es una tabla especial que necesita la base de datos para hacer sus cosas.
      - Debemos ignorarla y no modificarla nunca.
   - Navegador
      - Con este formulario enviamos un email y contraseña al servidor
   - Servidor
      - Así se configura la base de datos
         - Indicamos el fichero donde está la base de datos
         - Indicamos `verbose: console.log para que todas las llamadas que se hagan a la base de datos se muestren en consola
      - Con el endpoint
         - Obtenemos la fecha actual, esto es para que veamos que puedo añadir datos creados en el servidor o modificar los datos que nos vienen desde la web
         - Obtenemos los datos de la petición
         - Insertamos un nuevo registro en base de datos con la fecha, el email y el password
   - Hacemos una prueba
      - Vemos que se ha creado
- Como véis las tablas de SQL son como tablas de Excel
- En seguida veremos que se pueden crear muchas tablas dentro de una base de datos

> **IMPORTANTE:** os recordamos que cada vez que cambiamos algo en la base de datos desde SQLite hay que pulsar en **Guardar datos**.

## Diferencias entre base de datos, tablas y registros

- **Una base de datos en un conjunto de tablas**, lo que sería un documento de excel. Una aplicación de tamaño normal solo tiene una base de datos. Si es muy grande puede tener varias y puede combiar bases de datos de diferentes tipos.
- **Una tabla es un conjunto de regisros**, lo que sería una hoja de excel. Vamos a tener una tabla por cada una de las cosas que queramos guardar, como por ejemplo, una tabla para usuarios, otra tabla para productos, otra tabla para pedidos...
- **Un registro es cada una de las filas de una tabla**, lo que sería una fila de una hoja de un documento de excel. Cada registro guarda uno de nuestros usuarios, uno de nuestros productos, uno de nuestros pedidos...

Así que cuando penséis y habléis de bases de datos debéis usar las palabras adecuadas en cada caso.