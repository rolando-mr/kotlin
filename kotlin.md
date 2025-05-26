<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Welcome file</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__left">
    <div class="stackedit__toc">
      
<ul>
<li><a href="#curso-básico-de-kotlin">Curso Básico de Kotlin</a>
<ul>
<li><a href="#📚-módulo-1.-bienvenida-e-introducción">📚 Módulo 1. Bienvenida e introducción</a></li>
<li><a href="#📚-módulo-2.-conceptos-básicos">📚 Módulo 2. Conceptos básicos</a></li>
<li><a href="#📚-módulo-4.-programación-orientada-a-objetos">📚 Módulo 4. Programación Orientada a Objetos</a></li>
<li><a href="#📚-módulo-5.-programación-funcional">📚 Módulo 5. Programación Funcional</a></li>
</ul>
</li>
</ul>

    </div>
  </div>
  <div class="stackedit__right">
    <div class="stackedit__html">
      <h1 id="curso-básico-de-kotlin">Curso Básico de Kotlin</h1>
<h2 id="📚-módulo-1.-bienvenida-e-introducción">📚 Módulo 1. Bienvenida e introducción</h2>
<ul>
<li>
<h3 id="clase-1.-¿por-qué-debo-aprender-kotlin">Clase 1. ¿Por qué debo aprender Kotlin?</h3>
<p><strong>Kotlin</strong> es uno de los lenguajes oficiales que <strong>Google</strong> ha adoptado como parte de la familia de lenguajes de programación para desarrollar con <strong>Android</strong>. Kotlin fue desarrollado desde el año 2010 gracias a JetBrains y su primera versión fue liberada en el año 2016.</p>
<p><strong>Kotlin</strong> es:</p>
<ul>
<li><strong>Conciso</strong>: reduce código a diferencia de Java.</li>
<li><strong>Seguro</strong>: Kotlin tiene un método para evitar las excepciones así como para manejar las <em>NullPointerException</em>.</li>
<li><strong>Interoperable</strong>: <strong>Kotlin</strong> al ser creado por <strong>JetBrains</strong> lo decidieron hacer basado en la máquina virtual de Java, es decir puedes trabajar con <strong>Java</strong> y <strong>Kotlin</strong> en una aplicación ya que comparten la misma máquina virtual.</li>
<li><strong>Versátil</strong>: podemos aplicarlo en diferentes tipos de aplicaciones. Del lado del servidor con <em>Kotlin Server Side - Ktor</em>, del lado <em>Mobile Android</em> y del lado web con <em>KotlinJS</em>.</li>
</ul>
<p><strong>Java</strong> usa <em>javac</em> y <strong>Kotlin</strong> usa <em>kotlinc</em> ambos al ser compilado se transforman en código <strong>ByteCode</strong> que es el código que lee la máquina virtual de <strong>Java</strong> (<em>Java Virtual Machine</em>)</p>
<p><img src="https://i.imgur.com/4MO24Rq.png" alt="Cómo funciona Java"></p>
</li>
<li>
<h3 id="clase-2.-mi-primer-programa-en-kotlin">Clase 2. Mi primer programa en Kotlin</h3>
<p>Para empezar a trabajar con Kotlin se necesita:</p>
<ul>
<li>El JDK de Java</li>
<li>IntelliJ Idea (Integra por defecto el compilador de Kotlin)</li>
</ul>
<p>La extensión de archivo de Kotlin es <code>.kt</code></p>
<h4 id="función-main-en-kotlin">Función main en Kotlin</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">main</span><span class="token punctuation">(</span>args<span class="token operator">:</span> Array<span class="token operator">&lt;</span>String<span class="token operator">&gt;</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Hello World!"</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
</ul>
<h2 id="📚-módulo-2.-conceptos-básicos">📚 Módulo 2. Conceptos básicos</h2>
<ul>
<li>
<h3 id="clase-3.-variables-vs.-objetos">Clase 3. Variables vs. Objetos</h3>
<h4 id="variable">Variable</h4>
<p>Espacio que se reserva en memoria para guardar un sólo dato.</p>
<h4 id="objetos">Objetos</h4>
<p>Son un espacio en memoria un poco más complejo, pues puede componerse de múltiples variables y/o objetos, métodos, etc.</p>
<p>En Kotlin todo es un objeto, se tratan de evitar los tipos de datos primitivos por lo que <em>no se deben declarar valores primitivos en Kotlin</em>. No obstante cuando no se usa un elemento como un objeto Kotlin lo toma como un primitivo, <strong>por ejemplo:</strong></p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> i <span class="token operator">=</span> <span class="token number">10</span>
i <span class="token operator">=</span> i <span class="token operator">*</span> <span class="token number">2</span>
<span class="token function">println</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span>
</code></pre>
<p>Kotlin utiliza <em>Wrappers</em> para los números, a esto se le conoce como <strong>Boxing</strong>.</p>
<h4 id="operadores">Operadores</h4>
<p>Dado que en Kotlin hay que procurar como buena práctica que todo sea un objeto hay una serie de métodos que cumplen la misma función que los operadores de los tipos primitivos:</p>
<p><img src="https://i.imgur.com/VKJkrin.png" alt="métodos"></p>
<p><img src="https://i.imgur.com/xcDrb3q.png" alt="métodos 2"></p>
<p><img src="https://i.imgur.com/HYUswRU.png" alt="métodos 3"></p>
</li>
<li>
<h3 id="clase-4.-operadores-en-kotlin">Clase 4. Operadores en Kotlin</h3>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> a <span class="token operator">=</span> <span class="token number">4</span> <span class="token comment">// Declarar una variable. </span>
a<span class="token punctuation">.</span><span class="token function">plus</span><span class="token punctuation">(</span>b<span class="token punctuation">)</span> <span class="token comment">// Ejecutar métodos. plus() → Método para sumar</span>
</code></pre>
<p>Aunque aparentemente <code>a</code> es una variable, Kotlin internamente trata esa variable como un objeto, por eso se pueden ejecutar métodos sobre <code>a</code>.</p>
<p>Es recomendable usar los métodos para hacer operaciones en lugar de usar operadores, esto es porque los métodos están mejor optimizados y permiten tener manejar de forma más eficiente hilos y coroutines.</p>
</li>
<li>
<h3 id="clase-5.--otros-operadores-en-kotlin">Clase 5.  Otros Operadores en Kotlin</h3>
<h4 id="operadores-unarios">Operadores unarios</h4>
<p>Aplicar la ley de signos, permitiendo convertir un número positivo en negativo y viceversa.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> a <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">2</span>
<span class="token keyword">var</span> b <span class="token operator">=</span> a<span class="token punctuation">.</span><span class="token function">unaryMinus</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"b: <span class="token interpolation variable">$b</span>"</span><span class="token punctuation">)</span>

<span class="token comment">/* Esto imprimirá:
b: 2 
Porque (-) por (-) es (+)
*/</span>
</code></pre>
<p><strong>🛈 Nota:</strong> También se pueden crear variables usando la palabra reservada <code>var</code></p>
<h4 id="operador-de-negación">Operador de negación</h4>
<p>Funciona con datos lógicos, este simplemente negará el dato establecido.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> a <span class="token operator">=</span> <span class="token boolean">true</span>
<span class="token keyword">var</span> b <span class="token operator">=</span> a<span class="token punctuation">.</span><span class="token function">not</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"b: <span class="token interpolation variable">$b</span>"</span><span class="token punctuation">)</span>

