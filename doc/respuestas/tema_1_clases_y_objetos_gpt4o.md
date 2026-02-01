<!--
Posible prompt:
<prompt>
Tengo un cuestionario con preguntas sobre "Clases y Objetos". Debes tener en cuenta que los conocimientos previos que tengo (y por tanto tus respuestas deben ser adaptadas), son:
- C/C++ sin orientación a objetos.
- Temas de Java previos: ninguno.

Cada respuesta debe tener entre 2 - 4 párrafos de longitud (sin contar los trozos de código).

Por favor, escribe en impersonal las respuestas.

</prompt>
----
-->

# TEMA 1. Clases y objetos

## 1. ¿Cuáles son las cuatro características básicas de la programación orientada a objetos? Describe brevemente cada una

### Respuesta
La programación orientada a objetos se apoya en la idea de organizar el código en torno a objetos que combinan datos y funciones. Este enfoque contrasta con la programación estructurada tradicional, donde los datos y las funciones suelen estar separados. Al agrupar ambos elementos, se obtiene un modelo más cercano a cómo se describen entidades del mundo real, lo que facilita la comprensión y el mantenimiento del software.

La encapsulación consiste en proteger los datos internos de un objeto y controlar su acceso mediante métodos específicos. Esto evita modificaciones indebidas y permite cambiar la implementación interna sin afectar al resto del programa. La abstracción, por su parte, permite centrarse en lo esencial de un objeto, definiendo qué hace sin necesidad de conocer cómo lo hace. Este principio ayuda a trabajar con conceptos más simples y manejables.

La herencia permite crear nuevas clases basadas en otras ya existentes, reutilizando atributos y métodos comunes. Este mecanismo evita duplicar código y facilita la creación de jerarquías lógicas entre tipos relacionados. Finalmente, el polimorfismo permite que un mismo método pueda comportarse de distintas formas según el objeto que lo utilice, lo que aporta flexibilidad y permite escribir código más general y adaptable.

## 2. Cita cuatro lenguajes populares que permitan la programación orientada a objetos

### Respuesta
La programación orientada a objetos se encuentra presente en numerosos lenguajes modernos, ya que este paradigma facilita la organización del código y la construcción de sistemas complejos. Aunque cada lenguaje implementa la orientación a objetos con matices propios, todos comparten la idea de trabajar con clases, objetos y los principios fundamentales del paradigma. Esta diversidad permite elegir el lenguaje más adecuado según el tipo de proyecto o el entorno de desarrollo.

Uno de los lenguajes más representativos es Java, diseñado desde el inicio con un enfoque completamente orientado a objetos. También es muy común C++, que combina características de la programación estructurada con mecanismos de orientación a objetos, lo que lo convierte en una opción flexible para proyectos de alto rendimiento. Otro lenguaje ampliamente utilizado es Python, que ofrece una sintaxis sencilla y un modelo de objetos muy accesible para quienes comienzan en este paradigma. Finalmente, C# constituye otra alternativa popular, especialmente en entornos Windows y en el desarrollo con la plataforma .NET, donde la orientación a objetos es un pilar central.

Estos lenguajes no solo permiten aplicar los principios de encapsulación, abstracción, herencia y polimorfismo, sino que también proporcionan bibliotecas y herramientas que facilitan el trabajo con objetos. Gracias a ello, se han convertido en opciones habituales tanto en la industria como en el ámbito académico, y representan una base sólida para aprender y aplicar la programación orientada a objetos en distintos contextos.

## 3. Los paradigmas anteriores a la POO, ¿Qué es la **programación estructurada**? y, todavía mejor, ¿Qué es la **programación modular**?

### Respuesta
La programación estructurada es un paradigma que surgió para mejorar la claridad y la fiabilidad del código, especialmente en lenguajes como C. Se basa en dividir un programa en bloques lógicos y en utilizar únicamente tres estructuras de control: secuencia, selección e iteración. Este enfoque evita el uso indiscriminado de saltos como goto, que dificultan el seguimiento del flujo del programa. Gracias a ello, el código se vuelve más predecible, más fácil de leer y más sencillo de depurar, lo que supuso un avance importante respecto a estilos anteriores.

