# ¿Para qué usamos Clases en Python?

> Las Clases en el lenguaje Python las utilizaremos para lo que se conoce como **programación oirientada a objetos**. Asi, la programacion orientada a objetos, también conocida como **POO**  es un concepto muy utilizado para escribir aplicaciones potentes. En este sentido, debemos saber que como programador, dentro del trabajo científico de datos tendredremos que escribir aplicaciones para procesar esos datos y es aquí donde utilizaremos las denominadas **Clases**.

En definitiva las clases son mapeadores de objetos, lo que básicamente te permite crear un plano para los objetos. Esto significa que las clases pueden contener datos, funciones y comportamiento.

## Introducción a la Programación Orientada a Objetos (POO).

La programación orientada a objetos tiene algunas ventajas sobre otros patrones de diseño. El desarrollo es más rápido y con una mejor mantenibilidad del software. Esto, a su vez, conduce a un software de mayor calidad, que además es extensible con nuevos métodos y atributos. Sin embargo, es importante saber que la curva de aprendizaje es más pronunciada. Por otro lado, el software de POO es más lento y utiliza más memoria, ya que hay que escribir más líneas de código.

![La Clase & El Objeto](https://s3.us-east-2.amazonaws.com/mgpanel/619-poo-mgpanel2.jpg)

La programación orientada a objetos se basa en el paradigma de la ***programación imperativa***, que utiliza declaraciones para cambiar el estado de un programa. Se centra en describir cómo debe funcionar un programa.

Esto contrasta con la ***programación declarativa***, que se centra en lo que el programa informático debe realizar, sin especificar cómo. Ejemplos de ello son los lenguajes de consulta de bases de datos como SQL, en el que sólo se le dice al ordenador qué datos consultar y de dónde, pero no cómo hacerlo.

Por último, como hemos reflejado al inicio de esta pregunta, la programación orientada a objetos utiliza el concepto de **objetos** y **clases**. Una **clase** puede considerarse como un "plano técnico" de los objetos. Pueden tener sus propios atributos (características que poseen), y métodos (acciones que realizan).

### Ejemplo de Programación Orientada a Objetos (POO).

Un ejemplo de **clase** es la **clase** ``Dog``. No pienses en un perro concreto, ni en tu propio perro. Estamos describiendo lo que un perro es y puede hacer, en general. Los perros suelen tener ``name`` y ``age``; son atributos de instancia. Los perros también pueden ``ladrar``; éste es un método.

Cuando hablas de un perro concreto, en programación tendrías un objeto: un objeto es una instanciación de una **clase**. Éste es el principio básico en el que se basa la programación orientada a objetos. Así, mi perro Terry, por ejemplo, pertenece a la **clase** ``Dog``. Sus atributos son name = ``Terry`` y age = ``8``. Un perro diferente tendrá atributos diferentes.

### ¿Es Python un lenguaje de programación orientado a objetos?

Si. Python es un lenguaje de programación que admite la programación orientada a objetos. Por ello, lo vamos a utilizar para definir una clase con atributos y métodos, con el objetivo de poder llamarla. Python, además, ofrece una serie de ventajas en comparación con otros lenguajes de programación. Es un lenguaje dinámico con tipos de datos de alto nivel. Esto significa que el desarrollo es mucho más rápido que otros lenguajes. No requiere que eldeclaremos tipos de variables y argumentos. Esto también hace que Python sea más fácil de entender y aprender para las personas que están comenzando en el mundo de la programación, ya que su código es más legible e intuitivo.

![Python & Objetos](https://www.cursosgis.com/wp-content/uploads/2017/06/python_objetos_2.png)

## Como se crea una Clase Básica. 

Para definir una clase en Python, podemos utilizar la palabra clave ``class``, seguida del nombre de la clase y dos puntos. Dentro de la clase, hay que definir un método ``__init__`` con ``def``. Este es el inicializador que puedes utilizar después para instanciar objetos. Es similar a un constructor en Java. ``__init__`` ¡siempre debe estar presente! Toma un argumento: ``self``, que se refiere al objeto en sí. Dentro del método, se utiliza la palabra clave ``pass`` a partir de ahora, porque Python espera que escribas algo ahí. ¡Recuerda utilizar la sangría correcta!

```
class Dog:

    def __init__(self):
        pass
```

Para instanciar un objeto, se escribe el nombre de la clase, seguido de dos paréntesis. Podemos asignarlo a una variable para hacer un seguimiento del objeto.

```
terry = Dog()

print(terry)
```

Tras imprimir ``terry``, queda claro que este objeto es un perro. Pero aún no hemos añadido ningún atributo. Por ello daremos un nombre y una edad a la clase ``Dog`` reescribiéndola:

```
class Dog:

    def __init__(self, name, age):  
        self.name = name
        self.age = age
```

Para cerrar apartado de como se crea una clase básica, podemos ver que la función toma ahora dos argumentos después de ``self``: ``name`` y ``age``. A continuación, se asignan a ``self.name`` y ``self.age`` respectivamente. Ahora puedes crear un nuevo objeto terry con un nombre y una edad:

```
terry = Dog("Terry", 8)
```

Por último, para acceder a los atributos de un objeto en Python, podemos utilizar la anotación con punto. Esto se hace escribiendo el nombre del objeto, seguido de un punto y el nombre del atributo:

```
print(terry.name)

print(terry.age)

terry
8
```
---


# ¿Qué método se ejecuta automáticamente cuando se crea una instancia de una clase?

> Cuando se crea una **instancia de una clase**, el método ``__init__`` es llamado **automáticamente** por el intérprete de Python y se utiliza para realizar cualquier inicialización que sea necesaria para la instancia. El método ``__init__`` se usa para asignar valores iniciales a los atributos de una instancia de la clase.

Pa ampliar la información se puede consultar este video: [Método __init__ constructor POO en Python](https://youtu.be/4GV20aOmbt4 “Método __init__”)

Como deciamos y a modo de resumen, el método ***init*** se ejecuta automáticamente al crear una instancia de una clase en memoria durante la programación. Así, inicializa nuevos objetos usando los argumentos pasados ​​y asigna el estado inicial.

## Sintaxis y Ejemplo de la función constructora init de Python.

En Python, la forma de hacer esto es decir ``def`` y luego ``Dunder`` ``init`` y la forma correcta de escribirlo es:

```
__init__
```
Esta es una función reservada especial dentro del lenguaje Python, aunque no crees una función propia llamada init. Está disponible para las clases, y las funciones constructoras como init funcionan de forma que se llamará automáticamente al instanciar la clase.

Al crear una factura, primero se accede a la función "init" y esta procesará todo su contenido, configurando todo lo necesario y, específicamente para nuestro caso, agregando los datos a la clase. El primer argumento que se pasa es "self", ya que toda función dentro de una clase de Python necesita "self".

Luego, pasaremos un par de argumentos más: "client" y "total". Estas palabras clave no tienen nada de especial; son solo los elementos que usaremos para crear nuestra factura. La creamos como cualquier función, terminando con dos puntos.

![¿Que es __init__](https://codigoencasa.com/content/images/2024/06/1_vRslGzL6g4YZkmkF5DDX1g.gif)

Después, dentro de esta función init lo que voy a hacer es agregar los datos directamente a la clase y la forma de hacerlo es diciendo self dot y luego vamos a crear un nombre de variable, así que voy a establecer un ``self.client = client`` y ``self.total = total``.

Pero la razón por la que está estructurado así es porque, recordemos que prácticamente todo en Python es un objeto. Por lo tanto, al crear una factura, queremos asignar los datos introducidos. Por ejemplo, los datos introducidos para cliente y total se asignarán al objeto recién creado. Esto significa que creamos dos nuevas variables relacionadas directamente con la instancia. Si creamos ``inv_one`` y asignamos el nombre del cliente a ``Google``, ``self.client`` será igual a ``Google``. 

Ahora posteriormente crearemos la función. Diremos que `def formatter` y `formatters` simplemente tomarán `self` como cualquier otra función. La razón por la que hacemos esto, y espero que ahora tenga más sentido, es porque tenemos acceso a `self` en esta función formateadora. Esto significa que tenemos acceso a esos datos en `self`, por lo que tenemos acceso a este cliente y a ese total.

Y por último lo que quiero que haga el formateador es devolver una cadena formateada, digamos ``F`` y luego pasarla usando la sintaxis literal de cadena ``self.client`` y cerrarla y luego diremos que deben y luego ``$`` con llaves ``self.total`` cerrarla y finalizar la cadena y eso es todo lo que necesitamos hacer. Veamos aquí toda la sintaxis junta: 

```
class Invoice:
  def __init__(self, client, total):
    self.client = client
    self.total = total

  def formatter(self):
    return f'{self.client} owes: ${self.total}'


google = Invoice('Google', 100)

print(google.formatter())
```
---

# ¿Cuáles son los tres verbos de API?

> En el contexto de **API REST** los tres verbos denominados como los más comunes son **GET**, **POST** y **PUT**. Son los tres verbos básicos usados en las API REST para interactuar con los recursos de un servidor. Si utilizamos la aplicación Flask, podemos configurar rutas para manejar estos verbos y definir el comportamiento de nuestra aplicación web según el verbo HTTP recibido. Aunque es importate saber que hay mas verbos a parte de los tres mas comunes. 

Siguiendo en el contexto de API REST estos tres verbos significan lo siguiente: 

* ``GET``: Se utiliza para obtener información de un recurso. Por ejemplo, al hacer una solicitud GET, le estás pidiendo al servidor que te devuelva los datos de un recurso específico.

* ``POST``: Se utiliza para enviar datos al servidor y crear un nuevo recurso. Por ejemplo, cuando envías un formulario o datos a través de un POST, estás creando un nuevo registro o recurso en el servidor.

* ``PUT``: Se utiliza para actualizar un recurso existente. A diferencia de POST, que generalmente crea un nuevo recurso, PUT reemplaza el recurso existente con los nuevos datos proporcionados.

## Cómo manejar los verbos GET, POST, y PUT en una aplicación Flask.

1. ``GET``: Obtener datos de un recurso. En este ejemplo, vamos a imaginar que tenemos una lista de usuarios y queremos obtener la información de un usuario específico:

```
from flask import Flask,jsonify 

app = Flask(__name__)

usuarios = [
    {'id': 1, 'nombre': 'Silvia'},
    {'id': 2, 'nombre': 'Eric'},
    {'id': 3, 'nombre': 'Ibon'}
]

@app.route('/usuario/<int:id>', methods=['GET'])
def obtener_usuario(id):
    usuario = next((user for user in usuarios if user['id'] == id), None)
    if usuario:
        return jsonify(usuario)
    else:
        return jsonify({'error': 'Usuario no encontrado'}), 404

if __name__ == '__main__':
    app.run(debug=True)
```
2. ``POST``: Crear un nuevo recurso. Ahora agregaremos un nuevo usuario a la lista mediante una solicitud POST.

```
from flask import Flask, request, jsonify

app = Flask(__name__)

usuarios = [
    {'id': 1, 'nombre': 'Silvia'},
    {'id': 2, 'nombre': 'Eric'}
]

@app.route('/usuario', methods=['POST'])
def agregar_usuario():
    data = request.get_json()  
    nuevo_id = len(usuarios) + 1  # Generamos un ID único
    nuevo_usuario = {'id': nuevo_id, 'nombre': data['nombre']}
    usuarios.append(nuevo_usuario)
    return jsonify(nuevo_usuario), 201  

if __name__ == '__main__':
    app.run(debug=True)
```

3. ``PUT``: Actualizar un recurso existente. Ahora em este ultimo ejemplo actualizaremos el nombre de un usuario en la lista: 

```
from flask import Flask, request, jsonify

app = Flask(__name__)

usuarios = [
    {'id': 1, 'nombre': 'Silvia'},
    {'id': 2, 'nombre': 'Eric'}
]

@app.route('/usuario/<int:id>', methods=['PUT'])
def actualizar_usuario(id):
    usuario = next((user for user in usuarios if user['id'] == id), None)
    if usuario:
        data = request.get_json()  
        usuario['nombre'] = data['nombre']  
        return jsonify(usuario)
    else:
        return jsonify({'error': 'Usuario no encontrado'}), 404

if __name__ == '__main__':
    app.run(debug=True)
```
Por último y a modo de resumen de este epígrafe de la documentación debemos tener bien claro que, cada uno de estos verbos se utiliza con métodos específicos dentro de la aplicación Flask para realizar la acción adecuada según el tipo de solicitud HTTP: 

* GET: Se utiliza para obtener información sobre un recurso.

* POST: Se utiliza para crear un nuevo recurso.

* PUT: Se utiliza para actualizar un recurso existente.

---


# ¿Es MongoDB una base de datos SQL o NoSQL?

> MongoDB es un sistema de base de datos NoSQL, orientado a documentos y de código abierto. En lugar de guardar los datos en tablas, tal y como se hace en las bases de datos relacionales, MongoDB guarda estructuras de datos BSON (una especificación similar a JSON) con un esquema dinámico, haciendo que la integración de los datos en ciertas aplicaciones sea más fácil y rápida.

Antes de seguir con la explicación de uso de MongoDB recomiendo ver este video para hacer su instalación de una manera muy sencilla y altamente pedagógica: [Cómo instalar y configurar MongoDB](https://youtu.be/heZhS6UzF7k “MongoDB”)

De este modo y segun la web de la propia aplicación, MongoDB es una base de datos de documentos que nos ofrece una gran escalabilidad y flexibilidad, siendo al mismo tiempo un modelo de consultas e indexación avanzado.

## Características de MongoDB. 

Si tuviéramos que resumir a una la principal característica a destacar de MongoDB, sin duda esta sería la velocidad, que alcanza un balance perfecto entre rendimiento y funcionalidad gracias a su sistema de consulta de contenidos. Pero sus características principales no se limitan solo a esto, MongoDB cuenta, además, con otras que lo posicionan como el preferido de muchos desarrolladores.

Características principales:

* **Consultas ad hoc**. Con MongoDb podemos realizar todo tipo de consultas. Podemos hacer búsqueda por campos, consultas de rangos y expresiones regulares. Además, estas consultas pueden devolver un campo específico del documento, pero también puede ser una función JavaScript definida por el usuario.
* **Indexación**. El concepto de índices en MongoDB es similar al empleado en bases de datos relacionales, con la diferencia de que cualquier campo documentado puede ser indexado y añadir múltiples índices secundarios.
* **Replicación**. Del mismo modo, la replicación es un proceso básico en la gestión de bases de datos. MongoDB soporta el tipo de replicación primario-secundario. De este modo, mientras podemos realizar consultas con el primario, el secundario actúa como réplica de datos en solo lectura a modo copia de seguridad con la particularidad de que los nodos secundarios tienen la habilidad de poder elegir un nuevo primario en caso de que el primario actual deje de responder.
* **Balanceo de carga**. Resulta muy interesante cómo MongoDB puede escalar la carga de trabajo. MongoDB tiene la capacidad de ejecutarse de manera simultánea en múltiples servidores, ofreciendo un balanceo de carga o servicio de replicación de datos, de modo que podemos mantener el sistema funcionando en caso de un fallo del hardware.
* **Almacenamiento de archivos**. Aprovechando la capacidad de MongoDB para el balanceo de carga y la replicación de datos, Mongo puede ser utilizado también como un sistema de archivos. Esta funcionalidad, llamada GridFS e incluida en la distribución oficial, permite manipular archivos y contenido.
* **Ejecución de JavaScript del lado del servidor**. MongoDB tiene la capacidad de realizar consultas utilizando JavaScript, haciendo que estas sean enviadas directamente a la base de datos para ser ejecutadas.

## Cómo funciona la aplicación MongoDB.

MongoDB es una base de datos orientada a documentos. Esto quiere decir que en lugar de guardar los datos en registros, guarda los datos en documentos. Estos documentos son almacenados en BSON, que es una representación binaria de JSON.

Esto representa una de las diferencias más importantes con respecto a las bases de datos relacionales. Y resulta que no es que no es necesario seguir un esquema. Los documentos de una misma colección - concepto similar a una tabla de una base de datos relacional -, pueden tener esquemas diferentes.

Imaginemos que tenemos una colección a la que llamamos Personas. Un documento podría almacenarse de la siguiente manera:

```
{

   Nombre: "Txema",
   Apellidos: "Gonzalez",
   Edad: 39,
   Aficiones: ["Música","Ciclismo","Baloncesto"],
   Amigos: [
       {
         Nombre:"Maria",
         Edad:35    },
       {
         Nombre:"Luis", 
         Edad:42
       }
   ]
} 
```
Como se puede ver el ejemplo de código, la sintaxis es exactamente igual a lo que conocemos de un documento JSON. Lo interesante viene cuando queremos almacenar en una misma colección un documento como este: ``{ Nombre: "Roger Rabbit", Estudios: "Dibu y conejo", Amigos:102 }`` Tal como podemos ver, este no sigue el mismo esquema del primero, añadiendo algún campo nuevo que no existe en el documento anterior o incluso de un tipo distinto, pero no importa.

## Ventajas de la aplicación MongoDB.

![Ventajas de las Bases de Datos NoSQL](https://miro.medium.com/v2/resize:fit:720/format:webp/1*inswuUJi0eKszlhVWBpBaw.png)

1. **Equilibrio de carga.**
El auge de las aplicaciones en cloud y el incremento de la demanda de recursos para las empresas complican la disponibilidad y la fiabilidad de los servicios. El proceso de uso compartido del equilibrio de carga de MongoDB distribuye grandes conjuntos de datos a través de varias máquinas virtuales a la vez manteniendo rendimientos aceptables de lectura y grabación. Esta escalada horizontal se llama sharding (fragmentación) y ayuda a las organizaciones a evitar el coste de la escalada vertical de hardware al mismo tiempo que expande la capacidad de los despliegues basados en cloud.

2. **Consultas de base de datos ad hoc.**
Una de las mayores ventajas de MongoDB sobre otras bases de datos es su capacidad para manejar consultas ad hoc que no requieren esquemas predefinidos. Las bases de datos MongoDB utilizan un lenguaje de consulta similar a las bases de datos SQL que es extremadamente accesible, tanto para desarrolladores principiantes como avanzados. Esta accesibilidad facilita el envío, la consulta, la clasificación, la actualización y la exportación de sus datos con métodos de ayuda comunes y mandatos shell simples.

3. **Soporte a múltiples lenguajes.**
Uno de los mejores aspectos de MongoDB es su soporte a múltiples lenguajes. Se han publicado varias versiones de MongoDB y están en continuo desarrollo con soporte de controlador para los lenguajes de programación más populares, incluidos Python, PHP, Ruby, Node.js, C++, Scala, JavaScript y muchos más.

---


# ¿Qué es una API?

> **API** es una Interfaz de Programación de Aplicaciones. Es un servicio, algo parecido a un sitio WEB o servidor con el que podemos comunicarnos y en vez de devolvernos una página web, no devuelve datos con los que poder desarrollar aplicaciones y también nos permite pasar datos de un lado a otro. **API** es la forma en que podemos comunicarnos con una aplicación y podemos hacerlo implemetando un denominado "raspador".

![Una API es](https://i.ytimg.com/vi/rzqA4VvqTAk/maxresdefault.jpg)

Las APIs suponen un conjunto de funciones y procedimientos que permite integrar sistemas, permitiendo que sus funcionalidades puedan ser reutilizadas por otras aplicaciones o software o dicho de otra manera, es un conjunto de reglas o protocolos que permiten que las aplicaciones de software se comuniquen entre sí para intercambiar datos, características y funcionalidades.

## ¿Para qué sirve una API? & ¿Cómo funcionan las API?

Las APIs sirven para establecer un punto de conexión o interacción entre dos sistemas software. Sin ellas, no sería posible la conexión entre redes sociales, plataformas online, sistemas operativos o bases de datos.

El uso que se le dé dependerá de los permisos otorgados por el propietario de la API. La forma en la que una de las partes envía la solicitud de respuesta determinará cómo responderá el software de la otra parte.

![Cómo funcionan las API](https://outvio.com/static/b649eefd687b1e175f6cb22298929902/cfddd/cl2t0lc4l000w7b7t0yli356j.webp)

En función del tipo de API, el funcionamiento de esta cambiará. Sin embargo, de forma general, podemos decir que una API actúa como mensajero mandando una solicitud a un servidor, traduciendo el mensaje y entregando la respuesta al usuario.

### Tipos de API.

Según el nivel de acceso que permitan, podemos diferenciar entre:

1. API privada es utilizada de forma interna
2. API para partners, accesible solamente para desarrolladores externos autorizados
3. API pública es aquella creada para ser utilizada por cualquier desarrollador

Según la localización de ambos sistemas, pueden ser:

1. APIs locales: para aplicaciones que se comunican dentro de un mismo ecosistema. 
2. APIs remotas: para aquellas conexiones que se realizan desde un sistema en un punto diferente.

### Ventajas & Conclusiones de API.

La principal ventaja de utilizar una API y su razón de ser es el ahorro de tiempo y dinero que suponen a la hora de desarrollar soluciones software mediante la utilización de un código que ya está probado y funcionando.

El concepto de API nació para facilitar la comunicación entre programas. Esto significa que, al menos teóricamente, son fáciles de entender y promueven el crecimiento de una de las partes, o de ambas, ya que permiten ampliar las funcionalidad del sistema, reducir errores o acelerar procesos, entre otras ventajas, con una cantidad menor de recursos invertidos: tiempo, dinero…

Además de este ahorro de tiempo y recursos en el desarrollo, el uso de una aplicación determinada puede atraer a clientes. Por ejemplo, puede que a tus clientes les guste hacer compras a través de Amazon.

Siempre que se gestionen de forma correcta, el uso de una API permite ofrecer acceso a los recursos sin comprometer la seguridad, implementando, por ejemplo, el uso de una puerta de enlace de API.

En definitiva, una API ayuda a las empresas con una presencia online a acelerar su crecimiento, brindar una experiencia al usuario final más consistente, gracias al uso de un código ya existente y probado y a solventar problemas y ejecutar acciones con la cantidad mínima de recursos utilizados en el desarrollo.

---


# ¿Qué es Postman?

> **Postman** es una aplicación diseñada para poder establecer comunicaciones con **APIs** externas.  **Postman** ofrece una plataforma API para que los desarrolladores podamos diseñar, crear, probar y colaborar en API. Postman en sus inicios nace como una extensión que podía ser utilizada en el navegador de Google y básicamente permite realizar peticiones de una manera simple para testear APIs de tipo REST propias o de terceros.

![Beneficios de la APP Postman](https://miro.medium.com/v2/resize:fit:720/format:webp/1*x7zmO-4hYqmYtffpqRv0Hw.png)

Gracias a los avances tecnológicos, Postman ha evolucionado y ha pasado de ser de una extensión a una aplicación que dispone de herramientas nativas para diversos sistemas operativos como lo son Windows, Mac y Linux.

## Para qué sirve Postman.

Postman sirve para múltiples tareas dentro de las cuales destacaremos en esta oportunidad las siguientes:

* Testear colecciones o catálogos de APIs tanto para Frontend como para Backend.
* Organizar en carpetas, funcionalidades y módulos los servicios web.
* Permite gestionar el ciclo de vida (conceptualización y definición, desarrollo, monitoreo y mantenimiento) de nuestra API.
* Generar documentación de nuestras APIs.
* Trabajar con entornos (calidad, desarrollo, producción) y de este modo es posible compartir a través de un entorno cloud la información con el resto del equipo involucrado en el desarrollo.

## Métodos más utilizados & posibles errores en Postman.

Postman cuenta con una serie de métodos que nos permiten tomar acción ante nuestras peticiones, a continuación, te dejamos los más utilizados:

* ``GET``: Obtener información.
* ``POST``: Agregar información.
* ``PUT``: Reemplazar la información.
* ``PATCH``: Actualizar alguna información.
* ``DELETE``: Borrar información.

En cuanto a los posibles errores que podemos apreciar en la respuesta que nos ofrece la herramienta, lo resumiremos en que si la respuesta dada se encuentra en el rango de “200” quiere decir que toda la petición ha salido sin inconvenientes; mientras que el rango de los códigos de error “400” hacen referencia a errores con el cliente y aquellos errores en la línea de los “500” tienen que ver con fallos en el servidor.

## Ventajas & Conclusiones de Postman.

* Cuenta con una comunidad grande de usuarios.
* Es posible llevar a cabo trabajos de colaboración con el resto de los miembros de un equipo.
* Su interface es sencilla, atractiva a la vista del usuario e intuitiva.
* Cuenta con una extensión para el navegador web Google Chrome.
* Es posible agregar scripts (JavaScript) para añadir validaciones, automatizar y/o configurar pruebas.
* Es posible integrarla con otras herramientas.
* Y vimos al inicio de este epígrafe de la documentación permite trabajar con colecciones, que vienen siendo nuestra base de datos con las peticiones realizadas.

Por último, a modo de conclusión podemos decir que Postman es una herramienta que sirve de gran ayuda a los equipos de desarrollo, permitiendo mantener las colecciones actualizadas, ahorrando los tiempos de respuesta al momento de realizar los test o las llamadas a los servicios. Es potente gracias a su fácil integración con APIs de terceros y cuenta con una gran comunidad.

Para concluir te recomiendo que veas este video para dar los primeros pasos en esta gran aplicación: [Intro a Postman](https://youtu.be/OiDrIJRPoTE “Primero pasos en Postman”)

---


# ¿Qué es el polimorfismo?

> El **polimorfismo** en el lenguaje de Python está muy relacionado con el concepto de herencia y hace referencia a lo que podría parecer una palabra grande o compleja pero en realidad refleja algo sencillo. A nivel etimológico, "poli" significa muchos y "morfismo" significa cambiar, lo que supone que estamos hablando de un concepto de Python que aglutina muchos cambios.

![Polimorfismo es...](https://files.codingninjas.in/article_images/custom-upload-1683185384.webp)

* Siguiendo con el significado de polimorfismo en Python, éste hace referencia a la capacidad que tienen los objetos de diferentes clases para responder al mismo mensaje. En otras palabras, dos objetos de diferentes clases pueden tener métodos con el mismo nombre, y ambos métodos pueden ser llamados con el mismo código, dando respuestas diferentes. 

* El polimorfismo es una forma de lograr una mayor flexibilidad en nuestro código. Por ejemplo, puede realizar sumas aritméticas para números y concatenar cadenas para cadenas.

## Ejemplo de Polimorfismo en Python.

Veamos este ejemplo: 

```
class Animal:
    def __init__(self, name):
        self.name = name

    def make_sound(self):
        pass

class Dog(Animal):
    def make_sound(self):
        return "guau"

class Cat(Animal):
    def make_sound(self):
        return "miau"

class Cow(Animal):
    def make_sound(self):
        return "muu"
```
En el ejemplo, hemos hecho lo siguiente:

* Creamos, una superclase **Animal** y tres subclases **Dog**, **Cat** y **Cow**.
* Las tres subclases van a heredar de la clase base.
* Cada una de ellas tiene su propio método **make_sound()** la cual genera como mensaje el sonido respectivo del animal.

Siguiendo con el ejemplo vamos a:

1. Vamos a crear una lista de objetos (nuestros animales) a las cuales les pondremos sus respectivos nombres:

```
animals = [Dog("Terry"), Cat("Blanca"), Cow("Milka")]
```

2. Ahora, como lo guardamos en una lista vamos a realizar un ciclo que nos permita recorrer y llamar al método **make_sound()** de cada una de las subclases:

```
animals = [Dog("Terry"), Cat("Blanca"), Cow("Milka")]

for animal in animals:
    print(animal.name + " dice " + animal.make_sound())
```
3. Por último, si lo hemos realizado correctamente debe sacar el siguiente resultado: 

```
Terry dice guau
Blanca dice miau
Milka dice muuu
```
En resumen y como mensaje final, el polimorfismo en el lenguaje Python nos permite que diferentes objetos se comporten de manera similar, básicamente que adquieran “diferentes formas”, lo que hace que nuestro código sea más flexible y fácil de mantener.

---


# ¿Qué es un método dunder?

> En el lenguaje de programación de Python los **métodos dunder** son los métodos que se caracterizan porque su sintaxis comienza y termina siempre con dos guiones bajo. Se considera un método especial o incluso se le denomina también como un método mágico Se llaman así porque el nombre de todos ellos comienza y termina con dos caracteres underline ``(__)``

Antes de describir dos de los métodos Dunder más importantes, es importante saber que estamos hablando de una sintaxis extraña con los guiones bajos dobles delante del nombre. Esto se relaciona directamente con el funcionamiento de Python con los métodos privados y protegidos dentro de sus clases. Así, debemos saber que en muchos otros lenguajes de programación, no es necesario usar este tipo de estructura. No es necesario usar estos guiones bajos inusuales ni nada parecido, ya que cuentan con métodos privados.

Por ello y como el lenguaje Python no tiene métodos privados o protegidos, lo que hicieron fue decidir crear estos métodos Dunder, de modo que cada vez que vea un método Dunder en Python significa que se trata de un método que se le proporciona directamente desde el lenguaje Python.

En resumen, cada vez que veamos un **método dunder** en Python significa que es un métodos que se proporciona directamente desde Python; y se podrá usar pero no se podrá ni anular ni cambiar de ninguna manera. 

![Métodos mágicos de Python](https://media.geeksforgeeks.org/wp-content/uploads/20230426155435/Screenshot-from-2023-04-26-15-54-26.png)


## Descripción general de algunos métodos Dunder en Python: 3 ejemplos.

* Un primer ejemplo del método dunder es el ***dunder string*** o ``str``:

```
class Invoice:

    def __str__(self)
    return 'This is the invoice class'

inv = Invoice()
print = (str(inv))
```

* Un segundo ejemplo hace referencia a la definición de una clase donde suele haber un método llamado ``__init__`` que se conoce como inicializador. Este método es un método especial que se llama cada vez que se instancia una clase y sirve para inicializar el objeto que se crea.

```
class Teacher:
    
    def __init__(self, name, subject):
        self.name = name
        self.subject = subject
     
    def show(self):
        print(self.name, " teaches ", self.subject)
 T = Teacher('Txema Gonzalez', "Computer Science")
 ```
 * Un tercer ejemplo significativo de método dunder puede ser **Dunder repr**  ``__repr__``. Este dunder se utiliza más para la salida en bruto. Normalmente cuando se está programando no se le da un buen formato y lo utilizaremnos cuendo tengamos un "class" grande. El método Dunder repr es muy similar a Dunder string, con la diferencia clave de que Dunder repr se usa más para la salida sin procesar, por lo que no suele formatearse correctamente. En la práctica no hay ninguna diferencia en la implementación. La única diferencia es el nombre, y luego cambiamos su representación. El patrón común en Python es usar una cadena para la salida, quizás algo fácil de leer, y luego, con **Repr**, se obtienen los datos sin procesar de la instancia de la clase. Lo veremos a continuación con un ejemplo de sintaxis en el que se pueden ver los tres métodos dunder que hemos explicado.

 ```
clase  Factura :
   def  __init__ ( self , cliente, total):
     self.client = cliente
     self.total = total

  def  __str__ ( self ):
     return f " Factura de {self.client} por {self.total} "

  def  __repr__ ( self ):
     return f " Factura({self.cliente}, {self.total}) "


inv = Factura( ' Google ' , 500 )
imprimir( str (inv))
imprimir( repr (inv))
 ```

---


# ¿Qué es un decorador de Python?

> Los **decoradores** son **funciones** que modifican el comportamiento de otras funciones, ayudan a acortar nuestro código y hacen que se ajuste mucho más a la filosofía de Python. Si alguna vez has visto ``@``, estás ante un decorador o decorator, bien sea uno que Python ofrece por defecto o uno que puede haber sido creado ex-profeso.De este modo, podemos afirmar que los **decoradores** decoran una función y sobre todo sirven para tener más con menos código.   

A través de los decoradores de Python seremos capaces reducir las líneas de código duplicadas, haremos que nuestro código sea más legible, fácil de testear, fácil de mantener y sobre todo, tendremos un código mucho más acorde con las buenas prácticas del lenguaje Python.

![Decoradores en Python](https://i.ytimg.com/vi/xWVLsGwMplE/maxresdefault.jpg)

El funcionamiento de los decoradores se basa en tres ideas que vamos a desarrollar a continuación y que son las siguientes:

* Dentro de una función se pueden crear más funciones.
* Las funciones pueden retornar funciones.
* Las funciones se pueden pasar como argumentos a otras funciones.

## Ejemplo de decorador de Python

Veamos un ejemplo muy sencillo. Tenemos una función ``suma()`` que vamos a decorar usando ``mi_decorador()``. Para ello, antes de la declaración de la función suma, hacemos uso de ``@mi_decorador``.

```
def mi_decorador(funcion):
    def nueva_funcion(a, b):
        print("Se va a llamar")
        c = funcion(a, b)
        print("Se ha llamado")
        return c
    return nueva_funcion

@mi_decorador
def suma(a, b):
    print("Entra en funcion suma")
    return a + b

suma(5,8)

Se va a llamar
Entra en funcion suma
Se ha llamado

```
Lo que realiza ``mi_decorador()`` es definir una nueva función que encapsula o envuelve la función que se pasa como entrada. Concretamente lo que hace es hace uso de dos ``print()``, uno antes y otro después de la llamada la función.

Por lo tanto, cualquier función que use ``@mi_decorador`` tendrá dos print, uno y al principio y otro al final, dando igual lo que realmente haga la función.

## Decoradores con parámetros.

Tal vez quieras que tu decorador tenga algún parámetro de entrada para modificar su comportamiento. Se puede hacer envolviendo una vez más la función como se muestra en el siguiente ejemplo:

```
def mi_decorador(arg):
    def decorador_real(funcion):
        def nueva_funcion(a, b):
            print(arg)
            c = funcion(a, b)
            print(arg)
            return c
        return nueva_funcion
    return decorador_real

@mi_decorador("Imprimer esto antes y después")
def suma(a, b):
    print("Entra en funcion suma")
    return a + b

suma(5,8)

Imprimer esto antes y después
Entra en funcion suma
Imprimer esto antes y después
```
Es importante recalcar que los ejemplos mostrados hasta ahora son didácticos, y no tienen mucha utilidad práctica. Veamos un ejemplo más práctico con el ejemplo **loger**. Su uso nos permite escribir en un fichero los resultados de ciertas operaciones, que funciones han sido llamadas, o cualquier información que en un futuro resulte útil para ver que ha pasado. En el siguiente ejemplo tenemos un uso más completo del decorador ``log()`` que escribe en un fichero los resultados de las funciones que han sido llamadas:

```
def log(fichero_log):
    def decorador_log(func):
        def decorador_funcion(*args, **kwargs):
            with open(fichero_log, 'a') as opened_file:
                output = func(*args, **kwargs)
                opened_file.write(f"{output}\n")
        return decorador_funcion
    return decorador_log

@log('ficherosalida.log')
def suma(a, b):
    return a + b

@log('ficherosalida.log')
def resta(a, b):
    return a - b

@log('ficherosalida.log')
def multiplicadivide(a, b, c):
    return a*b/c

suma(10, 30)
resta(7, 23)
multiplicadivide(5, 10, 2)
```
Antes de concluir, unicamente recalcar queque el decorador puede ser usado sobre funciones que tienen diferente número de parámetros de entrada, y su funcionalidad será siempre la misma; escribir en el fichero pasado como parámetro los resultados de las operaciones.

Podéis ampliar la imformación en este video: 	[Decoradores & Parámetros](https://youtu.be/_IwlE3Z7U04 “Cómo utilizar decoradores con parámetros”)


---
---
---