<span class="token comment">// Esto imprimirá:</span>
B<span class="token operator">:</span> FALSE
</code></pre>
<p>Al utilizar datos lógicos, la función not() no será la única que se puede usar, hay otras opciones como se muestra en la figura:</p>
<p><img src="https://i.imgur.com/PE51l60.jpg" alt="Otros operadores lógicos en Kotlin"></p>
<h4 id="operador-incremento-y-decremento">Operador incremento y decremento</h4>
<p>Permiten incrementar o decrementar el valor de la variable en 1. Puede aplicarse pre-incremento/decremento y post-incremento/decremento.</p>
<h4 id="operadores-de-equidad">Operadores de equidad</h4>
<p>Permiten comparar si un dato es igual, o mayor, o mayor e igual que otro, etc. su resultado será un valor lógico. Estos pueden ser utilizados en los  controladores de flujo como if, when, for, while etc.</p>
</li>
<li>
<h3 id="clase--6.-tipos-de-variables-var-val-y-const">Clase  6. Tipos de variables: var, val y const</h3>
<p>Hay 2 Tipos de variables en Kotlin: <em>changeales</em>(que se valor puede cambiar) y <em>unchangeables</em>(su valor no puede cambiar).</p>
<h5 id="changeables">Changeables</h5>
<ul>
<li>
<h5 id="var">var</h5>
</li>
</ul>
<h4 id="unchangeables">Unchangeables</h4>
<p>En el caso de Kotlin es recomendable usar más este tipo de variables. Esto se debe a que Kotlin obedece mucho a los principios de la programación funcional, y uno de esos principios es la inmutabilidad.</p>
<ul>
<li>
<h5 id="val">val</h5>
<p>El valor se puede determinar en tiempo de ejecución.</p>
</li>
<li>
<h5 id="const">const</h5>
<p>El valor se determina en tiempo de compilación.</p>
</li>
</ul>
</li>
<li>
<h3 id="clase-7.-ejercicio-var-val-const">Clase 7. Ejercicio var val const</h3>
<h4 id="var-1">var</h4>
<p>No es una buena práctica usar <code>var</code>, usarlo sólo si es estrictamente necesario y las necesidades del programa lo requieran. Si ese es el caso hay que usar este tipo de variables sólo como <strong>locales a un método</strong>, nunca de manera global.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> n <span class="token operator">=</span> <span class="token number">3</span> <span class="token comment">// Declarar una variable con var</span>
</code></pre>
<p><strong>🛈 Nota:</strong> no es una buena práctica usar <code>var</code> en variables globales, pues esto interfiere con el concepto de <em>funciones puras</em> que son funciones que no pueden ser alteradas y además al ser de scope global y a la vez una variable cuyo valor puede ser alterado en cualquier momento se provoca que el código sea vulnerable y que el resultado de la ejecución del mismo sea arbitrario.</p>
<h4 id="val-1">val</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> name <span class="token operator">=</span> args<span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span>
</code></pre>
<p>En las variables de tipo <code>val</code> el valor se asigna durante la ejecución del código</p>
<p><code>val</code> es ampliamente usado en variables de scope local</p>
<h4 id="const-1">const</h4>
<p>No se usa para definir variables locales pues su uso más extendido es la definición de variables globales. Al ser una constante, por convención el nombre de la variable se escribe  en mayúsculas.</p>
<pre class=" language-java"><code class="prism  language-java"><span class="token keyword">const</span> val N <span class="token operator">=</span> <span class="token string">"NAME"</span> <span class="token comment">// const val es el equivalente a final static en Java</span>
</code></pre>
</li>
<li>
<h3 id="clase-8.--programación-funcional-funciones-puras-e-inmutabilidad">Clase 8.  Programación Funcional: Funciones Puras e Inmutabilidad</h3>
<h4 id="programación-funcional">Programación funcional</h4>
<p>Es un paradigma de programación, en el que se trabaja de una forma más declarativa preocupándose más por el <strong>qué</strong> que por el <strong>cómo</strong>.</p>
<p>En este paradigma se usan funciones todo el tiempo, en parámetros de otras funciones, asignadas a variables, etc. También tiene la peculiaridad de romper con la mayoría de los conceptos conocidos de la programación, se dejan de usar variables en favor de las <strong>constantes</strong> y la <strong>inmutabilidad</strong>, se cambian los bucles <code>for</code>, <code>while</code>, <code>do while</code>, etc, por la <strong>recursividad</strong>. Además debido al uso extendido de las funciones estas deben ser <strong>puras</strong> por definición.</p>
<h4 id="funciones-puras">Funciones puras</h4>
<p>Una función pura, deberá cumplir con dos cosas específicamente:</p>
<ol>
<li>Dados los mismos parámetros de entrada la función debe retornar siempre el mismo valor.</li>
<li>La función no debe tener efectos colaterales, es decir no debe haber  nada en el entorno que la altere. Como por ejemplo, variables globales.</li>
</ol>
<h4 id="inmutabilidad">Inmutabilidad</h4>
<p>Se fomenta el uso de <strong>constantes</strong> sobre las variables cuyo valor puede ser alterado.</p>
<p>La inmutabilidad es uno de los principios de la programación funcional  donde nos promueve la ausencia de estado mutable o también conocido como <strong>Stateless</strong>.</p>
<h4 id="estado">Estado</h4>
<p>Es cualquier dato que se pueda guardar y modificar posteriormente en memoria</p>
<ul>
<li>Una variable</li>
<li>Un archivo</li>
<li>Un socket</li>
</ul>
<p>Para el caso de las variables en Kotlin es una buena práctica declararlas como <code>val</code> en vez de <code>var</code>.<br>
Lo ideal es nunca tener variables de tipo <code>var</code> declaradas de manera <strong>global</strong> pues estas van en contra de la inmutabilidad, aunque a veces es  complicado prescindir de ellas en el resto del programa. Su mejor lugar  es cuando están declaradas de manera local al método.</p>
</li>
<li>
<h3 id="clase-9.--strings">Clase 9.  Strings</h3>
<p>Kotlin <strong>no es estrictamente tipado</strong>, por lo que no hay que no hay que poner explícitamente el tipo de dato, pues Kotlin puede inferirlo en base a los datos de la  variable.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> name <span class="token operator">=</span> <span class="token string">"Andrés López"</span> <span class="token comment">// Tipo de dato inferido por Kotlin</span>
<span class="token keyword">val</span> apellido<span class="token operator">:</span> String <span class="token operator">=</span> <span class="token string">"López"</span> <span class="token comment">// Tipo de dato definido explícitamente → String</span>
<span class="token keyword">val</span> x<span class="token operator">:</span> Int <span class="token operator">=</span> <span class="token number">4</span> <span class="token comment">// Tipo de dato → Int (entero)</span>

<span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Tu nombre es <span class="token interpolation variable">$nombre</span>"</span><span class="token punctuation">)</span> <span class="token comment">// Imprimir variable. $nombre → permite poner variables en un String. La concatenación con + también funciona en Kotlin</span>

</code></pre>
<p><strong>🛈 Nota:</strong> definir los tipos de datos es una buena práctica en la programación funcional.</p>
<h4 id="párrafos">Párrafos</h4>
<p>En Kotlin se pueden usar los <strong>raw strings</strong> para crear párrafos, su sintaxis es la siguiente:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> paragraph <span class="token operator">=</span> <span class="token raw-string string">"""
	Texto
	Un poco más de texto
	Aún más texto :v
"""</span><span class="token punctuation">.</span><span class="token function">trimIndent</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token comment">// .trimIndent() → Se usa para que se respete la indentación y los saltos de línea en el texto</span>
</code></pre>
<p>Limpiar el texto</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> paragraph <span class="token operator">=</span> <span class="token raw-string string">"""
	** Texto
	** Un poco más de texto
	** Aún más texto :v
"""</span><span class="token punctuation">.</span><span class="token function">trimIndent</span><span class="token punctuation">(</span><span class="token punctuation">)</span>

<span class="token function">println</span><span class="token punctuation">(</span>paragraph<span class="token punctuation">.</span><span class="token function">trimMargin</span><span class="token punctuation">(</span><span class="token string">"** "</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token comment">// Quita el patrón al inicio de cada línea</span>
</code></pre>
<h4 id="caracteres-especiales">Caracteres especiales</h4>
<ul>
<li><strong>\t :</strong> Tabular</li>
<li><strong>\b :</strong> Retrocede el cursor de texto 1 carácter</li>
<li><strong>\n :</strong> Crea un salto de línea</li>
<li><strong>\r :</strong> Mueve el cursor de texto al inicio de la línea en la que está</li>
<li><strong>\’, ", \ y $ :</strong> Permite usar los caracteres que hay luego del \ dentro de las comillas sin conflictos</li>
</ul>
</li>
<li>
<h3 id="clase-10.-conversión-de-tipos-de-datos">Clase 10. Conversión de tipos de datos</h3>
<p>En Kotlin asignar un tipo de dato menor a uno mayor produce un error. Para evitar esto hay que usar una serie de métodos que Kotlin proporciona para las conversiones entre tipos de datos:</p>
<ul>
<li><strong>toByte()</strong></li>
<li><strong>toShort()</strong></li>
<li><strong>toInt()</strong></li>
<li><strong>toLong()</strong></li>
<li><strong>toFloat()</strong></li>
<li><strong>toDouble()</strong></li>
<li><strong>toChar()</strong></li>
</ul>
<p><strong>Ejemplo:</strong></p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> a<span class="token operator">:</span> Int <span class="token operator">=</span> <span class="token number">5</span>
<span class="token keyword">var</span> b<span class="token operator">:</span> Long <span class="token operator">=</span> a<span class="token punctuation">.</span><span class="token function">toLong</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// Convertir de Int a Long</span>
</code></pre>
<p>Las posibles conversiones que se pueden hacer en Kotlin son las siguientes:</p>
<p><img src="https://i.imgur.com/7vK6V5f.jpg" alt="Conversiones de tipos de datos posibles en Kotlin"></p>
</li>
<li>
<h3 id="clase-11.-rangos">Clase 11. Rangos</h3>
<p>Es un operador que permite imprimir una secuencia de caracteres en una sintaxis muy simple.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token comment">// Imprimir los números del 1 al 100</span>
<span class="token keyword">val</span> oneToHundred<span class="token operator">:</span> IntRange <span class="token operator">=</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">100</span>
<span class="token keyword">for</span> <span class="token punctuation">(</span>i <span class="token keyword">in</span> oneToHundred<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span>
<span class="token punctuation">}</span>

<span class="token comment">// Imprimir letras de la A a la Z</span>
<span class="token keyword">val</span> aToZ<span class="token operator">:</span> CharRange <span class="token operator">=</span> <span class="token string">'A'</span><span class="token operator">..</span><span class="token string">'Z'</span>
<span class="token keyword">for</span> <span class="token punctuation">(</span>letter <span class="token keyword">in</span> aToZ<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span>letter<span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Los rangos son muy útiles para crear listados, numeraciones, índices, etc.</p>
</li>
<li>
<h3 id="clase-12.-if-y-when-en-kotlin">Clase 12. If y when en Kotlin</h3>
<h4 id="if">If</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> number <span class="token operator">=</span> <span class="token number">2</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span>number <span class="token operator">!=</span> <span class="token number">2</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"number es diferente de 2"</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>

<span class="token comment">// Si se trata a la variable como un objeto</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span>number<span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"number es igual a 2"</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="when">When</h4>
<p>Es similar a <code>switch</code> en otros lenguajes de programación. Se suele usar mucho en rangos.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">when</span><span class="token punctuation">(</span>number<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span> <span class="token operator">-&gt;</span> <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Si esta entre 1 y 5"</span><span class="token punctuation">)</span> <span class="token comment">// Evalua si el valor de un avariable esta dentro de un rango</span>
    <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">3</span> <span class="token operator">-&gt;</span> <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Si esta entre 1 y 3"</span><span class="token punctuation">)</span>
    <span class="token operator">!</span><span class="token keyword">in</span> <span class="token number">5</span><span class="token operator">..</span><span class="token number">10</span> <span class="token operator">-&gt;</span> <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"No esta entre 5 y 10"</span><span class="token punctuation">)</span> <span class="token comment">// ! → Niega este caso</span>
    <span class="token keyword">else</span> <span class="token operator">-&gt;</span> <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"No esta en ninguno de los anteriores"</span><span class="token punctuation">)</span> <span class="token comment">// Es el equivalente al default en otros lenguajes</span>