La programación modular va un paso más allá al proponer que un programa se divida en módulos independientes, cada uno encargado de una parte concreta de la funcionalidad. En C, esto suele materializarse mediante archivos .c y .h, donde cada módulo encapsula funciones y datos relacionados. Este enfoque permite trabajar en partes del programa sin afectar al resto, facilita la reutilización de código y mejora la organización general del proyecto. Aunque no alcanza el nivel de encapsulación de la POO, introduce una estructura más ordenada que sirve como puente conceptual hacia ella.

Ambos paradigmas comparten la idea de descomponer un problema grande en partes más pequeñas y manejables. La programación estructurada se centra en controlar el flujo del programa de forma clara, mientras que la programación modular se enfoca en dividir el código en unidades funcionales coherentes. Estos principios siguen siendo fundamentales incluso en lenguajes orientados a objetos, ya que la POO no reemplaza estas ideas, sino que las amplía y las integra en un modelo más completo basado en clases y objetos.

## 4. ¿Qué tres elementos definen a un objeto en programación orientada a objetos?

### Respuesta
La programación estructurada es un paradigma que surgió para mejorar la claridad y la fiabilidad del código, especialmente en lenguajes como C. Se basa en dividir un programa en bloques lógicos y en utilizar únicamente tres estructuras de control: secuencia, selección e iteración. Este enfoque evita el uso indiscriminado de saltos como goto, que dificultan el seguimiento del flujo del programa. Gracias a ello, el código se vuelve más predecible, más fácil de leer y más sencillo de depurar, lo que supuso un avance importante respecto a estilos anteriores.

La programación modular va un paso más allá al proponer que un programa se divida en módulos independientes, cada uno encargado de una parte concreta de la funcionalidad. En C, esto suele materializarse mediante archivos .c y .h, donde cada módulo encapsula funciones y datos relacionados. Este enfoque permite trabajar en partes del programa sin afectar al resto, facilita la reutilización de código y mejora la organización general del proyecto. Aunque no alcanza el nivel de encapsulación de la POO, introduce una estructura más ordenada que sirve como puente conceptual hacia ella.

Ambos paradigmas comparten la idea de descomponer un problema grande en partes más pequeñas y manejables. La programación estructurada se centra en controlar el flujo del programa de forma clara, mientras que la programación modular se enfoca en dividir el código en unidades funcionales coherentes. Estos principios siguen siendo fundamentales incluso en lenguajes orientados a objetos, ya que la POO no reemplaza estas ideas, sino que las amplía y las integra en un modelo más completo basado en clases y objetos.

## 5. ¿Qué es una clase? ¿Es lo mismo que un objeto? ¿Qué es una instancia? ¿Todos los lenguajes orientados a objetos manejan el concepto de clase?

### Respuesta
Una clase puede entenderse como un modelo o plantilla que describe cómo serán ciertos objetos dentro de un programa. Define qué datos tendrá un objeto (atributos) y qué operaciones podrá realizar (métodos). Desde la perspectiva de alguien acostumbrado a C, una clase se asemeja a una estructura (struct) que, además de variables, incorpora funciones asociadas directamente a esos datos. Sin embargo, la clase no es un objeto en sí misma, sino la definición a partir de la cual se crean objetos concretos.

Un objeto, en cambio, es una entidad real creada a partir de una clase. Representa un elemento concreto que posee su propio estado y puede ejecutar los métodos definidos en la clase. Cada objeto mantiene sus propios valores de los atributos, igual que varias variables de tipo struct pueden contener datos distintos. Por ello, aunque clase y objeto están estrechamente relacionados, no son lo mismo: la clase es el plano; el objeto, la construcción final.

El término instancia se utiliza para referirse a un objeto concreto creado a partir de una clase. Instanciar una clase significa reservar memoria y crear un objeto real que pueda utilizarse en el programa. En Java, por ejemplo, este proceso se realiza mediante el operador new, que genera una instancia con su propio estado. Así, “objeto” e “instancia” suelen emplearse como sinónimos, aunque el segundo enfatiza el acto de creación.

