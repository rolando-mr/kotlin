# Curso Básico de Kotlin



## 📚 Módulo 1. Bienvenida e introducción

- ### Clase 1. ¿Por qué debo aprender Kotlin?

  **Kotlin** es uno de los lenguajes oficiales que **Google** ha adoptado como parte de la familia de lenguajes de programación para desarrollar con **Android**. Kotlin fue desarrollado desde el año 2010 gracias a JetBrains y su primera versión fue liberada en el año 2016.

  **Kotlin** es:

  - **Conciso**: reduce código a diferencia de Java.
  - **Seguro**: Kotlin tiene un método para evitar las excepciones así como para manejar las *NullPointerException*.
  - **Interoperable**: **Kotlin** al ser creado por **JetBrains** lo decidieron hacer basado en la máquina virtual de Java, es decir puedes trabajar con **Java** y **Kotlin** en una aplicación ya que comparten la misma máquina virtual.
  - **Versátil**: podemos aplicarlo en diferentes tipos de aplicaciones. Del lado del servidor con *Kotlin Server Side - Ktor*, del lado *Mobile Android* y del lado web con *KotlinJS*.

  **Java** usa *javac* y **Kotlin** usa *kotlinc* ambos al ser compilado se transforman en código **ByteCode** que es el código que lee la máquina virtual de **Java** (*Java Virtual Machine*)

  ![Cómo funciona Java](https://i.imgur.com/4MO24Rq.png)

- ### Clase 2. Mi primer programa en Kotlin

  Para empezar a trabajar con Kotlin se necesita:

  - El JDK de Java
  - IntelliJ Idea (Integra por defecto el compilador de Kotlin)

  La extensión de archivo de Kotlin es ``.kt``

  #### Función main en Kotlin

  ````kotlin
  fun main(args: Array<String>) {
      println("Hello World!")
  }
  ````


## 📚 Módulo 2. Conceptos básicos

- ### Clase 3. Variables vs. Objetos

  #### Variable

  Espacio que se reserva en memoria para guardar un sólo dato.

  #### Objetos

  Son un espacio en memoria un poco más complejo, pues puede componerse de múltiples variables y/o objetos, métodos, etc.

  En Kotlin todo es un objeto, se tratan de evitar los tipos de datos primitivos por lo que *no se deben declarar valores primitivos en Kotlin*. No obstante cuando no se usa un elemento como un objeto Kotlin lo toma como un primitivo, **por ejemplo:**

  ````kotlin
  var i = 10
  i = i * 2
  println(i)
  ````

  Kotlin utiliza *Wrappers* para los números, a esto se le conoce como **Boxing**.

  #### Operadores

  Dado que en Kotlin hay que procurar como buena práctica que todo sea un objeto hay una serie de métodos que cumplen la misma función que los operadores de los tipos primitivos:

  ![métodos](https://i.imgur.com/VKJkrin.png)

  ![métodos 2](https://i.imgur.com/xcDrb3q.png)

  ![métodos 3](https://i.imgur.com/HYUswRU.png)


- ### Clase 4. Operadores en Kotlin

  ````kotlin
  val a = 4 // Declarar una variable. 
  a.plus(b) // Ejecutar métodos. plus() → Método para sumar
  ````

  Aunque aparentemente ``a`` es una variable, Kotlin internamente trata esa variable como un objeto, por eso se pueden ejecutar métodos sobre ``a``.

  Es recomendable usar los métodos para hacer operaciones en lugar de usar operadores, esto es porque los métodos están mejor optimizados y permiten tener manejar de forma más eficiente hilos y coroutines.

- ### Clase 5.  Otros Operadores en Kotlin

  #### Operadores unarios

  Aplicar la ley de signos, permitiendo convertir un número positivo en negativo y viceversa.

  ````kotlin
  var a = -2
  var b = a.unaryMinus()
  println("b: $b")
  
  /* Esto imprimirá:
  b: 2 
  Porque (-) por (-) es (+)
  */
  ````

  **🛈 Nota:** También se pueden crear variables usando la palabra reservada ``var``

  #### Operador de negación

  Funciona con datos lógicos, este simplemente negará el dato establecido.

  ````kotlin
  var a = true
  var b = a.not()
  println("b: $b")
  
  // Esto imprimirá:
  B: FALSE
  ````

  Al utilizar datos lógicos, la función not() no será la única que se puede usar, hay otras opciones como se muestra en la figura:

  ![Otros operadores lógicos en Kotlin](https://i.imgur.com/PE51l60.jpg)

  #### Operador incremento y decremento

  Permiten incrementar o decrementar el valor de la variable en 1. Puede aplicarse pre-incremento/decremento y post-incremento/decremento.

  #### Operadores de equidad

  Permiten comparar si un dato es igual, o mayor, o mayor e igual que otro, etc. su resultado será un valor lógico. Estos pueden ser utilizados en los  controladores de flujo como if, when, for, while etc.

- ### Clase  6. Tipos de variables: var, val y const

  Hay 2 Tipos de variables en Kotlin: *changeales*(que se valor puede cambiar) y *unchangeables*(su valor no puede cambiar).

  ##### Changeables

  - ##### var

  #### Unchangeables

  En el caso de Kotlin es recomendable usar más este tipo de variables. Esto se debe a que Kotlin obedece mucho a los principios de la programación funcional, y uno de esos principios es la inmutabilidad.

  - ##### val

    El valor se puede determinar en tiempo de ejecución.

  - ##### const

    El valor se determina en tiempo de compilación.

- ### Clase 7. Ejercicio var val const

  #### var

  No es una buena práctica usar ``var``, usarlo sólo si es estrictamente necesario y las necesidades del programa lo requieran. Si ese es el caso hay que usar este tipo de variables sólo como **locales a un método**, nunca de manera global.

  ````kotlin
  var n = 3 // Declarar una variable con var
  ````

  **🛈 Nota:** no es una buena práctica usar ``var`` en variables globales, pues esto interfiere con el concepto de *funciones puras* que son funciones que no pueden ser alteradas y además al ser de scope global y a la vez una variable cuyo valor puede ser alterado en cualquier momento se provoca que el código sea vulnerable y que el resultado de la ejecución del mismo sea arbitrario.

  #### val

  ````kotlin
  val name = args[0]
  ````

  En las variables de tipo ``val`` el valor se asigna durante la ejecución del código

  ``val`` es ampliamente usado en variables de scope local

  #### const

  No se usa para definir variables locales pues su uso más extendido es la definición de variables globales. Al ser una constante, por convención el nombre de la variable se escribe  en mayúsculas. 

  ````java
  const val N = "NAME" // const val es el equivalente a final static en Java
  ````

- ### Clase 8.  Programación Funcional: Funciones Puras e Inmutabilidad

  #### Programación funcional

  Es un paradigma de programación, en el que se trabaja de una forma más declarativa preocupándose más por el **qué** que por el **cómo**.

  En este paradigma se usan funciones todo el tiempo, en parámetros de otras funciones, asignadas a variables, etc. También tiene la peculiaridad de romper con la mayoría de los conceptos conocidos de la programación, se dejan de usar variables en favor de las **constantes** y la **inmutabilidad**, se cambian los bucles ``for``, ``while``, ``do while``, etc, por la **recursividad**. Además debido al uso extendido de las funciones estas deben ser **puras** por definición.

  #### Funciones puras

  Una función pura, deberá cumplir con dos cosas específicamente:

  1. Dados los mismos parámetros de entrada la función debe retornar siempre el mismo valor.
  2. La función no debe tener efectos colaterales, es decir no debe haber  nada en el entorno que la altere. Como por ejemplo, variables globales.

  #### Inmutabilidad

  Se fomenta el uso de **constantes** sobre las variables cuyo valor puede ser alterado.

  La inmutabilidad es uno de los principios de la programación funcional  donde nos promueve la ausencia de estado mutable o también conocido como **Stateless**.

  #### Estado

  Es cualquier dato que se pueda guardar y modificar posteriormente en memoria

  - Una variable
  - Un archivo
  - Un socket

  Para el caso de las variables en Kotlin es una buena práctica declararlas como ``val`` en vez de ``var``.
   Lo ideal es nunca tener variables de tipo ``var`` declaradas de manera **global** pues estas van en contra de la inmutabilidad, aunque a veces es  complicado prescindir de ellas en el resto del programa. Su mejor lugar  es cuando están declaradas de manera local al método.

- ### Clase 9.  Strings

  Kotlin **no es estrictamente tipado**, por lo que no hay que no hay que poner explícitamente el tipo de dato, pues Kotlin puede inferirlo en base a los datos de la  variable.

  ````kotlin
  val name = "Andrés López" // Tipo de dato inferido por Kotlin
  val apellido: String = "López" // Tipo de dato definido explícitamente → String
  val x: Int = 4 // Tipo de dato → Int (entero)
  
  println("Tu nombre es $nombre") // Imprimir variable. $nombre → permite poner variables en un String. La concatenación con + también funciona en Kotlin
  
  ````

  **🛈 Nota:** definir los tipos de datos es una buena práctica en la programación funcional.

  #### Párrafos

  En Kotlin se pueden usar los **raw strings** para crear párrafos, su sintaxis es la siguiente:

  ````kotlin
  val paragraph = """
  	Texto
  	Un poco más de texto
  	Aún más texto :v
  """.trimIndent()
  // .trimIndent() → Se usa para que se respete la indentación y los saltos de línea en el texto
  ````

  Limpiar el texto

  ````kotlin
  val paragraph = """
  	** Texto
  	** Un poco más de texto
  	** Aún más texto :v
  """.trimIndent()
  
  println(paragraph.trimMargin("** ")) // Quita el patrón al inicio de cada línea
  ````

  #### Caracteres especiales

  - **\t :** Tabular
  -  **\b :** Retrocede el cursor de texto 1 carácter
  - **\n :** Crea un salto de línea
  - **\r :** Mueve el cursor de texto al inicio de la línea en la que está
  - **\’, ", \ y $ :** Permite usar los caracteres que hay luego del \ dentro de las comillas sin conflictos

- ### Clase 10. Conversión de tipos de datos

  En Kotlin asignar un tipo de dato menor a uno mayor produce un error. Para evitar esto hay que usar una serie de métodos que Kotlin proporciona para las conversiones entre tipos de datos:

  - **toByte()**
  - **toShort()**
  - **toInt()**
  - **toLong()**
  - **toFloat()**
  - **toDouble()**
  - **toChar()**

  **Ejemplo:**

  ````kotlin
  var a: Int = 5
  var b: Long = a.toLong() // Convertir de Int a Long
  ````

  Las posibles conversiones que se pueden hacer en Kotlin son las siguientes:

  ![Conversiones de tipos de datos posibles en Kotlin](https://i.imgur.com/7vK6V5f.jpg)

- ### Clase 11. Rangos

  Es un operador que permite imprimir una secuencia de caracteres en una sintaxis muy simple.

  ````kotlin
  // Imprimir los números del 1 al 100
  val oneToHundred: IntRange = 1..100
  for (i in oneToHundred) {
      println(i)
  }
  
  // Imprimir letras de la A a la Z
  val aToZ: CharRange = 'A'..'Z'
  for (letter in aToZ) {
      println(letter)
  }
  ````

  Los rangos son muy útiles para crear listados, numeraciones, índices, etc.

- ### Clase 12. If y when en Kotlin

  #### If

  ````kotlin
  val number = 2
  if (number != 2) {
      println("number es diferente de 2")
  }
  
  // Si se trata a la variable como un objeto
  if (number.equals(2)) {
      println("number es igual a 2")
  }
  ````

  #### When

  Es similar a ``switch`` en otros lenguajes de programación. Se suele usar mucho en rangos.

  ````kotlin
  when(number) {
      in 1..5 -> println("Si esta entre 1 y 5") // Evalua si el valor de un avariable esta dentro de un rango
      in 1..3 -> println("Si esta entre 1 y 3")
      !in 5..10 -> println("No esta entre 5 y 10") // ! → Niega este caso
      else -> println("No esta en ninguno de los anteriores") // Es el equivalente al default en otros lenguajes
  }
  ````

  **🛈 Nota:** al usar ``when`` a diferencia de ``switch`` cuando se cumple un cosa se deja de evaluar los demás, como si en cada caso de definiera un break para romper el flujo del programa.

  Hay que tener en cuanta que si bien ``when`` se usa mucho en rangos, este [no es su único uso posible](https://kotlinlang.org/docs/reference/basic-syntax.html#using-when-expression). **Ejemplo:**

  ````kotlin
  fun describe(obj: Any): String =
      when (obj) {
          1          -> "One"
          "Hello"    -> "Greeting"
          is Long    -> "Long"
          !is String -> "Not a string"
          else       -> "Unknown"
      }
  ````

  Además ``when`` puede evaluar varias condiciones simultáneamente

  ````kotlin
  when (x) {
      0, 1 -> print("x == 0 or x == 1")
      else -> print("otherwise")
  }
  ````

   Es posible usar ``when`` **como un reemplazo de una sentencia if-else if**


  ```kotlin
  when {
      x.isOdd() -> print("x is odd")
      y.isEven() -> print("y is even")
      else -> print("x+y is odd.")
  }
  ```
  Y también para **validar peticiones HTTP**
  _Esto es partir de Kotlin v1.3_

  ```kotlin
  fun Request.getBody() =
  	when (val response = executeRequest()) {
          is Success -> response.body
          is HttpError -> throw HttpException(response.status)
  	}
  ```

- ### Clase 13. Bucles while y  do while

  #### While
  
  ````kotlin
  var i = 1
  while (i <= 10) {
      println("i = $i")
      i++
  }
  ````
  
  #### Do While
  
  ````kotlin
  i = 1
  do {
      println("i = $i")
      i++
  } while (i <= 10)
  ````
  
- ### Clase 14. Ciclos for y foreach en Kotlin

  #### For

  ````kotlin
  val daysOfWeek = listOf("Domingo","Lunes","Martes","Miercoles","Jueves","Viernes","Sabado")
  for(day in daysOfWeek){
          println(day)
  }
  ````

  Si se quiere tener acceso al índice de cada elemento del Array la sintaxis es la siguiente:

  ````kotlin
  for((index,day) in daysOfWeek.withIndex()){
          println("$index :$day")
  }
  ````

  #### Foreach

  También permite recorrer una lista con múltiples elementos pero usando una sintaxis más simple:

  ````kotlin
  val daysOfWeek = listOf("Domingo","Lunes","Martes","Miercoles","Jueves","Viernes","Sabado")
  daysOfWeek.forEach{
          println(it)
  }
  ````

  `it` será el iterador que contiene cada elemento de la lista mientras es recorrida.

  También se puede usar ``forEachIndexed`` para obtener acceso a los índices:

  ````kotlin
  daysOfWeek.forEachIndexed { index, s -> println(“Index $index: $s”) }
  ````

  **🛈 Nota:** un ciclo ``for`` es 10x más rápido que uno ``foreach``.

  #### Conclusiones de rendimiento

  - **Si es para un rango es mejor usar For**
  - **Si es para una colección (sequence, list, set) es mejor foreach**
  - **Si se va a usar break y continue es mejor For**

- ### Clase 15. Break, Continue y Labels

  #### break

  Permite interrumpir el código cuando se cumpla una condición.

  **Ejemplo:**

  ````kotlin
  for (i in 1..3) {
          println("\ni: $i ")
          for (j in 1..5) {
              if (j.equals(3)) break // Termina el ciclo más cercano
              println("j: $j")
          }
  }
  ````

  #### continue

  Permite  omitir iteraciones de un ciclo cuando se cumpla una condición

  ````kotlin
  for (i in 1..3) {
          println("\ni: $i ")
          for (j in 1..5) {
              if (j.equals(3)) continue // Va a la siguiente línea de código del ciclo más cercano.
              println("j: $j")
          }
  }
  ````

  #### Labels

  Sirven para controlar mejor los saltos y **definir en qué ciclo queremos que inicie después de saltar.** Permiten "etiquetar" por así decirlo el ciclo especifico al que se quiere aplicar ``break`` o ``continue``. Son particularmente útiles cuando se tienen ciclos anidados.

  La sintaxis para **crear** un label es: ``nombre@``

  La sintaxis para **llamar** a un label es: ``break/continue@nombre``

  **Ejemplos:**

  - ##### break y label

    ````kotlin
    terminarTodoCiclo@ for (i in 1..3) {
        println("\ni: $i ")
        for (j in 1..3) {
            println("\nj: $j")
            for (k in 1..5) {
                if (k.equals(3)) break@terminarTodoCiclo
                println("k: $k")
            }
        }
    }
    ````

  - ##### break y continue

    ````kotlin
    escaparJ@ for (i in 1..3) {
        println("\ni: $i ")
        for (j in 1..3) {
            println("\nj: $j")
            for (k in 1..5) {
                if (k.equals(3)) continue@escaparJ
                println("k: $k")
            }
        }
    }
    ````

- ### Clase 16. Valores Nulos y Double Bang

  La *"nada"* es un concepto ligado al lenguaje natural, en  el caso de Kotlin lo más cercano para representar nada es un valor *nulo*.

  **🛈 Nota:** es una práctica inicializar las variables y no dejarlas como valores nulos.

  Kotlin es **Null Safety** lo que significa que previene las indeterminaciones que causan los ``NullPointerExeptions``. Por defecto **ningún valor puede ser nulo** pues esto marcará un error. Kotlin evita que una excepción sea lanzada pues esto provoca vulnerabilidades.

  No obstante habrá ocasiones en las que se necesite forzosamente trabajar con valores nulos. En ese caso Kotlin ofrece una sintaxis especial para ello.

  ````kotlin
  val foo: Int? // ? → Permite que la variaable sea Null Saftly, es decir que no se lance una excepción por ser un valor nulo 
  foo?.metodo()
  ````

  ####  Double bang

  Es un operador que permite manejar una excepción. Si por ejemplo se tiene un valor nulo este operador va a forzar que se lance la excepción.

  ````kotlin
  var msg: String?
  msg = null
  println(msg!!.length) // !! → Operador Double bang
  ````

  **🛈 Nota:** el operador *double bang* se rara vez en el flujo de desarrollo profesional con Kotlin. **No se recomienda usarlo**, pues esto se considera una mala práctica.

- ### Clase 17. Operador Elvis

  Una de las comparaciones más comunes en la programación es la siguiente:

  ````kotlin
  if (list != null) return list.size
  else return 0
  ````

  Lo anterior es una evaluación en la que si un elemento no es ``null`` se retorna alguna operación sobre dicho elemento, de lo contrario se retorna 0.

  Usando el operador Elvis(``?:``) la sintaxis de la anterior se resumiría así:

  ````kotlin
  it.listFiles()?.size ?: 0
  ````

- ### Clase 18. Ejercicios con Null safety y operador Elvis

  #### Doubel bang

  ````kotlin
  // Siempre que se use !! se DEBE manejat la excepción con un try/cath
  try {
      var compute: String?
      compute = null
      var longitud: Int = compute!!.length
  } catch (e: NullPointerException) {
      println("Ingresa un valor, no aceptamos nulos")
  }
  ````

  #### Llamada segura

  Evitar que salte una excepción

  ````kotlin
  val compute: String? = null
  val longitud: Int? = compute?.length
  println("longitud = $longitud")
  ````

  #### Operador Elvis

  ````kotlin
  val teclado: String? = null
  val longitudTeclado: Int = teclado?.length ?: 0
  println("Longitud teclado; $longitudTeclado")
  ````

  #### Filtrar Nulls en un List

  ````kotlin
  val listWithNulls: List<Int?> = listOf<Int?>(7, null, null, 4)
  println("Lista con null: $listWithNulls")
  
  val listWithoutNull: List<Int> = listWithNulls.filterNotNull() // filterNotNull() → Elimina los valores null de una lista 
  println(listWithoutNull)
  ````

- ### Clase 20. ¿Qué es un Array en Kotlin?

  #### Arrays

  Son colecciones de datos que permiten múltiples datos.

  ##### Declarar Arrays

  ````kotlin
  val countries = arrayOf("India", "México", "Colombia", "Argentina", "Chile", "Perú") // Crea un array cuyo tipo de dato será inferido
  
  val days = arrayOf<String>("Lunes", "Martes", "Miércoles", "Jueves", "Sábado", "Domingo") // Crea un array de un tipo de dato especifico.
  
  val numbers = intArrayOf(1, 2, 3, 4, 5) // Crea un Array de enteros
  ````

  ##### Recorrer Arrays

  ````kotlin
  for (num in numbers) {
      println("Numbers: $num")
  }
  ````

  ##### Conocer longitud de un Array

  ````kotlin
  numbers.size
  ````

- ### Clase 21. Métodos útiles en arreglos

  #### Diferencias entre las formas de declarar Arrays

  Esta forma de declarar Arrays se usa para almacenar objetos:

  ````kotlin
  val foo = arrayOf<String>(...)
  ````

  Por el contrario esta otra forma se usa para almacenar tipos de datos primitivos:

  ````kotlin
  val bar = intArrayOf(...)
  ````

  #### Convertir un Array de objetos en un Array de tipos primitivos

  ````kotlin
  var arrayObject = arrayOf(5, 6, 7, 8)
  var intPrimitive: IntArray = arrayObject.toIntArray() // Convertir a Array de primitivos
  ````

  #### Métodos de Arrays

  ````kotlin
  val suma = arrayObject.sum() // sum() → Suma los elementos de un Array
  arrayObject = arrayObject.plus(4) // plus() → Añadir un elemento al Array
  arrayObject = arrayObject.reversedArray() // reversedArray() → Invertir un Array
  arrayObject.reverse() // Lo mismo que el anterior pero sin asignar el array modificado a una variable
  
  ````

- ### Clase 22. Expresiones vs. Valores

  En Kotlin **todo** es una **expresión**.
  
  En Kotlin **siempre** se devuelve un valor y eso incluye a las expresiones.
  
  #### Expresiones
  
  Se componen de variables y operadores que devuelven un valor.
  
  ````kotlin
  // ${} → poner expresiones
  println("x es igual a 5? ${x == 5}")
  
  // $ → poner valores
  val msg = "El valor de x es $x"
  ````
  
  Hay algunas funciones del lenguaje que so pueden ser una expresión como por ejemplo los bucles ``for`` y ``while``. De ahí en adelante todo en Kotlin puede ser una expresión (condicionales, funciones,  operaciones matemáticas, etc). 

- ### Clase 23. Funciones en Kotlin

  En Kotlin existen dos tipos de funciones:

  - Funciones provistas con Kotlin
  - Funciones declaradas por el desarrollador.

  En Kotlin una función **siempre** va a devolver un **valor**

  **🛈 Nota:** se pueden usar funciones escritas en Java dentro de Kotlin

  #### Declarar funciones en Kotlin

  ````kotlin
  fun averageNumbers(numbers: IntArray): Int {
      var sum = 0
      for (num in numbers) {
          sum += num
      }
  
      return sum / numbers.size
  }
  ````

   **🛈 Nota:** En Kotlin **Unit** es la forma de decir que una función no retorna nada. En caso de que una función si retorne algo es necesario poner el tipo de dato que se va a retornar.

  #### Llamar funciones

  ````kotlin
  averageNumbers(numbers)
  ````

- ### Clase 24. Funciones con parámetros por defecto

  Kotlin permite definir valores por defecto en las funciones (Named arguments). Estos valores se usarán en caso de que se pase ningún parámetro a la función.

  ````kotlin
  // character: Char = '=', number: Int  = 2 → Son los Named arguments
  fun evaluate(character: Char = '=', number: Int  = 2): String {
      return "$number es $character"
  }
  
  evaluate() // Al no pasarse ningún parámetro se usarán los Named arguments definidos en la declaración de la función
  evaluate('+') // Reemplaza uno de los Named arguments por '+'
  ````

- ### Clase 25. Lambdas en Kotlin

  Lambdas permite tener una nueva forma de escribir funciones. En otros lenguajes  a las lambdas se les conoce como *funciones anónimas*, *functions literals* o *funciones literales*. Las Lambdas son en esencia funciones que no tienen nombre.

  ````kotlin
  {println("Hola mundo")}() // Las sentencias de la función se ponen dentro de {...}. Luego se ponen ()
  
  // Por lo general las Lambdas se guardan dentro de una variable
  var hola = {println("Hola mundo")}()
  
  // La función se llamaría así
  hola()
  ````

  Hay otro tipo de sintaxis que se puede usar para crear funciones Lambdas

  ````kotlin
  val w = {d: Int, c: Int -> d+c} // -> separa los parámetros de las acciones de la Lambda. Al lado izquierdo se ponen los parámetros y a la derecha las acciones
  
  // Llamar a la función Lambdas
  println(w(2,3))
  
  // Aquí se define al función lambda, los parámetros que va recibir y se pasan dichos parámetros (4, 4) en una sóla línea 
  println({d: Int, c: Int -> d + c}(4, 4))
  ````


## 📚 Módulo 4. Programación Orientada a Objetos

- ### Clase  28. Clases

  En Kotlin las Clases se definen con la palabra reservada ``class``.

- ### Clase 29. Ejercicio de  Clases

  ````kotlin
  class Camera // Esta es la forma mínima de definir una Clase en Kotlin
  ````

  #### Instanciar una Clase en Kotlin

  ````kotlin
  val camera = Camera() // Crear un objeto
  
  camera.turnOn() // Ejecutar métodos
  println(camera.isOn) // Acceder a atributos
  ````

  **🛈 Nota:** ningún atributo debería poder ser modificado directamente fuera de la Clase, esto es una mala práctica

- ### Clase 30. Modificadores de acceso

  En kotlin todos los atributos son **públicos** por defecto.

  #### Modificadores de acceso en Kotlin

  - **public:** todos tienen acceso.
  - **private:** acceso sólo dentro de la Clase
  - **protected:** acceso sólo dentro de la Clase y las Clases que hereden
  - **internal:** acceso entre módulos

  #### Usar modificadores de acceso

  ````kotlin
  private var size
  ````

- ### Clase 31. Getters y Setters

  Koltlin tiene dos tipos de getters y setters:

  - **Provistos por el programador:** son métodos que son creados por el programador para acceder y/o modificar un atributo. Se usan cuando los elementos están encapsulados. **Ejemplo:**

    ````kotlin
    fun getCameraStatus(): String {
        return if (isOn) "Camera is Turned" else "Camera is not turned"
    }
    ````

  - **Acceso directo desde Kotlin:** se usan cuando los elementos no están encapsulados. Permiten definir validaciones a la asignación de los atributos para que los datos sean lo más íntegros posible a la lógica de negocio de la aplicación.

  **🛈 Nota:** algunos *getters* y *setters* podrían no existir dependiendo de los métodos que ya estén definidos dentro de la Clase.

  - ### Clase 32. El Get() y Set() propio de Kotlin

    **field:** es un tipo de  variable que toma temporalmente el atributo al que se esta haciendo un ``set()`` para que dicho atributo pueda ser alterado.

    #### Sintaxis de un set()

    ````kotlin
    var size: Int = 34
        set(value) {
            if (value >= 34)
                field = value
            else
                field = 34
        }
    ````

    **🛈 Nota:** este tipo de sintaxis se usan mucho Clases para datos, cómo por ejemplo Clases que alberguen datos traídos de una API (*Data Class*. - Clases de Datos) para así efectuar una serie de validaciones para verificar que los datos estén íntegros.

- ### Clase 33. Data class en Kotlin

  Los **Data Class** son tipos de Clases que permiten manejar datos, dichos datos pueden provenir de una fuente que no sea el código fuente del programa, como por ejemplo una API, una base de datos, etc. Los Data Class se usan para mapear esa fuente de datos y así manejar la consistencia de los atributos de esos datos.

  #### Declarar un Data Class

  ````kotlin
  data class Movie(val title: String, val creator: String, val duration: Int) // Atributos mínmos para crear la Clase {
  	// Implementación
  }
  ````

  **🛈 Nota:** si bien es posible definir Data Class dentro de otra Clase, estás sólo "vivirán temporalmente" y sólo podrán ser accedidas por la Clase que las contiene. Lo ideal es aferrarse al principio de modularidad y definir las Data Class en un archivo aparte.

- ### Clase 34. Método Constructor

  En Kotlin hay 2 tipos de constructores:

  - #### Constructor primario

    Es la forma clásica de inicializar una Clase

    ````kotlin
    class Shoe(val sku: Int, var mark: String) {
    	// Implementación   
    }
    ````

    

  - #### Constructor secundario

    Se define con el prefijo ``constructor``. 

    ````kotlin
    class Person {
        var children: MutableList<Person> = mutableListOf()
        constructor(parent: Person) {
            parent.children.add(this)
        }
    }
    ````

    

    Si la Clase en cuestión ya tiene un constructor primario, cada constructor secundario debe delegar al constructor primario, ya sea directa o indirectamente a través de otro(s) constructor(es) secundario(s). La delegación a otro constructor de la misma clase se realiza mediante la palabra reservada ``this``:

    ````kotlin
    class Person(val name: String) {
        var children: MutableList<Person> = mutableListOf()
        constructor(name: String, parent: Person) : this(name) {
            parent.children.add(this)
        }
    }
    ````

    

  En Kotlin además también se cuenta con otro elemento:

  - #### Bloque de Inicialización (initializer blocks)

    Alberga el código de inicialización. Se ejecuta cuando se construya la Clase y permite definir el código que se quiere ejecutar cuando se cree la Clase.

    ````kotlin
    init {
    	// Implementación    
    }
    ````

- ### Clase 35. Herencia y polimorfismo

  **Todas** las Clases de Kotlin heredan de la Clase ``Any``.

  #### Definir herencia en Kotlin

  ````kotlin
  class Subclase : Superclase {
      // Implementación
  }
  ````

  #### Polimorfismo en Kotlin
  
  ````kotlin
  override fun toString(): String {
  	return "SKU ID: $SKU\nMARK: $mark\nMODEL: $model\nCOLOR: $color\nSIZE: $size
  }
  ````

- ### Clase 36. Aplicando herencia y polimorfismo

  En Kotlin por defecto no se puede heredar una Clase. Esto se debe a que por defecto las Clases en Kotlin están **cerradas**. Para "abrir" una Clase se usa la siguiente sintaxis:

  ````kotlin
  open class Product
  ````

  #### Aplicando herencia

  - ##### Superclase

    ````kotlin
    open class Product(var name: String, var description: String, var sku: Int) {
    	// Implementación
    }
    ````

  - ##### Subclase

    ````kotlin
    class Shoe(sku: Int, var mark: String, name: String, description: String): Product(name, description, sku) {
        // Implementación
    }
    ````

    Como el constructor de la superclase tiene parámetros definidos es necesario pasar también dichos parámetros al aplicar al herencia, sólo que en este caso no llevaran tipo de dato ni la palabra  reservada para declarar variables: ``: Product(name, description, sku)``.

    Además también es necesario indicar dichos parámetros en el constructor de la subclase, en este caso si se declararán como variables y llevarán su respectivo tipo de dato en caso de ser necesario: ``class Shoe(sku: Int, var mark: String, name: String, description: String):``

    **🛈 Nota:** en Kotlin los métodos de una clase también están cerrados por defecto, por lo que si se quiere sobrescribir un método hay que poner el prefijo ``open`` en su definición para hacerlo "abierto" y poder sobrescribirlo.
    
    ````kotlin
    open fun create(): String {
        // Implementación
    }
    ````
    
    Para acceder a métodos/atributos de la super clase se usa la palabra reservada ``super``.
    
    ````kotlin
    override fun toString(): String {
        return super.toString() + "SKU ID: $sku\nBRAND: $brand\nMODEL: $model\nCOLOR: $color\nSIZE: $size"
    }
    ````
  
- ### Clase 37. Clases abstractas

  Son Clases que **no tienen implementación**. No se pueden crear instancias de este tipo de Clases.

  Las Clases Abstractas se define con el prefijo ``abstract``.

  ````kotlin
  abstract class Product
  ````

  Este tipo de Clases pueden contener **métodos abstractos**, que son métodos que no tienen cuerpo y que tienen que implementarse obligatoriamente en las subclases, y también pueden contener métodos normales cuya implementación es opcional.

  **Ejemplo de método abstracto:**

  ````kotlin
  abstract fun create(): String
  ````

- ### Clase 38. Interfaces

  - Las **interfaces** se centran en las acciones/métodos que se repiten entre clases. Los métodos que se definen en una interfaz pueden implementarse en cualquier Clase independientemente de su familia o jerarquía.

  - Por lo general se nombran con una ``I`` como prefijo o ``able`` como sufijo.

    Las **Clases Abstractas** por el contrario se centran en los atributos/propiedades redundantes entre Clases. Se heredan de forma lineal al igual que cualquier otra Clase.

  #### Implementar una Interfaz

  ````kotlin
  class Shoe(sku: Int, var brand: String, name: String, description: String): Product(name, description, sku), ICrudActions {
      // Implementación
  }
  ````

  **🛈 Nota:** una Clase puede implementar tantas interfaces como sea posible. Además las Interfaces también pueden albergar métodos con implementación y no sólo métodos sin cuerpo.

## 📚 Módulo 5. Programación Funcional

- ### Clase 40. Funciones de orden superior

  Son funciones que **reciben como parámetro otras funciones.** 

  #### Declarar funciones de orden superior

  ````kotlin
  fun foo(var1, function): String { // var1 → Datos para la función que se pasa cómo parámetro. function → Función que se pasa como parámetro.
      return function(var1)
  }
  ````

  Algunas funciones de orden superior pueden no contener datos para su ejecución (``var1`` en el ejemplo anterior).

  También es común que las funciones de orden superior reciban una Lambda por parámetro.

  ````kotlin
  fun foo(var1, {... -> ...}): String {
  	return ...    
  }
  ````

  El objetivo de las funciones de orden superior que pueda reutilizar la estructura que se le define muchas veces

  #### Llamar a una función de orden superior.

  ````kotlin
  foo(3, "hola", ::function) // 3, "hola" → Datos para la función que se pasa cómo parámetro. function → Función que se pasa como parámetro.
  ````

- ### Clase 41. Una función como parámetro

  **Ejemplo de una función de orden superior:**

  Para empezar se declara la función de orden superior.

  ````kotlin
  fun calculator(a: Int, b: Int, c: Int, operation: (Int, Int, Int) -> Int): Int {
      return operation (a, b, c)
  }
  ````

  Se indican los parámetros (``a: Int, b: Int, c: Int``) que va a recibir la función ``operation``, esta es a su vez una función lo más genérica posible para que sea posible reutilizar su estructura. Es por eso que sólo se define que va a recibir 3 parámetros de tipo entero y va a retornar un número entero. Después se define el tipo de dato que va retornar la función  de orden superior y finalmente en el cuerpo de la función se retorna la función ``operation`` con sus respectivos parámetros.

  La estructura que se definió en la  función de orden superior puede ser reutilizada tantas veces como sea necesario en otras funciones:

  ````kotlin
  fun sum(a: Int, b: Int, c: Int) = a + b + c
  fun subtract(a: Int, b: Int, c: Int) = a - b - c
  fun multiply(a: Int, b: Int, c: Int) = a * b * c
  ````

  Las 3 funciones pueden reutilizar la función de orden superior puesto que se apegan a su estructura; reciben por parámetros 3 números enteros y retornar a su vez un número entero.

  ````kotlin
  calculator(1, 2, 3, ::multiply)
  ````

  Por último se llama a la función de orden superior, a la que gracias a su estructura genérica se le puede pasar cualquiera de las 3 funciones creadas anteriormente.

   Un ejemplo en el que se ve mucho el uso de funciones de orden superior es el desarrollo de apps Android, por ejemplo en el siguiente código:

  ````kotlin
  view.setOnClickListener({ view -> 
  	// Implementación
  })
  ````

  Otra lugar en el que se pueden ver las funciones de orden superior son los Callbacks:

  ````kotlin
  fun someRequest(callback: (Data, Int) -> Unit) {
      // Implementación
  }
  ````

- ### Clase 42. Recursividad. List

  Se pueden crear listas que contengan elementos de un mismo tipo de dato:

  ````kotlin
  val numbersInt = listOf(4,3,2)
  ````

  Pero también se pueden crear listas que almacenen elementos con diferentes tipos de datos, en este caso el tipo de dato de la lista será ``Any``.

  ````kotlin
   val mylist = listOf(4,"lala","ll",2)
  ````

  También se pueden pueden crear estructuras de clave-valor utilizando listas tipo *hashMapOf*.

  ````kotlin
  val months = hashMapOf(1 to "Enero", 2 to "Febrero", 3 to "Marzo", 4 to "Abril", 5 to "Mayo", 6 to "Junio", 7 to "Julio", 8 to "Agosto", 9 to "Septiembre" , 10 to "Octubre", 11 to "Noviembre" ,  12 to "Diciembre" )
  ````

  Para recorrer el HashMap:

  ````kotlin
  for (key in months.keys)
  	println("key:$key  value:${months[key]}")
  ````

- ### Clase 43. Recursividad. Filter

  Esta función sirve para filtrar los datos que cumplan con determinada condición en una lista. Además es un claro ejemplo de como se usan las funciones de orden  superior, recibe como parámetro un Lambda en la que se puede poner el auxiliar ``it`` para poner las acciones únicamente sin necesidad de expresar los parámetros. ``filter`` puede recibir una comparación lógica o un método.

  ````kotlin
  val numbersInt = listOf(4,3,2)
  numbersInt.filter { it % 2 == 0 }  
  
  // Este será el resultado: [4,2]
  
  val words = listOf("Oasis","Hola", "Holanda", "Objeto")
  words.filter { it.startsWith('O') }
  
  // Este será el resultado: [Oasis, Objeto]
  ````

  