<span class="token punctuation">}</span>
</code></pre>
<p><strong>🛈 Nota:</strong> al usar <code>when</code> a diferencia de <code>switch</code> cuando se cumple un cosa se deja de evaluar los demás, como si en cada caso de definiera un break para romper el flujo del programa.</p>
<p>Hay que tener en cuanta que si bien <code>when</code> se usa mucho en rangos, este <a href="https://kotlinlang.org/docs/reference/basic-syntax.html#using-when-expression">no es su único uso posible</a>. <strong>Ejemplo:</strong></p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">describe</span><span class="token punctuation">(</span>obj<span class="token operator">:</span> Any<span class="token punctuation">)</span><span class="token operator">:</span> String <span class="token operator">=</span>
    <span class="token keyword">when</span> <span class="token punctuation">(</span>obj<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token number">1</span>          <span class="token operator">-&gt;</span> <span class="token string">"One"</span>
        <span class="token string">"Hello"</span>    <span class="token operator">-&gt;</span> <span class="token string">"Greeting"</span>
        <span class="token keyword">is</span> Long    <span class="token operator">-&gt;</span> <span class="token string">"Long"</span>
        <span class="token operator">!</span><span class="token keyword">is</span> String <span class="token operator">-&gt;</span> <span class="token string">"Not a string"</span>
        <span class="token keyword">else</span>       <span class="token operator">-&gt;</span> <span class="token string">"Unknown"</span>
    <span class="token punctuation">}</span>
</code></pre>
<p>Además <code>when</code> puede evaluar varias condiciones simultáneamente</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">when</span> <span class="token punctuation">(</span>x<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token number">0</span><span class="token punctuation">,</span> <span class="token number">1</span> <span class="token operator">-&gt;</span> <span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"x == 0 or x == 1"</span><span class="token punctuation">)</span>
    <span class="token keyword">else</span> <span class="token operator">-&gt;</span> <span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"otherwise"</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Es posible usar <code>when</code> <strong>como un reemplazo de una sentencia if-else if</strong></p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">when</span> <span class="token punctuation">{</span>
    x<span class="token punctuation">.</span><span class="token function">isOdd</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">-&gt;</span> <span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"x is odd"</span><span class="token punctuation">)</span>
    y<span class="token punctuation">.</span><span class="token function">isEven</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">-&gt;</span> <span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"y is even"</span><span class="token punctuation">)</span>
    <span class="token keyword">else</span> <span class="token operator">-&gt;</span> <span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"x+y is odd."</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Y también para <strong>validar peticiones HTTP</strong><br>
<em>Esto es partir de Kotlin v1.3</em></p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> Request<span class="token punctuation">.</span><span class="token function">getBody</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=</span>
	<span class="token keyword">when</span> <span class="token punctuation">(</span><span class="token keyword">val</span> response <span class="token operator">=</span> <span class="token function">executeRequest</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token keyword">is</span> Success <span class="token operator">-&gt;</span> response<span class="token punctuation">.</span>body
        <span class="token keyword">is</span> HttpError <span class="token operator">-&gt;</span> <span class="token keyword">throw</span> <span class="token function">HttpException</span><span class="token punctuation">(</span>response<span class="token punctuation">.</span>status<span class="token punctuation">)</span>
	<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<h3 id="clase-13.-bucles-while-y--do-while">Clase 13. Bucles while y  do while</h3>
<h4 id="while">While</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> i <span class="token operator">=</span> <span class="token number">1</span>
<span class="token keyword">while</span> <span class="token punctuation">(</span>i <span class="token operator">&lt;=</span> <span class="token number">10</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"i = <span class="token interpolation variable">$i</span>"</span><span class="token punctuation">)</span>
    i<span class="token operator">++</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="do-while">Do While</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin">i <span class="token operator">=</span> <span class="token number">1</span>
<span class="token keyword">do</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"i = <span class="token interpolation variable">$i</span>"</span><span class="token punctuation">)</span>
    i<span class="token operator">++</span>