No todos los lenguajes orientados a objetos utilizan necesariamente el concepto de clase. Algunos lenguajes, como Java o C#, se basan completamente en clases para definir objetos. Sin embargo, otros lenguajes orientados a objetos, como JavaScript, emplean un modelo basado en prototipos, donde los objetos pueden crearse y extenderse sin necesidad de una clase formal. Esto demuestra que la orientación a objetos puede implementarse de distintas maneras, aunque el uso de clases sea la aproximación más común en muchos lenguajes modernos.

## 6. ¿Dónde se almacenan en memoria los objetos? ¿Es igual en todos los lenguajes? ¿Qué es la **recolección de basura**? 

### Respuesta
El lugar donde se almacenan los objetos depende del lenguaje y de su modelo de memoria. En lenguajes como Java, los objetos se crean siempre en la memoria dinámica, es decir, en el heap. Las variables que se declaran dentro de métodos solo almacenan referencias a esos objetos, pero no contienen los datos directamente. Este enfoque permite que los objetos tengan una vida útil independiente del ámbito donde se declaran las variables que los utilizan, lo que facilita la gestión de estructuras complejas.

En cambio, en lenguajes como C++ la situación es más flexible. Un objeto puede almacenarse en la pila (stack) si se declara como una variable local normal, o en el heap si se crea con new. Esto implica que el programador debe gestionar explícitamente la vida del objeto, liberando la memoria cuando ya no se necesita. Esta diferencia muestra que no todos los lenguajes orientados a objetos manejan la memoria de la misma manera, y que el modelo de Java es más restrictivo pero también más seguro para principiantes.

La recolección de basura (garbage collection) es un mecanismo automático que libera la memoria ocupada por objetos que ya no están en uso. En lenguajes como Java, el programador no necesita llamar a ninguna función para destruir un objeto; el sistema detecta cuándo ya no existen referencias hacia él y lo elimina de forma automática. Este proceso reduce errores comunes como fugas de memoria o accesos a memoria liberada, que son habituales en lenguajes donde la gestión es manual.

Sin embargo, la recolección de basura no está presente en todos los lenguajes orientados a objetos. C++ es un ejemplo claro: aunque permite POO, no incorpora un recolector de basura integrado, por lo que la responsabilidad de liberar memoria recae en el programador. Esto demuestra que la orientación a objetos no implica necesariamente un modelo de memoria concreto, sino que cada lenguaje combina el paradigma con sus propias decisiones de diseño.


## 7. ¿Qué es un método? ¿Qué es la **sobrecarga de métodos**? 

### Respuesta
Un método es una función asociada a una clase y, por tanto, a los objetos que se crean a partir de ella. Mientras que en C las funciones existen de forma independiente, en la programación orientada a objetos los métodos forman parte del comportamiento de un tipo concreto. Esto permite que cada objeto pueda ejecutar acciones relacionadas directamente con sus propios datos, lo que refuerza la idea de que los objetos combinan estado y comportamiento dentro de una misma unidad lógica.

La sobrecarga de métodos consiste en definir varios métodos con el mismo nombre dentro de una misma clase, pero con diferentes parámetros. El lenguaje decide cuál de ellos utilizar en función del número y tipo de los argumentos que se pasen en la llamada. Este mecanismo permite ofrecer varias formas de realizar una misma operación, adaptándose a distintas necesidades sin tener que inventar nombres diferentes para cada variante, algo que en C suele resolverse manualmente con funciones con sufijos distintos.

Este concepto resulta especialmente útil para mejorar la legibilidad y la coherencia del código. Al mantener un mismo nombre para acciones conceptualmente iguales, se facilita la comprensión del programa y se evita la proliferación de funciones con nombres poco intuitivos. Además, la sobrecarga permite que una clase ofrezca interfaces más flexibles, ya que distintos tipos de datos o combinaciones de parámetros pueden manejarse de forma natural sin romper la estructura del diseño.

## 8. Ejemplo mínimo de clase en Java, que se llame Punto, con dos atributos, x e y, con un método que se llame `calculaDistanciaAOrigen`, que calcule la distancia a la posición 0,0. Por sencillez, los atributos deben tener visibilidad por defecto. Crea además un ejemplo de uso con una instancia y uso del método

