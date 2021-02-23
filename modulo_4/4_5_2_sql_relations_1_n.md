# Relaciones 1 a N

## Múltiples tablas de una base de datos

Lo normal es tener **muchas tablas dentro de una base de datos** porque queremos guardar muchos tipos de información.

Por ejemplo en una tienda virtual vamos a tener una base de datos para los usuarios registrados, otra para los productos, otra para los pedidos, otra para las direcciones de entrega de los pedidos.

Cada tipo de información lo creamos en una tabla diferente con sus diferentes campos.

**A estos tipos de información les llamamos entidades o entities.** Una tabla guarda entidades del mismo tipo, por ejemplo usuarios. Y cada columna define las características de una entidad, como el nombre, email, password... del usuario.

## Relaciones entre los registros de dos tablas

Una base de datos suele tener muchas tablas. A menudo nos interesa relacionar unos registros de una tabla con los registros de otra tabla.

Por ejemplo en una tienda virtual tenemos una tabla para almacenar las diferentes direcciones de entrega donde se deben enviar los pedidos. Pero necesitamos saber qué dirección de entrega pertenece a un usuario concreto.

**Por ello queremos relacionar cada dirección con su usuario.**

Para relacionar los registros vamos a usar los campos `id` ya que son identificadores únicos que nunca van a cambiar.

**Por este motivo SQL se define como una base de datos relacional.**

## Relaciones 1 a N

En siguientes lecciones explicaremos las relaciones 1 a 1 y las relaciones N a N. Ahora vamos a empezar por explicar las relaciones 1 a N que son las más fáciles de entender:

<!-- - Vídeo
   - SQL es una base de datos relacional
      - Esto significa que vamos a tener muchas tablas dentro de nuestra base de datos
      - Cada registro de una tabla se relaciona con otro registro de otra tabla gracias a los ids
   - Esta podría ser la base de datos de una tienda online
      - Abrir la tabla usuarios
      - Si yo quiero guardar en base de datos la dirección de entrega del usuario puedo añadir más campos para el país, provincia...
      - Pero y si quiero guardar dos direcciones del usuario o tres o 30
      - No puedo saber cuantas direcciones va a añadir el usuario
      - Por ello lo que hago es crear otra tabla para las direcciones
      - Con el userId indico a qué usuario pertenece esta dirección
      - Así el usuario puede crear tantas direcciones como quiera
      - Así relaciono unas cosas con otras
   - Esto es una relación 1 a N porque cada 1 usuario puede tener N direcciones
   - Si nos damos cuenta es como si el usuario tuviese un array de direcciones -->