<span class="token punctuation">}</span> <span class="token keyword">while</span> <span class="token punctuation">(</span>i <span class="token operator">&lt;=</span> <span class="token number">10</span><span class="token punctuation">)</span>
</code></pre>
</li>
<li>
<h3 id="clase-14.-ciclos-for-y-foreach-en-kotlin">Clase 14. Ciclos for y foreach en Kotlin</h3>
<h4 id="for">For</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> daysOfWeek <span class="token operator">=</span> <span class="token function">listOf</span><span class="token punctuation">(</span><span class="token string">"Domingo"</span><span class="token punctuation">,</span><span class="token string">"Lunes"</span><span class="token punctuation">,</span><span class="token string">"Martes"</span><span class="token punctuation">,</span><span class="token string">"Miercoles"</span><span class="token punctuation">,</span><span class="token string">"Jueves"</span><span class="token punctuation">,</span><span class="token string">"Viernes"</span><span class="token punctuation">,</span><span class="token string">"Sabado"</span><span class="token punctuation">)</span>
<span class="token keyword">for</span><span class="token punctuation">(</span>day <span class="token keyword">in</span> daysOfWeek<span class="token punctuation">)</span><span class="token punctuation">{</span>
        <span class="token function">println</span><span class="token punctuation">(</span>day<span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Si se quiere tener acceso al índice de cada elemento del Array la sintaxis es la siguiente:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">for</span><span class="token punctuation">(</span><span class="token punctuation">(</span>index<span class="token punctuation">,</span>day<span class="token punctuation">)</span> <span class="token keyword">in</span> daysOfWeek<span class="token punctuation">.</span><span class="token function">withIndex</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
        <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"<span class="token interpolation variable">$index</span> :<span class="token interpolation variable">$day</span>"</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="foreach">Foreach</h4>
<p>También permite recorrer una lista con múltiples elementos pero usando una sintaxis más simple:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> daysOfWeek <span class="token operator">=</span> <span class="token function">listOf</span><span class="token punctuation">(</span><span class="token string">"Domingo"</span><span class="token punctuation">,</span><span class="token string">"Lunes"</span><span class="token punctuation">,</span><span class="token string">"Martes"</span><span class="token punctuation">,</span><span class="token string">"Miercoles"</span><span class="token punctuation">,</span><span class="token string">"Jueves"</span><span class="token punctuation">,</span><span class="token string">"Viernes"</span><span class="token punctuation">,</span><span class="token string">"Sabado"</span><span class="token punctuation">)</span>
daysOfWeek<span class="token punctuation">.</span><span class="token function">forEach</span><span class="token punctuation">{</span>
        <span class="token function">println</span><span class="token punctuation">(</span>it<span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<p><code>it</code> será el iterador que contiene cada elemento de la lista mientras es recorrida.</p>
<p>También se puede usar <code>forEachIndexed</code> para obtener acceso a los índices:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin">daysOfWeek<span class="token punctuation">.</span><span class="token function">forEachIndexed</span> <span class="token punctuation">{</span> index<span class="token punctuation">,</span> s <span class="token operator">-&gt;</span> <span class="token function">println</span><span class="token punctuation">(</span>“Index $index<span class="token operator">:</span> $s”<span class="token punctuation">)</span> <span class="token punctuation">}</span>
</code></pre>
<p><strong>🛈 Nota:</strong> un ciclo <code>for</code> es 10x más rápido que uno <code>foreach</code>.</p>
<h4 id="conclusiones-de-rendimiento">Conclusiones de rendimiento</h4>
<ul>
<li><strong>Si es para un rango es mejor usar For</strong></li>
<li><strong>Si es para una colección (sequence, list, set) es mejor foreach</strong></li>
<li><strong>Si se va a usar break y continue es mejor For</strong></li>
</ul>
</li>
<li>
<h3 id="clase-15.-break-continue-y-labels">Clase 15. Break, Continue y Labels</h3>
<h4 id="break">break</h4>
<p>Permite interrumpir el código cuando se cumpla una condición.</p>
<p><strong>Ejemplo:</strong></p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">for</span> <span class="token punctuation">(</span>i <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">3</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"\ni: <span class="token interpolation variable">$i</span> "</span><span class="token punctuation">)</span>
        <span class="token keyword">for</span> <span class="token punctuation">(</span>j <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>j<span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">break</span> <span class="token comment">// Termina el ciclo más cercano</span>
            <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"j: <span class="token interpolation variable">$j</span>"</span><span class="token punctuation">)</span>
        <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="continue">continue</h4>
<p>Permite  omitir iteraciones de un ciclo cuando se cumpla una condición</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">for</span> <span class="token punctuation">(</span>i <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">3</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"\ni: <span class="token interpolation variable">$i</span> "</span><span class="token punctuation">)</span>
        <span class="token keyword">for</span> <span class="token punctuation">(</span>j <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>j<span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">continue</span> <span class="token comment">// Va a la siguiente línea de código del ciclo más cercano.</span>
            <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"j: <span class="token interpolation variable">$j</span>"</span><span class="token punctuation">)</span>
        <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="labels">Labels</h4>
<p>Sirven para controlar mejor los saltos y <strong>definir en qué ciclo queremos que inicie después de saltar.</strong> Permiten “etiquetar” por así decirlo el ciclo especifico al que se quiere aplicar <code>break</code> o <code>continue</code>. Son particularmente útiles cuando se tienen ciclos anidados.</p>
<p>La sintaxis para <strong>crear</strong> un label es: <code>nombre@</code></p>
<p>La sintaxis para <strong>llamar</strong> a un label es: <code>break/continue@nombre</code></p>
<p><strong>Ejemplos:</strong></p>
<ul>
<li>
<h5 id="break-y-label">break y label</h5>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token label symbol">terminarTodoCiclo@</span> <span class="token keyword">for</span> <span class="token punctuation">(</span>i <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">3</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"\ni: <span class="token interpolation variable">$i</span> "</span><span class="token punctuation">)</span>
    <span class="token keyword">for</span> <span class="token punctuation">(</span>j <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">3</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"\nj: <span class="token interpolation variable">$j</span>"</span><span class="token punctuation">)</span>
        <span class="token keyword">for</span> <span class="token punctuation">(</span>k <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>k<span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">break</span><span class="token label symbol">@terminarTodoCiclo</span>
            <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"k: <span class="token interpolation variable">$k</span>"</span><span class="token punctuation">)</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<h5 id="break-y-continue">break y continue</h5>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token label symbol">escaparJ@</span> <span class="token keyword">for</span> <span class="token punctuation">(</span>i <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">3</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"\ni: <span class="token interpolation variable">$i</span> "</span><span class="token punctuation">)</span>
    <span class="token keyword">for</span> <span class="token punctuation">(</span>j <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">3</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"\nj: <span class="token interpolation variable">$j</span>"</span><span class="token punctuation">)</span>
        <span class="token keyword">for</span> <span class="token punctuation">(</span>k <span class="token keyword">in</span> <span class="token number">1</span><span class="token operator">..</span><span class="token number">5</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>k<span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">continue</span><span class="token label symbol">@escaparJ</span>
            <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"k: <span class="token interpolation variable">$k</span>"</span><span class="token punctuation">)</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
</ul>
</li>
<li>
<h3 id="clase-16.-valores-nulos-y-double-bang">Clase 16. Valores Nulos y Double Bang</h3>
<p>La <em>“nada”</em> es un concepto ligado al lenguaje natural, en  el caso de Kotlin lo más cercano para representar nada es un valor <em>nulo</em>.</p>
<p><strong>🛈 Nota:</strong> es una práctica inicializar las variables y no dejarlas como valores nulos.</p>
<p>Kotlin es <strong>Null Safety</strong> lo que significa que previene las indeterminaciones que causan los <code>NullPointerExeptions</code>. Por defecto <strong>ningún valor puede ser nulo</strong> pues esto marcará un error. Kotlin evita que una excepción sea lanzada pues esto provoca vulnerabilidades.</p>
<p>No obstante habrá ocasiones en las que se necesite forzosamente trabajar con valores nulos. En ese caso Kotlin ofrece una sintaxis especial para ello.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> foo<span class="token operator">:</span> Int<span class="token operator">?</span> <span class="token comment">// ? → Permite que la variaable sea Null Saftly, es decir que no se lance una excepción por ser un valor nulo </span>
foo<span class="token operator">?</span><span class="token punctuation">.</span><span class="token function">metodo</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<h4 id="double-bang">Double bang</h4>
<p>Es un operador que permite manejar una excepción. Si por ejemplo se tiene un valor nulo este operador va a forzar que se lance la excepción.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> msg<span class="token operator">:</span> String<span class="token operator">?</span>
msg <span class="token operator">=</span> <span class="token keyword">null</span>
<span class="token function">println</span><span class="token punctuation">(</span>msg<span class="token operator">!!</span><span class="token punctuation">.</span>length<span class="token punctuation">)</span> <span class="token comment">// !! → Operador Double bang</span>
</code></pre>
<p><strong>🛈 Nota:</strong> el operador <em>double bang</em> se rara vez en el flujo de desarrollo profesional con Kotlin. <strong>No se recomienda usarlo</strong>, pues esto se considera una mala práctica.</p>
</li>
<li>
<h3 id="clase-17.-operador-elvis">Clase 17. Operador Elvis</h3>
<p>Una de las comparaciones más comunes en la programación es la siguiente:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">if</span> <span class="token punctuation">(</span>list <span class="token operator">!=</span> <span class="token keyword">null</span><span class="token punctuation">)</span> <span class="token keyword">return</span> list<span class="token punctuation">.</span>size
<span class="token keyword">else</span> <span class="token keyword">return</span> <span class="token number">0</span>
</code></pre>
<p>Lo anterior es una evaluación en la que si un elemento no es <code>null</code> se retorna alguna operación sobre dicho elemento, de lo contrario se retorna 0.</p>
<p>Usando el operador Elvis(<code>?:</code>) la sintaxis de la anterior se resumiría así:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin">it<span class="token punctuation">.</span><span class="token function">listFiles</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token operator">?</span><span class="token punctuation">.</span>size <span class="token operator">?:</span> <span class="token number">0</span>
</code></pre>
</li>
<li>
<h3 id="clase-18.-ejercicios-con-null-safety-y-operador-elvis">Clase 18. Ejercicios con Null safety y operador Elvis</h3>
<h4 id="doubel-bang">Doubel bang</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token comment">// Siempre que se use !! se DEBE manejat la excepción con un try/cath</span>
<span class="token keyword">try</span> <span class="token punctuation">{</span>
    <span class="token keyword">var</span> compute<span class="token operator">:</span> String<span class="token operator">?</span>
    compute <span class="token operator">=</span> <span class="token keyword">null</span>
    <span class="token keyword">var</span> longitud<span class="token operator">:</span> Int <span class="token operator">=</span> compute<span class="token operator">!!</span><span class="token punctuation">.</span>length
<span class="token punctuation">}</span> <span class="token keyword">catch</span> <span class="token punctuation">(</span>e<span class="token operator">:</span> NullPointerException<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Ingresa un valor, no aceptamos nulos"</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="llamada-segura">Llamada segura</h4>
<p>Evitar que salte una excepción</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> compute<span class="token operator">:</span> String<span class="token operator">?</span> <span class="token operator">=</span> <span class="token keyword">null</span>
<span class="token keyword">val</span> longitud<span class="token operator">:</span> Int<span class="token operator">?</span> <span class="token operator">=</span> compute<span class="token operator">?</span><span class="token punctuation">.</span>length
<span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"longitud = <span class="token interpolation variable">$longitud</span>"</span><span class="token punctuation">)</span>
</code></pre>
<h4 id="operador-elvis">Operador Elvis</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> teclado<span class="token operator">:</span> String<span class="token operator">?</span> <span class="token operator">=</span> <span class="token keyword">null</span>
<span class="token keyword">val</span> longitudTeclado<span class="token operator">:</span> Int <span class="token operator">=</span> teclado<span class="token operator">?</span><span class="token punctuation">.</span>length <span class="token operator">?:</span> <span class="token number">0</span>
<span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Longitud teclado; <span class="token interpolation variable">$longitudTeclado</span>"</span><span class="token punctuation">)</span>
</code></pre>
<h4 id="filtrar-nulls-en-un-list">Filtrar Nulls en un List</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> listWithNulls<span class="token operator">:</span> List<span class="token operator">&lt;</span>Int<span class="token operator">?</span><span class="token operator">&gt;</span> <span class="token operator">=</span> listOf<span class="token operator">&lt;</span>Int<span class="token operator">?</span><span class="token operator">&gt;</span><span class="token punctuation">(</span><span class="token number">7</span><span class="token punctuation">,</span> <span class="token keyword">null</span><span class="token punctuation">,</span> <span class="token keyword">null</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">)</span>
<span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Lista con null: <span class="token interpolation variable">$listWithNulls</span>"</span><span class="token punctuation">)</span>

<span class="token keyword">val</span> listWithoutNull<span class="token operator">:</span> List<span class="token operator">&lt;</span>Int<span class="token operator">&gt;</span> <span class="token operator">=</span> listWithNulls<span class="token punctuation">.</span><span class="token function">filterNotNull</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// filterNotNull() → Elimina los valores null de una lista </span>
<span class="token function">println</span><span class="token punctuation">(</span>listWithoutNull<span class="token punctuation">)</span>
</code></pre>
</li>
<li>
<h3 id="clase-20.-¿qué-es-un-array-en-kotlin">Clase 20. ¿Qué es un Array en Kotlin?</h3>
<h4 id="arrays">Arrays</h4>
<p>Son colecciones de datos que permiten múltiples datos.</p>
<h5 id="declarar-arrays">Declarar Arrays</h5>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> countries <span class="token operator">=</span> <span class="token function">arrayOf</span><span class="token punctuation">(</span><span class="token string">"India"</span><span class="token punctuation">,</span> <span class="token string">"México"</span><span class="token punctuation">,</span> <span class="token string">"Colombia"</span><span class="token punctuation">,</span> <span class="token string">"Argentina"</span><span class="token punctuation">,</span> <span class="token string">"Chile"</span><span class="token punctuation">,</span> <span class="token string">"Perú"</span><span class="token punctuation">)</span> <span class="token comment">// Crea un array cuyo tipo de dato será inferido</span>

<span class="token keyword">val</span> days <span class="token operator">=</span> arrayOf<span class="token operator">&lt;</span>String<span class="token operator">&gt;</span><span class="token punctuation">(</span><span class="token string">"Lunes"</span><span class="token punctuation">,</span> <span class="token string">"Martes"</span><span class="token punctuation">,</span> <span class="token string">"Miércoles"</span><span class="token punctuation">,</span> <span class="token string">"Jueves"</span><span class="token punctuation">,</span> <span class="token string">"Sábado"</span><span class="token punctuation">,</span> <span class="token string">"Domingo"</span><span class="token punctuation">)</span> <span class="token comment">// Crea un array de un tipo de dato especifico.</span>

<span class="token keyword">val</span> numbers <span class="token operator">=</span> <span class="token function">intArrayOf</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">)</span> <span class="token comment">// Crea un Array de enteros</span>
</code></pre>
<h5 id="recorrer-arrays">Recorrer Arrays</h5>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">for</span> <span class="token punctuation">(</span>num <span class="token keyword">in</span> numbers<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Numbers: <span class="token interpolation variable">$num</span>"</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<h5 id="conocer-longitud-de-un-array">Conocer longitud de un Array</h5>
<pre class=" language-kotlin"><code class="prism  language-kotlin">numbers<span class="token punctuation">.</span>size
</code></pre>
</li>
<li>
<h3 id="clase-21.-métodos-útiles-en-arreglos">Clase 21. Métodos útiles en arreglos</h3>
<h4 id="diferencias-entre-las-formas-de-declarar-arrays">Diferencias entre las formas de declarar Arrays</h4>
<p>Esta forma de declarar Arrays se usa para almacenar objetos:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> foo <span class="token operator">=</span> arrayOf<span class="token operator">&lt;</span>String<span class="token operator">&gt;</span><span class="token punctuation">(</span><span class="token operator">..</span><span class="token punctuation">.</span><span class="token punctuation">)</span>
</code></pre>
<p>Por el contrario esta otra forma se usa para almacenar tipos de datos primitivos:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> bar <span class="token operator">=</span> <span class="token function">intArrayOf</span><span class="token punctuation">(</span><span class="token operator">..</span><span class="token punctuation">.</span><span class="token punctuation">)</span>
</code></pre>
<h4 id="convertir-un-array-de-objetos-en-un-array-de-tipos-primitivos">Convertir un Array de objetos en un Array de tipos primitivos</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> arrayObject <span class="token operator">=</span> <span class="token function">arrayOf</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">6</span><span class="token punctuation">,</span> <span class="token number">7</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">)</span>
<span class="token keyword">var</span> intPrimitive<span class="token operator">:</span> IntArray <span class="token operator">=</span> arrayObject<span class="token punctuation">.</span><span class="token function">toIntArray</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// Convertir a Array de primitivos</span>
</code></pre>
<h4 id="métodos-de-arrays">Métodos de Arrays</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> suma <span class="token operator">=</span> arrayObject<span class="token punctuation">.</span><span class="token function">sum</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// sum() → Suma los elementos de un Array</span>
arrayObject <span class="token operator">=</span> arrayObject<span class="token punctuation">.</span><span class="token function">plus</span><span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">)</span> <span class="token comment">// plus() → Añadir un elemento al Array</span>
arrayObject <span class="token operator">=</span> arrayObject<span class="token punctuation">.</span><span class="token function">reversedArray</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// reversedArray() → Invertir un Array</span>
arrayObject<span class="token punctuation">.</span><span class="token function">reverse</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// Lo mismo que el anterior pero sin asignar el array modificado a una variable</span>

</code></pre>
</li>
<li>
<h3 id="clase-22.-expresiones-vs.-valores">Clase 22. Expresiones vs. Valores</h3>
<p>En Kotlin <strong>todo</strong> es una <strong>expresión</strong>.</p>
<p>En Kotlin <strong>siempre</strong> se devuelve un valor y eso incluye a las expresiones.</p>
<h4 id="expresiones">Expresiones</h4>
<p>Se componen de variables y operadores que devuelven un valor.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token comment">// ${} → poner expresiones</span>
<span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"x es igual a 5? <span class="token interpolation"><span class="token delimiter variable">${</span>x <span class="token operator">==</span> <span class="token number">5</span><span class="token delimiter variable">}</span></span>"</span><span class="token punctuation">)</span>

<span class="token comment">// $ → poner valores</span>
<span class="token keyword">val</span> msg <span class="token operator">=</span> <span class="token string">"El valor de x es <span class="token interpolation variable">$x</span>"</span>
</code></pre>
<p>Hay algunas funciones del lenguaje que so pueden ser una expresión como por ejemplo los bucles <code>for</code> y <code>while</code>. De ahí en adelante todo en Kotlin puede ser una expresión (condicionales, funciones,  operaciones matemáticas, etc).</p>
</li>
<li>
<h3 id="clase-23.-funciones-en-kotlin">Clase 23. Funciones en Kotlin</h3>
<p>En Kotlin existen dos tipos de funciones:</p>
<ul>
<li>Funciones provistas con Kotlin</li>
<li>Funciones declaradas por el desarrollador.</li>
</ul>
<p>En Kotlin una función <strong>siempre</strong> va a devolver un <strong>valor</strong></p>
<p><strong>🛈 Nota:</strong> se pueden usar funciones escritas en Java dentro de Kotlin</p>
<h4 id="declarar-funciones-en-kotlin">Declarar funciones en Kotlin</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">averageNumbers</span><span class="token punctuation">(</span>numbers<span class="token operator">:</span> IntArray<span class="token punctuation">)</span><span class="token operator">:</span> Int <span class="token punctuation">{</span>
    <span class="token keyword">var</span> sum <span class="token operator">=</span> <span class="token number">0</span>
    <span class="token keyword">for</span> <span class="token punctuation">(</span>num <span class="token keyword">in</span> numbers<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        sum <span class="token operator">+=</span> num
    <span class="token punctuation">}</span>

    <span class="token keyword">return</span> sum <span class="token operator">/</span> numbers<span class="token punctuation">.</span>size
<span class="token punctuation">}</span>
</code></pre>
<p><strong>🛈 Nota:</strong> En Kotlin <strong>Unit</strong> es la forma de decir que una función no retorna nada. En caso de que una función si retorne algo es necesario poner el tipo de dato que se va a retornar.</p>
<h4 id="llamar-funciones">Llamar funciones</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token function">averageNumbers</span><span class="token punctuation">(</span>numbers<span class="token punctuation">)</span>
</code></pre>
</li>
<li>
<h3 id="clase-24.-funciones-con-parámetros-por-defecto">Clase 24. Funciones con parámetros por defecto</h3>
<p>Kotlin permite definir valores por defecto en las funciones (Named arguments). Estos valores se usarán en caso de que se pase ningún parámetro a la función.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token comment">// character: Char = '=', number: Int  = 2 → Son los Named arguments</span>
<span class="token keyword">fun</span> <span class="token function">evaluate</span><span class="token punctuation">(</span>character<span class="token operator">:</span> Char <span class="token operator">=</span> <span class="token string">'='</span><span class="token punctuation">,</span> number<span class="token operator">:</span> Int  <span class="token operator">=</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token operator">:</span> String <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token string">"<span class="token interpolation variable">$number</span> es <span class="token interpolation variable">$character</span>"</span>
<span class="token punctuation">}</span>