### Respuesta
Una clase en Java puede definirse de forma muy sencilla, incluso cuando solo contiene unos pocos atributos y un método básico. En este caso, la clase Punto representa una posición en un plano bidimensional mediante dos atributos, x e y, que almacenan las coordenadas. Al no especificar modificadores de visibilidad, ambos atributos quedan con visibilidad por defecto, lo que significa que solo serán accesibles desde clases del mismo paquete. Este tipo de ejemplo resulta útil para familiarizarse con la sintaxis básica de Java sin introducir todavía conceptos más avanzados.

El método calculaDistanciaAOrigen permite obtener la distancia del punto al origen de coordenadas (0,0). Para ello, se aplica la fórmula matemática habitual basada en el teorema de Pitágoras. Este método demuestra cómo una clase puede encapsular tanto datos como operaciones relacionadas con esos datos, lo que constituye uno de los principios fundamentales de la programación orientada a objetos. Además, el ejemplo de uso muestra cómo crear una instancia de la clase y cómo invocar uno de sus métodos, lo que ayuda a comprender la relación entre clase y objeto.

public class Punto {
    int x;  // visibilidad por defecto
    int y;  // visibilidad por defecto

    double calculaDistanciaAOrigen() {
        return Math.sqrt(x * x + y * y);
    }
}

public class EjemploUso {
    public static void main(String[] args) {
        Punto p = new Punto();
        p.x = 3;
        p.y = 4;

        double distancia = p.calculaDistanciaAOrigen();
        System.out.println("Distancia al origen: " + distancia);
    }
}

## 9. ¿Cuál es el punto de entrada en un programa en Java? ¿Qué es `static` y para qué vale? ¿Sólo se emplea para ese método `main`? ¿Para qué se combina con `final`?

### Respuesta
En Java, el punto de entrada de cualquier programa es el método main, cuya firma estándar es public static void main(String[] args). Este método es el primero que se ejecuta cuando se inicia la aplicación, de forma similar a la función main en C o C++. La máquina virtual de Java busca exactamente esa firma para comenzar la ejecución, lo que convierte a este método en el punto de arranque obligatorio para cualquier programa independiente.

La palabra clave static indica que un método o atributo pertenece a la clase en sí misma y no a una instancia concreta. Esto significa que puede utilizarse sin necesidad de crear un objeto previamente. En el caso del método main, se utiliza static porque la JVM debe poder ejecutarlo sin instanciar la clase que lo contiene. Este comportamiento recuerda a las funciones globales en C, aunque en Java todo debe estar dentro de una clase, por lo que static permite simular ese acceso directo.

El uso de static no se limita al método main. Puede aplicarse a métodos auxiliares, constantes o atributos que deban compartirse entre todas las instancias de una clase. Esto resulta útil cuando una funcionalidad no depende del estado particular de un objeto, sino que pertenece al comportamiento general de la clase. Por ejemplo, métodos matemáticos como Math.sqrt() son estáticos porque no requieren crear un objeto de tipo Math.

Cuando static se combina con final, suele emplearse para definir constantes. La palabra final indica que un valor no puede modificarse después de ser asignado, lo que garantiza su inmutabilidad. Al unir ambos modificadores, se obtiene un valor único, compartido por toda la clase y que no puede cambiar, lo que resulta ideal para constantes como static final double PI = 3.14159;. Esta combinación mejora la claridad del código y evita errores derivados de modificaciones accidentales.

## 10. Intenta ejecutar un poco de Java de forma básica, con los comandos `javac` y `java`. ¿Cómo podemos compilar el programa y ejecutarlo desde linea de comandos? ¿Java es compilado? ¿Qué es la **máquina virtual**? ¿Qué es el *byte-code* y los ficheros `.class`?

### Respuesta
Para compilar un programa Java desde la línea de comandos se utiliza el comando javac, que recibe como argumento el archivo .java que contiene el código fuente. Este proceso genera uno o varios archivos .class, que contienen el byte-code resultante de la compilación. Una vez compilado, el programa se ejecuta mediante el comando java, indicando el nombre de la clase que contiene el método main. Este flujo recuerda al de C/C++, aunque en Java la compilación no produce directamente un ejecutable nativo.

Java se considera un lenguaje compilado e interpretado a la vez. Primero se compila el código fuente a byte-code, un formato intermedio independiente del sistema operativo. Después, ese byte-code es ejecutado por la Máquina Virtual de Java (JVM), que actúa como un intérprete especializado. Este diseño permite que el mismo programa pueda ejecutarse en distintos sistemas sin necesidad de recompilarlo, lo que constituye una de las principales ventajas del lenguaje.

La máquina virtual es un componente que simula un ordenador abstracto capaz de ejecutar el byte-code generado por el compilador. Su función es traducir ese código intermedio a instrucciones que el sistema real pueda entender, aplicando además optimizaciones en tiempo de ejecución. Gracias a la JVM, Java ofrece portabilidad y un entorno controlado que facilita la gestión de memoria y la seguridad del programa.

El byte-code es el conjunto de instrucciones intermedias que produce el compilador de Java y que se almacenan en los archivos .class. No es código máquina nativo, sino un formato diseñado para ser ejecutado por la JVM. Este enfoque separa la compilación del sistema operativo concreto, permitiendo que el mismo archivo .class funcione en cualquier plataforma que disponga de una máquina virtual compatible. Así, los ficheros .class representan la unidad ejecutable básica en el ecosistema Java.

## 11. En el código anterior de la clase `Punto` ¿Qué es `new`? ¿Qué es un **constructor**? Pon un ejemplo de constructor en una clase `Empleado` que tenga DNI, nombre y apellidos

### Respuesta
La palabra clave new en Java se utiliza para crear objetos en memoria dinámica. Cuando se emplea new, la máquina virtual reserva espacio en el heap y devuelve una referencia al objeto recién creado. Este mecanismo recuerda al uso de malloc o new en C/C++, pero con la diferencia de que en Java no es necesario liberar la memoria manualmente, ya que el recolector de basura se encarga de ello. Por tanto, new es el punto de partida para instanciar clases y trabajar con objetos reales dentro del programa.

Un constructor es un método especial que se ejecuta automáticamente cuando se crea un objeto mediante new. Su función es inicializar los atributos del objeto, garantizando que comience su vida en un estado válido. A diferencia de los métodos normales, un constructor no tiene tipo de retorno y debe llevar exactamente el mismo nombre que la clase. En lenguajes como C++ también existen constructores, por lo que este concepto resulta familiar, aunque en Java su uso es obligatorio para cualquier inicialización personalizada.

A continuación se muestra un ejemplo de una clase Empleado con un constructor que inicializa el DNI, el nombre y los apellidos. Este ejemplo ilustra cómo se define un constructor y cómo se asignan valores a los atributos del objeto durante su creación.

public class Empleado {
    String dni;
    String nombre;
    String apellidos;

    public Empleado(String dni, String nombre, String apellidos) {
        this.dni = dni;
        this.nombre = nombre;
        this.apellidos = apellidos;
    }
}


## 12. ¿Qué es la referencia `this`? ¿Se llama igual en todos los lenguajes? Pon un ejemplo del uso de `this` en la clase `Punto`

### Respuesta
La referencia this en Java se utiliza para referirse al objeto actual, es decir, a la instancia sobre la que se está ejecutando un método. Su función principal es distinguir entre los atributos del objeto y los parámetros o variables locales que puedan tener el mismo nombre. Aunque en muchos casos no es obligatorio utilizarla, resulta especialmente útil cuando se desea dejar claro que se está accediendo al estado interno del objeto. Este concepto no existe en C, pero sí aparece en C++ con el mismo nombre y un propósito equivalente.

No todos los lenguajes orientados a objetos utilizan exactamente la palabra this, aunque la mayoría emplea un mecanismo similar. Por ejemplo, en Python se usa self, mientras que en otros lenguajes pueden encontrarse variantes como me o current. A pesar de estas diferencias de sintaxis, la idea es siempre la misma: proporcionar una referencia explícita al objeto que está ejecutando el método. Esto permite acceder a sus atributos, llamar a otros métodos internos o pasar la propia instancia como argumento.