<span class="token function">evaluate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// Al no pasarse ningún parámetro se usarán los Named arguments definidos en la declaración de la función</span>
<span class="token function">evaluate</span><span class="token punctuation">(</span><span class="token string">'+'</span><span class="token punctuation">)</span> <span class="token comment">// Reemplaza uno de los Named arguments por '+'</span>
</code></pre>
</li>
<li>
<h3 id="clase-25.-lambdas-en-kotlin">Clase 25. Lambdas en Kotlin</h3>
<p>Lambdas permite tener una nueva forma de escribir funciones. En otros lenguajes  a las lambdas se les conoce como <em>funciones anónimas</em>, <em>functions literals</em> o <em>funciones literales</em>. Las Lambdas son en esencia funciones que no tienen nombre.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token punctuation">{</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Hola mundo"</span><span class="token punctuation">)</span><span class="token punctuation">}</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// Las sentencias de la función se ponen dentro de {...}. Luego se ponen ()</span>

<span class="token comment">// Por lo general las Lambdas se guardan dentro de una variable</span>
<span class="token keyword">var</span> hola <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Hola mundo"</span><span class="token punctuation">)</span><span class="token punctuation">}</span><span class="token punctuation">(</span><span class="token punctuation">)</span>

<span class="token comment">// La función se llamaría así</span>
<span class="token function">hola</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<p>Hay otro tipo de sintaxis que se puede usar para crear funciones Lambdas</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> w <span class="token operator">=</span> <span class="token punctuation">{</span>d<span class="token operator">:</span> Int<span class="token punctuation">,</span> c<span class="token operator">:</span> Int <span class="token operator">-&gt;</span> d<span class="token operator">+</span>c<span class="token punctuation">}</span> <span class="token comment">// -&gt; separa los parámetros de las acciones de la Lambda. Al lado izquierdo se ponen los parámetros y a la derecha las acciones</span>