A continuación se muestra un ejemplo de uso de this aplicado a la clase Punto. En este caso, se añade un constructor que recibe valores para x e y, y se utiliza this para diferenciar los atributos del objeto de los parámetros del constructor.

public class Punto {
    int x;
    int y;

    public Punto(int x, int y) {
        this.x = x;  // 'this.x' se refiere al atributo del objeto
        this.y = y;  // 'y' es el parámetro del constructor
    }

    double calculaDistanciaAOrigen() {
        return Math.sqrt(this.x * this.x + this.y * this.y);
    }
}


## 13. Añade ahora otro nuevo método que se llame `distanciaA`, que reciba un `Punto` como parámetro y calcule la distancia entre `this` y el punto proporcionado

### Respuesta
Para calcular la distancia entre dos puntos en Java, resulta útil añadir un método que reciba otro objeto de la misma clase y aplique la fórmula correspondiente. En este caso, el método distanciaA utiliza la referencia this para acceder a las coordenadas del punto actual y compara esos valores con los del punto recibido como parámetro. Este enfoque muestra cómo los objetos pueden interactuar entre sí y cómo los métodos pueden operar sobre datos pertenecientes a distintas instancias.

El cálculo de la distancia entre dos puntos sigue la fórmula habitual basada en el teorema de Pitágoras. Al encapsular esta operación dentro de un método, se consigue que la clase Punto ofrezca un comportamiento más completo y coherente. Además, este ejemplo permite observar cómo se combinan atributos, parámetros y la referencia this para construir métodos que dependen del estado interno del objeto. Este tipo de diseño es fundamental en la programación orientada a objetos, donde cada clase define tanto datos como operaciones relacionadas.

## 14. El paso del `Punto` como parámetro a un método, es **por copia** o **por referencia**, es decir, si se cambia el valor de algún atributo del punto pasado como parámetro, dichos cambios afectan al objeto fuera del método? ¿Qué ocurre si en vez de un `Punto`, se recibiese un entero (`int`) y dicho entero se modificase dentro de la función? 

### Respuesta
En Java, todos los parámetros se pasan por valor, pero el tipo de valor que se copia depende de si se trata de un tipo primitivo o de un objeto. Cuando se pasa un objeto como parámetro, lo que se copia es la referencia al objeto, no el objeto en sí. Esto significa que dentro del método se trabaja con la misma instancia que existe fuera, por lo que cualquier modificación realizada sobre sus atributos afecta directamente al objeto original. Este comportamiento puede recordar al paso de punteros en C, donde modificar aquello a lo que apunta el puntero afecta al valor externo.

Sin embargo, si dentro del método se reasigna la referencia (por ejemplo, p = new Punto(0,0);), esa reasignación no afecta a la variable original fuera del método, porque la referencia también se pasa por copia. Solo los cambios en los atributos del objeto compartido se reflejan externamente. Esta distinción es fundamental para comprender cómo se comportan los objetos al ser utilizados como parámetros en Java y evita confusiones comunes sobre si el lenguaje emplea paso por referencia real.

En el caso de los tipos primitivos, como int, double o boolean, el valor que se copia es simplemente el dato en sí. Por tanto, si un método recibe un entero y lo modifica dentro de su cuerpo, ese cambio no afecta al valor original fuera del método. Este comportamiento es idéntico al paso por valor tradicional en C, donde las modificaciones internas no alteran la variable externa. Así, Java mantiene un modelo coherente: siempre se pasa por valor, pero el contenido de ese valor varía según el tipo.

Este diseño permite que los objetos puedan ser modificados desde métodos sin necesidad de punteros explícitos, mientras que los tipos primitivos permanecen protegidos frente a cambios accidentales. Comprender esta diferencia resulta esencial para evitar errores lógicos y para diseñar métodos que manipulen correctamente los datos que reciben como parámetros.

## 15. ¿Qué es el método `toString()` en Java? ¿Existe en otros lenguajes? Pon un ejemplo de `toString()` en la clase `Punto` en Java