<span class="token comment">// Llamar a la función Lambdas</span>
<span class="token function">println</span><span class="token punctuation">(</span><span class="token function">w</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span>

<span class="token comment">// Aquí se define al función lambda, los parámetros que va recibir y se pasan dichos parámetros (4, 4) en una sóla línea </span>
<span class="token function">println</span><span class="token punctuation">(</span><span class="token punctuation">{</span>d<span class="token operator">:</span> Int<span class="token punctuation">,</span> c<span class="token operator">:</span> Int <span class="token operator">-&gt;</span> d <span class="token operator">+</span> c<span class="token punctuation">}</span><span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
</code></pre>
</li>
</ul>
<h2 id="📚-módulo-4.-programación-orientada-a-objetos">📚 Módulo 4. Programación Orientada a Objetos</h2>
<ul>
<li>
<h3 id="clase--28.-clases">Clase  28. Clases</h3>
<p>En Kotlin las Clases se definen con la palabra reservada <code>class</code>.</p>
</li>
<li>
<h3 id="clase-29.-ejercicio-de--clases">Clase 29. Ejercicio de  Clases</h3>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">class</span> Camera <span class="token comment">// Esta es la forma mínima de definir una Clase en Kotlin</span>
</code></pre>
<h4 id="instanciar-una-clase-en-kotlin">Instanciar una Clase en Kotlin</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> camera <span class="token operator">=</span> <span class="token function">Camera</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// Crear un objeto</span>

camera<span class="token punctuation">.</span><span class="token function">turnOn</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token comment">// Ejecutar métodos</span>
<span class="token function">println</span><span class="token punctuation">(</span>camera<span class="token punctuation">.</span>isOn<span class="token punctuation">)</span> <span class="token comment">// Acceder a atributos</span>
</code></pre>
<p><strong>🛈 Nota:</strong> ningún atributo debería poder ser modificado directamente fuera de la Clase, esto es una mala práctica</p>
</li>
<li>
<h3 id="clase-30.-modificadores-de-acceso">Clase 30. Modificadores de acceso</h3>
<p>En kotlin todos los atributos son <strong>públicos</strong> por defecto.</p>
<h4 id="modificadores-de-acceso-en-kotlin">Modificadores de acceso en Kotlin</h4>
<ul>
<li><strong>public:</strong> todos tienen acceso.</li>
<li><strong>private:</strong> acceso sólo dentro de la Clase</li>
<li><strong>protected:</strong> acceso sólo dentro de la Clase y las Clases que hereden</li>
<li><strong>internal:</strong> acceso entre módulos</li>
</ul>
<h4 id="usar-modificadores-de-acceso">Usar modificadores de acceso</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">private</span> <span class="token keyword">var</span> size
</code></pre>
</li>
<li>
<h3 id="clase-31.-getters-y-setters">Clase 31. Getters y Setters</h3>
<p>Koltlin tiene dos tipos de getters y setters:</p>
<ul>
<li>
<p><strong>Provistos por el programador:</strong> son métodos que son creados por el programador para acceder y/o modificar un atributo. Se usan cuando los elementos están encapsulados. <strong>Ejemplo:</strong></p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">getCameraStatus</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token operator">:</span> String <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>isOn<span class="token punctuation">)</span> <span class="token string">"Camera is Turned"</span> <span class="token keyword">else</span> <span class="token string">"Camera is not turned"</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Acceso directo desde Kotlin:</strong> se usan cuando los elementos no están encapsulados. Permiten definir validaciones a la asignación de los atributos para que los datos sean lo más íntegros posible a la lógica de negocio de la aplicación.</p>
</li>
</ul>
<p><strong>🛈 Nota:</strong> algunos <em>getters</em> y <em>setters</em> podrían no existir dependiendo de los métodos que ya estén definidos dentro de la Clase.</p>
<ul>
<li>
<h3 id="clase-32.-el-get-y-set-propio-de-kotlin">Clase 32. El Get() y Set() propio de Kotlin</h3>
<p><strong>field:</strong> es un tipo de  variable que toma temporalmente el atributo al que se esta haciendo un <code>set()</code> para que dicho atributo pueda ser alterado.</p>
<h4 id="sintaxis-de-un-set">Sintaxis de un set()</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">var</span> size<span class="token operator">:</span> Int <span class="token operator">=</span> <span class="token number">34</span>
    <span class="token keyword">set</span><span class="token punctuation">(</span>value<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token keyword">if</span> <span class="token punctuation">(</span>value <span class="token operator">&gt;=</span> <span class="token number">34</span><span class="token punctuation">)</span>
            field <span class="token operator">=</span> value
        <span class="token keyword">else</span>
            field <span class="token operator">=</span> <span class="token number">34</span>
    <span class="token punctuation">}</span>
</code></pre>
<p><strong>🛈 Nota:</strong> este tipo de sintaxis se usan mucho Clases para datos, cómo por ejemplo Clases que alberguen datos traídos de una API (<em>Data Class</em>. - Clases de Datos) para así efectuar una serie de validaciones para verificar que los datos estén íntegros.</p>
</li>
</ul>
</li>
<li>
<h3 id="clase-33.-data-class-en-kotlin">Clase 33. Data class en Kotlin</h3>
<p>Los <strong>Data Class</strong> son tipos de Clases que permiten manejar datos, dichos datos pueden provenir de una fuente que no sea el código fuente del programa, como por ejemplo una API, una base de datos, etc. Los Data Class se usan para mapear esa fuente de datos y así manejar la consistencia de los atributos de esos datos.</p>
<h4 id="declarar-un-data-class">Declarar un Data Class</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">data</span> <span class="token keyword">class</span> <span class="token function">Movie</span><span class="token punctuation">(</span><span class="token keyword">val</span> title<span class="token operator">:</span> String<span class="token punctuation">,</span> <span class="token keyword">val</span> creator<span class="token operator">:</span> String<span class="token punctuation">,</span> <span class="token keyword">val</span> duration<span class="token operator">:</span> Int<span class="token punctuation">)</span> <span class="token comment">// Atributos mínmos para crear la Clase {</span>
	<span class="token comment">// Implementación</span>
<span class="token punctuation">}</span>
</code></pre>
<p><strong>🛈 Nota:</strong> si bien es posible definir Data Class dentro de otra Clase, estás sólo “vivirán temporalmente” y sólo podrán ser accedidas por la Clase que las contiene. Lo ideal es aferrarse al principio de modularidad y definir las Data Class en un archivo aparte.</p>
</li>
<li>
<h3 id="clase-34.-método-constructor">Clase 34. Método Constructor</h3>
<p>En Kotlin hay 2 tipos de constructores:</p>
<ul>
<li>
<h4 id="constructor-primario">Constructor primario</h4>
<p>Es la forma clásica de inicializar una Clase</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">class</span> <span class="token function">Shoe</span><span class="token punctuation">(</span><span class="token keyword">val</span> sku<span class="token operator">:</span> Int<span class="token punctuation">,</span> <span class="token keyword">var</span> mark<span class="token operator">:</span> String<span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token comment">// Implementación   </span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<h4 id="constructor-secundario">Constructor secundario</h4>
<p>Se define con el prefijo <code>constructor</code>.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">class</span> Person <span class="token punctuation">{</span>
    <span class="token keyword">var</span> children<span class="token operator">:</span> MutableList<span class="token operator">&lt;</span>Person<span class="token operator">&gt;</span> <span class="token operator">=</span> <span class="token function">mutableListOf</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
    <span class="token keyword">constructor</span><span class="token punctuation">(</span>parent<span class="token operator">:</span> Person<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        parent<span class="token punctuation">.</span>children<span class="token punctuation">.</span><span class="token function">add</span><span class="token punctuation">(</span><span class="token keyword">this</span><span class="token punctuation">)</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Si la Clase en cuestión ya tiene un constructor primario, cada constructor secundario debe delegar al constructor primario, ya sea directa o indirectamente a través de otro(s) constructor(es) secundario(s). La delegación a otro constructor de la misma clase se realiza mediante la palabra reservada <code>this</code>:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">class</span> <span class="token function">Person</span><span class="token punctuation">(</span><span class="token keyword">val</span> name<span class="token operator">:</span> String<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">var</span> children<span class="token operator">:</span> MutableList<span class="token operator">&lt;</span>Person<span class="token operator">&gt;</span> <span class="token operator">=</span> <span class="token function">mutableListOf</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
    <span class="token keyword">constructor</span><span class="token punctuation">(</span>name<span class="token operator">:</span> String<span class="token punctuation">,</span> parent<span class="token operator">:</span> Person<span class="token punctuation">)</span> <span class="token operator">:</span> <span class="token keyword">this</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        parent<span class="token punctuation">.</span>children<span class="token punctuation">.</span><span class="token function">add</span><span class="token punctuation">(</span><span class="token keyword">this</span><span class="token punctuation">)</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
</ul>
<p>En Kotlin además también se cuenta con otro elemento:</p>
<ul>
<li>
<h4 id="bloque-de-inicialización-initializer-blocks">Bloque de Inicialización (initializer blocks)</h4>
<p>Alberga el código de inicialización. Se ejecuta cuando se construya la Clase y permite definir el código que se quiere ejecutar cuando se cree la Clase.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">init</span> <span class="token punctuation">{</span>
	<span class="token comment">// Implementación    </span>
<span class="token punctuation">}</span>
</code></pre>
</li>
</ul>
</li>
<li>
<h3 id="clase-35.-herencia-y-polimorfismo">Clase 35. Herencia y polimorfismo</h3>
<p><strong>Todas</strong> las Clases de Kotlin heredan de la Clase <code>Any</code>.</p>
<h4 id="definir-herencia-en-kotlin">Definir herencia en Kotlin</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">class</span> Subclase <span class="token operator">:</span> Superclase <span class="token punctuation">{</span>
    <span class="token comment">// Implementación</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="polimorfismo-en-kotlin">Polimorfismo en Kotlin</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">override</span> <span class="token keyword">fun</span> <span class="token function">toString</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token operator">:</span> String <span class="token punctuation">{</span>
	<span class="token keyword">return</span> "SKU ID<span class="token operator">:</span> $SKU\nMARK<span class="token operator">:</span> $mark\nMODEL<span class="token operator">:</span> $model\nCOLOR<span class="token operator">:</span> $color\nSIZE<span class="token operator">:</span> $size
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<h3 id="clase-36.-aplicando-herencia-y-polimorfismo">Clase 36. Aplicando herencia y polimorfismo</h3>
<p>En Kotlin por defecto no se puede heredar una Clase. Esto se debe a que por defecto las Clases en Kotlin están <strong>cerradas</strong>. Para “abrir” una Clase se usa la siguiente sintaxis:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">open</span> <span class="token keyword">class</span> Product
</code></pre>
<h4 id="aplicando-herencia">Aplicando herencia</h4>
<ul>
<li>
<h5 id="superclase">Superclase</h5>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">open</span> <span class="token keyword">class</span> <span class="token function">Product</span><span class="token punctuation">(</span><span class="token keyword">var</span> name<span class="token operator">:</span> String<span class="token punctuation">,</span> <span class="token keyword">var</span> description<span class="token operator">:</span> String<span class="token punctuation">,</span> <span class="token keyword">var</span> sku<span class="token operator">:</span> Int<span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token comment">// Implementación</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<h5 id="subclase">Subclase</h5>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">class</span> <span class="token function">Shoe</span><span class="token punctuation">(</span>sku<span class="token operator">:</span> Int<span class="token punctuation">,</span> <span class="token keyword">var</span> mark<span class="token operator">:</span> String<span class="token punctuation">,</span> name<span class="token operator">:</span> String<span class="token punctuation">,</span> description<span class="token operator">:</span> String<span class="token punctuation">)</span><span class="token operator">:</span> <span class="token function">Product</span><span class="token punctuation">(</span>name<span class="token punctuation">,</span> description<span class="token punctuation">,</span> sku<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// Implementación</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Como el constructor de la superclase tiene parámetros definidos es necesario pasar también dichos parámetros al aplicar al herencia, sólo que en este caso no llevaran tipo de dato ni la palabra  reservada para declarar variables: <code>: Product(name, description, sku)</code>.</p>
<p>Además también es necesario indicar dichos parámetros en el constructor de la subclase, en este caso si se declararán como variables y llevarán su respectivo tipo de dato en caso de ser necesario: <code>class Shoe(sku: Int, var mark: String, name: String, description: String):</code></p>
<p><strong>🛈 Nota:</strong> en Kotlin los métodos de una clase también están cerrados por defecto, por lo que si se quiere sobrescribir un método hay que poner el prefijo <code>open</code> en su definición para hacerlo “abierto” y poder sobrescribirlo.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">open</span> <span class="token keyword">fun</span> <span class="token function">create</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token operator">:</span> String <span class="token punctuation">{</span>
    <span class="token comment">// Implementación</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Para acceder a métodos/atributos de la super clase se usa la palabra reservada <code>super</code>.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">override</span> <span class="token keyword">fun</span> <span class="token function">toString</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token operator">:</span> String <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token keyword">super</span><span class="token punctuation">.</span><span class="token function">toString</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span> <span class="token string">"SKU ID: <span class="token interpolation variable">$sku</span>\nBRAND: <span class="token interpolation variable">$brand</span>\nMODEL: <span class="token interpolation variable">$model</span>\nCOLOR: <span class="token interpolation variable">$color</span>\nSIZE: <span class="token interpolation variable">$size</span>"</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
</ul>
</li>
<li>
<h3 id="clase-37.-clases-abstractas">Clase 37. Clases abstractas</h3>
<p>Son Clases que <strong>no tienen implementación</strong>. No se pueden crear instancias de este tipo de Clases.</p>
<p>Las Clases Abstractas se define con el prefijo <code>abstract</code>.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">abstract</span> <span class="token keyword">class</span> Product
</code></pre>
<p>Este tipo de Clases pueden contener <strong>métodos abstractos</strong>, que son métodos que no tienen cuerpo y que tienen que implementarse obligatoriamente en las subclases, y también pueden contener métodos normales cuya implementación es opcional.</p>
<p><strong>Ejemplo de método abstracto:</strong></p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">abstract</span> <span class="token keyword">fun</span> <span class="token function">create</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token operator">:</span> String
</code></pre>
</li>
<li>
<h3 id="clase-38.-interfaces">Clase 38. Interfaces</h3>
<ul>
<li>
<p>Las <strong>interfaces</strong> se centran en las acciones/métodos que se repiten entre clases. Los métodos que se definen en una interfaz pueden implementarse en cualquier Clase independientemente de su familia o jerarquía.</p>
</li>
<li>
<p>Por lo general se nombran con una <code>I</code> como prefijo o <code>able</code> como sufijo.</p>
<p>Las <strong>Clases Abstractas</strong> por el contrario se centran en los atributos/propiedades redundantes entre Clases. Se heredan de forma lineal al igual que cualquier otra Clase.</p>
</li>
</ul>
<h4 id="implementar-una-interfaz">Implementar una Interfaz</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">class</span> <span class="token function">Shoe</span><span class="token punctuation">(</span>sku<span class="token operator">:</span> Int<span class="token punctuation">,</span> <span class="token keyword">var</span> brand<span class="token operator">:</span> String<span class="token punctuation">,</span> name<span class="token operator">:</span> String<span class="token punctuation">,</span> description<span class="token operator">:</span> String<span class="token punctuation">)</span><span class="token operator">:</span> <span class="token function">Product</span><span class="token punctuation">(</span>name<span class="token punctuation">,</span> description<span class="token punctuation">,</span> sku<span class="token punctuation">)</span><span class="token punctuation">,</span> ICrudActions <span class="token punctuation">{</span>
    <span class="token comment">// Implementación</span>
<span class="token punctuation">}</span>
</code></pre>
<p><strong>🛈 Nota:</strong> una Clase puede implementar tantas interfaces como sea posible. Además las Interfaces también pueden albergar métodos con implementación y no sólo métodos sin cuerpo.</p>
</li>
</ul>
<h2 id="📚-módulo-5.-programación-funcional">📚 Módulo 5. Programación Funcional</h2>
<ul>
<li>
<h3 id="clase-40.-funciones-de-orden-superior">Clase 40. Funciones de orden superior</h3>
<p>Son funciones que <strong>reciben como parámetro otras funciones.</strong></p>
<h4 id="declarar-funciones-de-orden-superior">Declarar funciones de orden superior</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">foo</span><span class="token punctuation">(</span>var1<span class="token punctuation">,</span> function<span class="token punctuation">)</span><span class="token operator">:</span> String <span class="token punctuation">{</span> <span class="token comment">// var1 → Datos para la función que se pasa cómo parámetro. function → Función que se pasa como parámetro.</span>
    <span class="token keyword">return</span> <span class="token function">function</span><span class="token punctuation">(</span>var1<span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Algunas funciones de orden superior pueden no contener datos para su ejecución (<code>var1</code> en el ejemplo anterior).</p>
<p>También es común que las funciones de orden superior reciban una Lambda por parámetro.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">foo</span><span class="token punctuation">(</span>var1<span class="token punctuation">,</span> <span class="token punctuation">{</span><span class="token operator">..</span><span class="token punctuation">.</span> <span class="token operator">-&gt;</span> <span class="token operator">..</span><span class="token punctuation">.</span><span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token operator">:</span> String <span class="token punctuation">{</span>
	<span class="token keyword">return</span> <span class="token operator">..</span><span class="token punctuation">.</span>    
<span class="token punctuation">}</span>
</code></pre>
<p>El objetivo de las funciones de orden superior que pueda reutilizar la estructura que se le define muchas veces</p>
<h4 id="llamar-a-una-función-de-orden-superior.">Llamar a una función de orden superior.</h4>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token function">foo</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token string">"hola"</span><span class="token punctuation">,</span> <span class="token operator">::</span>function<span class="token punctuation">)</span> <span class="token comment">// 3, "hola" → Datos para la función que se pasa cómo parámetro. function → Función que se pasa como parámetro.</span>
</code></pre>
</li>
<li>
<h3 id="clase-41.-una-función-como-parámetro">Clase 41. Una función como parámetro</h3>
<p><strong>Ejemplo de una función de orden superior:</strong></p>
<p>Para empezar se declara la función de orden superior.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">calculator</span><span class="token punctuation">(</span>a<span class="token operator">:</span> Int<span class="token punctuation">,</span> b<span class="token operator">:</span> Int<span class="token punctuation">,</span> c<span class="token operator">:</span> Int<span class="token punctuation">,</span> operation<span class="token operator">:</span> <span class="token punctuation">(</span>Int<span class="token punctuation">,</span> Int<span class="token punctuation">,</span> Int<span class="token punctuation">)</span> <span class="token operator">-&gt;</span> Int<span class="token punctuation">)</span><span class="token operator">:</span> Int <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token function">operation</span> <span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">,</span> c<span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Se indican los parámetros (<code>a: Int, b: Int, c: Int</code>) que va a recibir la función <code>operation</code>, esta es a su vez una función lo más genérica posible para que sea posible reutilizar su estructura. Es por eso que sólo se define que va a recibir 3 parámetros de tipo entero y va a retornar un número entero. Después se define el tipo de dato que va retornar la función  de orden superior y finalmente en el cuerpo de la función se retorna la función <code>operation</code> con sus respectivos parámetros.</p>
<p>La estructura que se definió en la  función de orden superior puede ser reutilizada tantas veces como sea necesario en otras funciones:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">sum</span><span class="token punctuation">(</span>a<span class="token operator">:</span> Int<span class="token punctuation">,</span> b<span class="token operator">:</span> Int<span class="token punctuation">,</span> c<span class="token operator">:</span> Int<span class="token punctuation">)</span> <span class="token operator">=</span> a <span class="token operator">+</span> b <span class="token operator">+</span> c
<span class="token keyword">fun</span> <span class="token function">subtract</span><span class="token punctuation">(</span>a<span class="token operator">:</span> Int<span class="token punctuation">,</span> b<span class="token operator">:</span> Int<span class="token punctuation">,</span> c<span class="token operator">:</span> Int<span class="token punctuation">)</span> <span class="token operator">=</span> a <span class="token operator">-</span> b <span class="token operator">-</span> c
<span class="token keyword">fun</span> <span class="token function">multiply</span><span class="token punctuation">(</span>a<span class="token operator">:</span> Int<span class="token punctuation">,</span> b<span class="token operator">:</span> Int<span class="token punctuation">,</span> c<span class="token operator">:</span> Int<span class="token punctuation">)</span> <span class="token operator">=</span> a <span class="token operator">*</span> b <span class="token operator">*</span> c
</code></pre>
<p>Las 3 funciones pueden reutilizar la función de orden superior puesto que se apegan a su estructura; reciben por parámetros 3 números enteros y retornar a su vez un número entero.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token function">calculator</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token operator">::</span>multiply<span class="token punctuation">)</span>
</code></pre>
<p>Por último se llama a la función de orden superior, a la que gracias a su estructura genérica se le puede pasar cualquiera de las 3 funciones creadas anteriormente.</p>
<p>Un ejemplo en el que se ve mucho el uso de funciones de orden superior es el desarrollo de apps Android, por ejemplo en el siguiente código:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin">view<span class="token punctuation">.</span><span class="token function">setOnClickListener</span><span class="token punctuation">(</span><span class="token punctuation">{</span> view <span class="token operator">-&gt;</span> 
	<span class="token comment">// Implementación</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre>
<p>Otra lugar en el que se pueden ver las funciones de orden superior son los Callbacks:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">fun</span> <span class="token function">someRequest</span><span class="token punctuation">(</span>callback<span class="token operator">:</span> <span class="token punctuation">(</span>Data<span class="token punctuation">,</span> Int<span class="token punctuation">)</span> <span class="token operator">-&gt;</span> Unit<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// Implementación</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<h3 id="clase-42.-recursividad.-list">Clase 42. Recursividad. List</h3>
<p>Se pueden crear listas que contengan elementos de un mismo tipo de dato:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> numbersInt <span class="token operator">=</span> <span class="token function">listOf</span><span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">)</span>
</code></pre>
<p>Pero también se pueden crear listas que almacenen elementos con diferentes tipos de datos, en este caso el tipo de dato de la lista será <code>Any</code>.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"> <span class="token keyword">val</span> mylist <span class="token operator">=</span> <span class="token function">listOf</span><span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token string">"lala"</span><span class="token punctuation">,</span><span class="token string">"ll"</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">)</span>
</code></pre>
<p>También se pueden pueden crear estructuras de clave-valor utilizando listas tipo <em>hashMapOf</em>.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> months <span class="token operator">=</span> <span class="token function">hashMapOf</span><span class="token punctuation">(</span><span class="token number">1</span> <span class="token keyword">to</span> <span class="token string">"Enero"</span><span class="token punctuation">,</span> <span class="token number">2</span> <span class="token keyword">to</span> <span class="token string">"Febrero"</span><span class="token punctuation">,</span> <span class="token number">3</span> <span class="token keyword">to</span> <span class="token string">"Marzo"</span><span class="token punctuation">,</span> <span class="token number">4</span> <span class="token keyword">to</span> <span class="token string">"Abril"</span><span class="token punctuation">,</span> <span class="token number">5</span> <span class="token keyword">to</span> <span class="token string">"Mayo"</span><span class="token punctuation">,</span> <span class="token number">6</span> <span class="token keyword">to</span> <span class="token string">"Junio"</span><span class="token punctuation">,</span> <span class="token number">7</span> <span class="token keyword">to</span> <span class="token string">"Julio"</span><span class="token punctuation">,</span> <span class="token number">8</span> <span class="token keyword">to</span> <span class="token string">"Agosto"</span><span class="token punctuation">,</span> <span class="token number">9</span> <span class="token keyword">to</span> <span class="token string">"Septiembre"</span> <span class="token punctuation">,</span> <span class="token number">10</span> <span class="token keyword">to</span> <span class="token string">"Octubre"</span><span class="token punctuation">,</span> <span class="token number">11</span> <span class="token keyword">to</span> <span class="token string">"Noviembre"</span> <span class="token punctuation">,</span>  <span class="token number">12</span> <span class="token keyword">to</span> <span class="token string">"Diciembre"</span> <span class="token punctuation">)</span>
</code></pre>
<p>Para recorrer el HashMap:</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">for</span> <span class="token punctuation">(</span>key <span class="token keyword">in</span> months<span class="token punctuation">.</span>keys<span class="token punctuation">)</span>
	<span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"key:<span class="token interpolation variable">$key</span>  value:<span class="token interpolation"><span class="token delimiter variable">${</span>months<span class="token punctuation">[</span>key<span class="token punctuation">]</span><span class="token delimiter variable">}</span></span>"</span><span class="token punctuation">)</span>