### Respuesta
El método toString() en Java es un método definido en la clase base Object, de la cual heredan todas las clases del lenguaje. Su función es devolver una representación en forma de texto del objeto, normalmente útil para depuración, impresión por consola o registro de información. Si no se sobrescribe, la implementación por defecto muestra el nombre de la clase y una referencia interna, lo cual no suele ser descriptivo. Por ello, es habitual redefinir este método para que muestre información relevante sobre el estado del objeto.

Este concepto existe también en otros lenguajes orientados a objetos, aunque con nombres distintos. En C++ puede lograrse un comportamiento similar sobrecargando el operador <<, mientras que en Python se emplean métodos como __str__ o __repr__. En todos los casos, la idea es proporcionar una forma estándar de convertir un objeto en una cadena legible, lo que facilita la inspección del estado interno durante la ejecución del programa.

A continuación 

public class Punto {
    int x;
    int y;

    public Punto(int x, int y) {
        this.x = x;
        this.y = y;
    }

    @Override
    public String toString() {
        return "Punto(" + x + ", " + y + ")";
    }
}


## 16. Reflexiona: ¿una clase es como un `struct` en C? ¿Qué le falta al `struct` para ser como una clase y las variables de ese tipo ser instancias?


### Respuesta
Un struct en C puede considerarse un precursor muy básico de una clase, ya que permite agrupar varios datos bajo un mismo tipo. Sin embargo, su capacidad se limita exclusivamente al almacenamiento de información, sin ofrecer mecanismos para asociar funciones directamente al tipo ni para controlar el acceso a los datos. Por ello, aunque conceptualmente ambos agrupan atributos, una clase representa un modelo mucho más completo y autónomo dentro del paradigma orientado a objetos.

Para que un struct se comportase como una clase, necesitaría incorporar métodos, es decir, funciones asociadas directamente al tipo y capaces de operar sobre sus datos internos. También requeriría mecanismos de encapsulación, que permitieran ocultar ciertos atributos y exponer solo aquellos necesarios mediante interfaces controladas. En C, esta separación debe hacerse manualmente mediante archivos .h y .c, mientras que en una clase forma parte del propio lenguaje.

Además, una clase necesita la capacidad de definir constructores, que inicialicen automáticamente los datos del objeto al crearlo, y destructores, que gestionen su ciclo de vida. En C, estas tareas deben realizarse de forma explícita y no están vinculadas al tipo. Finalmente, una clase permite crear instancias, que son objetos con comportamiento propio, mientras que un struct solo genera bloques de memoria sin lógica asociada. Por tanto, aunque un struct puede verse como un punto de partida, carece de los elementos esenciales que convierten a una clase en una unidad completa de datos y comportamiento.

## 17. Quitemos un poco de magia a todo esto: ¿Como se podría “emular”, con `struct` en C, la clase `Punto`, con su función para calcular la distancia al origen? ¿Qué ha pasado con `this`?

### Respuesta
Para emular una clase en C utilizando un struct, es necesario separar manualmente los datos y las funciones, ya que el lenguaje no permite asociar métodos directamente a un tipo. En este caso, el struct almacenaría las coordenadas del punto, mientras que la función encargada de calcular la distancia al origen se definiría por separado y recibiría un puntero al struct como parámetro. Este enfoque reproduce parcialmente el comportamiento de una clase, aunque de forma menos integrada y sin soporte directo del lenguaje.

En esta simulación, el equivalente a this sería simplemente el puntero que se pasa a la función. En C++, this es un puntero implícito que se recibe automáticamente en los métodos de una clase, pero en C debe proporcionarse de manera explícita. Esto obliga a que todas las funciones que operen sobre el struct reciban un puntero como argumento, lo que hace más evidente la separación entre datos y comportamiento. Aunque funcional, este modelo carece de encapsulación y de la sintaxis más natural que ofrece la programación orientada a objetos.

A continuación se muestra un ejemplo de cómo podría emularse la clase Punto en C:

#include <math.h>

typedef struct {
    int x;
    int y;
} Punto;

double calculaDistanciaAOrigen(Punto *p) {
    return sqrt(p->x * p->x + p->y * p->y);
}