</code></pre>
</li>
<li>
<h3 id="clase-43.-recursividad.-filter">Clase 43. Recursividad. Filter</h3>
<p>Esta función sirve para filtrar los datos que cumplan con determinada condición en una lista. Además es un claro ejemplo de como se usan las funciones de orden  superior, recibe como parámetro un Lambda en la que se puede poner el auxiliar <code>it</code> para poner las acciones únicamente sin necesidad de expresar los parámetros. <code>filter</code> puede recibir una comparación lógica o un método.</p>
<pre class=" language-kotlin"><code class="prism  language-kotlin"><span class="token keyword">val</span> numbersInt <span class="token operator">=</span> <span class="token function">listOf</span><span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">)</span>
numbersInt<span class="token punctuation">.</span><span class="token function">filter</span> <span class="token punctuation">{</span> it <span class="token operator">%</span> <span class="token number">2</span> <span class="token operator">==</span> <span class="token number">0</span> <span class="token punctuation">}</span>  

<span class="token comment">// Este será el resultado: [4,2]</span>

<span class="token keyword">val</span> words <span class="token operator">=</span> <span class="token function">listOf</span><span class="token punctuation">(</span><span class="token string">"Oasis"</span><span class="token punctuation">,</span><span class="token string">"Hola"</span><span class="token punctuation">,</span> <span class="token string">"Holanda"</span><span class="token punctuation">,</span> <span class="token string">"Objeto"</span><span class="token punctuation">)</span>
words<span class="token punctuation">.</span><span class="token function">filter</span> <span class="token punctuation">{</span> it<span class="token punctuation">.</span><span class="token function">startsWith</span><span class="token punctuation">(</span><span class="token string">'O'</span><span class="token punctuation">)</span> <span class="token punctuation">}</span>

<span class="token comment">// Este será el resultado: [Oasis, Objeto]</span>
</code></pre>
</li>
</ul>

    </div>
  </div>
</body>

</html>
