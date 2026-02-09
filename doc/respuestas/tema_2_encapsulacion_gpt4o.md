<!--
Posible prompt:
<prompt>
Tengo un cuestionario con preguntas sobre "Encapsulación". Debes tener en cuenta que los conocimientos previos que tengo (y por tanto tus respuestas deben ser adaptadas), son:
- C/C++ sin orientación a objetos.
- Temas de Java previos: Clases y Objetos.

Cada respuesta debe tener entre 2 - 4 párrafos de longitud (sin contar los trozos de código).

Por favor, escribe en impersonal las respuestas.

</prompt>
----
-->
# TEMA 2. Encapsulación

## 1. En Programación Orientada a Objetos (POO), ¿Qué buscan la **encapsulación** y **la ocultación** de información? Enumera brevemente algunas ventajas de la ocultación de información.

### Respuesta
En Programación Orientada a Objetos, la encapsulación y la ocultación de información persiguen agrupar en una misma unidad los datos de un objeto y las operaciones que actúan sobre ellos, controlando además cómo se accede a dichos datos desde el exterior. A diferencia de lenguajes estructurados como C, donde las estructuras de datos suelen ser accesibles directamente, en POO se busca que el estado interno de los objetos no pueda modificarse de forma arbitraria, sino únicamente a través de métodos bien definidos.

La encapsulación permite establecer una frontera clara entre la implementación interna de una clase y su uso externo. Mediante mecanismos de visibilidad, como los modificadores de acceso en Java, se decide qué partes de la clase son accesibles y cuáles permanecen ocultas. De este modo, se protege la coherencia del objeto, evitando estados inválidos y dependencias innecesarias entre distintas partes del programa.

La ocultación de información aporta varias ventajas importantes. Entre ellas se encuentran una mayor seguridad, al impedir modificaciones directas no controladas; una mejor mantenibilidad, ya que los cambios internos en una clase no afectan al código que la utiliza; y una mayor claridad y modularidad, al obligar a interactuar con los objetos a través de interfaces bien definidas. Todo ello facilita el desarrollo de programas más robustos, comprensibles y fáciles de evolucionar.

## 2. ¿Qué se entiende por la **interfaz pública** de un objeto o clase en POO? Describe brevemente cómo se relaciona con la ocultación de información.

### Respuesta
En Programación Orientada a Objetos, la interfaz pública de una clase u objeto se entiende como el conjunto de métodos y atributos accesibles desde el exterior, que definen cómo otros elementos del programa pueden interactuar con él. Esta interfaz actúa como un contrato que especifica qué operaciones se pueden realizar sobre un objeto, sin necesidad de conocer cómo están implementadas internamente. En Java, la interfaz pública está formada por los miembros declarados con el modificador public.

La interfaz pública permite separar claramente el qué se puede hacer con un objeto del cómo se hace internamente. Mientras que el código externo solo conoce y utiliza los métodos públicos, los detalles de implementación —como variables internas, cálculos auxiliares o estructuras de apoyo— permanecen ocultos. Esta separación resulta especialmente relevante si se compara con lenguajes como C, donde el acceso a los campos de una estructura suele ser directo y sin restricciones.

La relación entre la interfaz pública y la ocultación de información es directa: la ocultación se logra precisamente limitando el acceso al estado interno del objeto y exponiendo únicamente lo necesario a través de dicha interfaz. De este modo, se evita que el resto del programa dependa de detalles internos, lo que facilita la modificación y evolución de la clase sin afectar al código que la utiliza, mejorando así la modularidad y la robustez del sistema.


## 3. Brevemente: ¿Por qué hay que ser conscientes y diseñar con cuidado la **interfaz pública** de una clase? ¿Es fácil cambiarla?

### Respuesta
La interfaz pública de una clase constituye el conjunto de elementos visibles desde el exterior, normalmente métodos y, en menor medida, constantes. Diseñarla con cuidado resulta esencial porque define cómo otras partes del programa interactúan con esa clase. Si la interfaz es confusa, demasiado amplia o expone detalles internos que no deberían conocerse, se genera una dependencia innecesaria entre módulos. Esto dificulta el mantenimiento y aumenta el riesgo de errores, ya que cualquier cambio interno puede afectar a múltiples componentes que dependen de esa interfaz.

Además, una interfaz pública mal diseñada puede obligar a mantener decisiones internas que ya no resultan adecuadas. En Java, modificar la implementación privada es sencillo siempre que la interfaz pública permanezca estable. Sin embargo, cambiar esa interfaz no es trivial, porque implica revisar y adaptar todo el código que la utiliza. En proyectos grandes, esto puede suponer un impacto considerable, ya que la interfaz actúa como un contrato que otros desarrolladores o módulos esperan que se mantenga.

Por este motivo, se recomienda exponer únicamente lo necesario y mantener ocultos los detalles internos mediante encapsulación. Una interfaz pública bien pensada permite evolucionar la clase sin romper el código existente, favoreciendo la modularidad y la reutilización. En cambio, una interfaz improvisada o demasiado abierta limita la capacidad de modificar o mejorar la clase en el futuro.

## 4. ¿Qué son las **invariantes de clase** y por qué la ocultación de información nos ayuda?

### Respuesta
Las invariantes de clase se entienden como condiciones lógicas que deben cumplirse siempre para que un objeto sea válido. Estas condiciones describen el estado coherente que la clase garantiza mantener, por ejemplo, que un atributo numérico nunca sea negativo o que una colección interna no contenga valores nulos. Aunque no se expresan explícitamente en el código como una característica del lenguaje, se reflejan en las restricciones que se aplican dentro de los métodos y en la forma en que se controla el acceso a los atributos.

La ocultación de información contribuye directamente a mantener estas invariantes, porque impide que el código externo modifique los atributos de manera arbitraria. Al declarar los campos como private y proporcionar métodos controlados para modificarlos, la clase puede validar los datos antes de aceptarlos y evitar estados inconsistentes. Esto permite que la lógica interna se mantenga bajo control y que las invariantes se preserven sin depender del comportamiento de otros módulos.

Además, la encapsulación facilita que las invariantes evolucionen con el tiempo sin afectar al resto del programa. Si se decide cambiar la forma en que se valida un dato o se ajustan las reglas internas, basta con modificar la implementación privada, manteniendo intacta la interfaz pública. De esta manera, la clase conserva su integridad y se reduce el riesgo de errores derivados de un uso incorrecto de sus atributos.


## 5. Pon un ejemplo de una clase `Punto` en `Java`, con dos coordenadas, `x` e `y`, de tipo `double`, con un método `calcularDistanciaAOrigen`, y que haga uso de la ocultación de información. ¿Cuál es la interfaz pública de la clase `Punto`? ¿Qué significa `public` y `private`?

### Respuesta
public class Punto {
    private double x;
    private double y;

    public Punto(double x, double y) {
        this.x = x;
        this.y = y;
    }

    public double getX() {
        return x;
    }

    public double getY() {
        return y;
    }

    public double calcularDistanciaAOrigen() {
        return Math.sqrt(x * x + y * y);
    }
}
La interfaz pública de esta clase está formada por el constructor Punto(double, double), los métodos getX(), getY() y el método calcularDistanciaAOrigen(). Estos elementos constituyen el conjunto de operaciones accesibles desde fuera de la clase y permiten crear objetos, consultar sus coordenadas y obtener la distancia al origen sin exponer directamente cómo se almacenan o gestionan internamente los datos.

El modificador public indica que un elemento puede ser utilizado desde cualquier parte del programa, siempre que se tenga acceso a la clase. Esto permite que otros módulos creen objetos de tipo Punto y llamen a sus métodos públicos. Por el contrario, private restringe el acceso exclusivamente al interior de la propia clase, impidiendo que el código externo modifique directamente los atributos x e y. Gracias a esta separación, se protege el estado interno del objeto y se favorece la encapsulación.

## 6. En Java, ¿A quiénes se pueden aplicar los modificadores `public` o `private`?

### Respuesta
En Java, los modificadores public y private pueden aplicarse tanto a clases como a los elementos que contienen, aunque con ciertas limitaciones según el contexto. En el caso de las clases, solo las clases de nivel superior pueden ser public, mientras que no pueden ser private. Las clases internas, en cambio, sí pueden declararse como public, private o incluso protected, ya que forman parte de otra clase y no del nivel superior del archivo.

En cuanto a los miembros de una clase, los modificadores public y private pueden aplicarse a atributos, métodos y constructores. Esto permite controlar qué partes del código externo pueden acceder a ellos y cuáles deben permanecer ocultas. Los atributos suelen declararse como private para proteger el estado interno del objeto, mientras que los métodos que forman parte de la interfaz pública se declaran como public.

También es posible aplicar estos modificadores a clases internas estáticas o no estáticas, lo que permite encapsular comportamientos auxiliares dentro de una clase principal. De esta manera, Java ofrece un control detallado sobre la visibilidad y el acceso, favoreciendo la encapsulación y el diseño modular del código.


## 7. En POO, la visibilidad puede ser pública o privada, pero ¿existen más tipos de visibilidad? ¿Qué ocurre en Java? ¿Y en otros lenguajes?

### Respuesta
En programación orientada a objetos existen más niveles de visibilidad además de lo público y lo privado, aunque su disponibilidad depende del lenguaje. La visibilidad define hasta qué punto una parte del código puede acceder a clases, atributos o métodos, y constituye un mecanismo fundamental para controlar la encapsulación. En general, los lenguajes orientados a objetos ofrecen varios grados intermedios para ajustar con precisión qué se expone y qué se oculta.

En Java existen cuatro niveles de visibilidad: public, private, protected y el nivel package‑private (también llamado “por defecto”), que se aplica cuando no se especifica ningún modificador. public permite el acceso desde cualquier parte del programa, mientras que private lo restringe exclusivamente a la propia clase. protected permite el acceso desde la clase, sus subclases y otras clases del mismo paquete. Por último, el nivel package‑private permite el acceso únicamente desde clases del mismo paquete, lo que favorece la organización modular sin necesidad de exponer elementos al exterior.

En otros lenguajes orientados a objetos pueden encontrarse variaciones de estos niveles. Por ejemplo, C++ ofrece public, private y protected, pero su comportamiento difiere en algunos detalles, especialmente en relación con la herencia y el acceso a miembros. Lenguajes como C# incluyen también niveles intermedios como internal o combinaciones como protected internal, que permiten ajustar aún más la visibilidad según el ensamblado o la jerarquía de clases. Estas diferencias muestran que, aunque la idea general es común, cada lenguaje adapta los niveles de visibilidad a su propio modelo de organización y encapsulación.

## 8. Responde: Los miembros de instancia privados de un objeto están ocultos para (a) otras clases o (b) otras instancias, aunque sean de la misma clase. Pon un ejemplo añadiendo un método `calcularDistanciaAPunto(Punto otro)` y explica la respuesta.

### Respuesta
Los miembros de instancia privados están ocultos para otras clases, pero no para otras instancias de la misma clase. Esto significa que el código externo no puede acceder directamente a esos atributos, pero cualquier método definido dentro de la propia clase sí puede leerlos o modificarlos, incluso cuando pertenecen a otro objeto del mismo tipo. Esta característica permite que una clase implemente operaciones que comparan o combinan información entre dos objetos sin romper la encapsulación.

En Java, un método de la clase puede acceder a los atributos privados de cualquier instancia de esa misma clase, porque la visibilidad se evalúa por clase y no por objeto. Esto permite implementar métodos como el cálculo de la distancia entre dos puntos sin necesidad de exponer los atributos x e y públicamente. De esta forma, se mantiene la ocultación de información y se evita que otras partes del programa manipulen directamente los datos internos.

public class Punto {
    private double x;
    private double y;

    public Punto(double x, double y) {
        this.x = x;
        this.y = y;
    }

    public double calcularDistanciaAPunto(Punto otro) {
        double dx = this.x - otro.x;   // Acceso permitido: misma clase
        double dy = this.y - otro.y;
        return Math.sqrt(dx * dx + dy * dy);
    }
}

En este ejemplo, el método calcularDistanciaAPunto accede directamente a otro.x y otro.y, aunque sean privados. Esto es válido porque el acceso ocurre dentro de la propia clase Punto. Si otra clase intentara acceder a esos atributos, el compilador lo impediría. Así, Java permite que los objetos cooperen entre sí dentro de la misma clase sin comprometer la encapsulación frente al exterior.

## 9. ¿Qué son los métodos "getter" y "setter" en los lenguajes orientados a objetos?

### Respuesta
Los métodos getter y setter son funciones utilizadas en programación orientada a objetos para acceder y modificar atributos que están ocultos mediante encapsulación. Cuando los atributos se declaran como private, no pueden ser leídos ni cambiados directamente desde fuera de la clase. Los getters permiten obtener el valor de un atributo, mientras que los setters permiten modificarlo de forma controlada, aplicando validaciones si es necesario. De este modo, la clase mantiene el control sobre su propio estado interno.

Estos métodos forman parte habitual de la interfaz pública de una clase, ya que proporcionan un punto de acceso seguro a los datos encapsulados. Un getter suele devolver el valor de un atributo sin modificarlo, mientras que un setter recibe un parámetro y lo asigna al atributo correspondiente, pudiendo comprobar previamente si el valor es válido. Este patrón evita que el código externo manipule directamente los datos internos y permite mantener las invariantes de clase.

En muchos lenguajes orientados a objetos, como Java, este enfoque es una práctica estándar para garantizar la integridad del objeto. Aunque pueda parecer más verboso que acceder directamente a los atributos, ofrece flexibilidad para cambiar la implementación interna sin afectar al código que utiliza la clase. Además, permite añadir lógica adicional, como restricciones, cálculos derivados o notificaciones, sin modificar la interfaz pública.

## 10. Cuando nos referimos a que la ocultación de información mejora la "seguridad" del programa, ¿nos referimos a que no pueda ser "hackeado"?

### Respuesta
Cuando se afirma que la ocultación de información mejora la “seguridad” del programa, no se hace referencia a evitar ataques externos o impedir que el sistema sea “hackeado”. El término se utiliza en un sentido más limitado y propio del diseño de software, relacionado con la integridad y el correcto funcionamiento interno del programa. La idea principal es que, al restringir el acceso directo a los datos, se reduce la posibilidad de que otras partes del código los modifiquen de forma incorrecta o inesperada.

Esta forma de seguridad se centra en evitar errores lógicos, estados inconsistentes y dependencias innecesarias entre módulos. Al mantener los atributos privados y controlar su modificación mediante métodos bien definidos, la clase puede garantizar que sus invariantes se cumplan y que su comportamiento sea predecible. Esto protege al programa de fallos provocados por un uso indebido de sus componentes, no de amenazas externas.

En lenguajes como Java, la encapsulación actúa como una barrera que separa la implementación interna de la interfaz pública. Gracias a ello, se puede modificar la estructura interna sin afectar al resto del sistema, lo que contribuye a un software más robusto y fácil de mantener. Por tanto, la “seguridad” mencionada se refiere a la fiabilidad y estabilidad del código, no a la protección frente a ataques informáticos.

## 11. ¿Qué diferencia hay entre **miembro de instancia** y **miembro de clase**? ¿Los miembros de clase también se pueden ocultar?

### Respuesta
Un miembro de instancia es un atributo o método cuyo comportamiento depende de cada objeto concreto creado a partir de una clase. Cada instancia mantiene su propia copia de esos atributos, de modo que modificar el valor en un objeto no afecta a los demás. Este tipo de miembros representa el estado particular de cada objeto y constituye la base del funcionamiento orientado a objetos, donde cada instancia mantiene su propia identidad y datos internos.

Por otro lado, un miembro de clase (también llamado estático) pertenece a la clase en sí misma y no a los objetos individuales. Esto significa que existe una única copia compartida por todas las instancias, y puede utilizarse incluso sin crear objetos. Los miembros estáticos se emplean para información o comportamientos que no dependen del estado particular de un objeto, como contadores globales o utilidades comunes.

En cuanto a la ocultación, los miembros de clase también pueden declararse como private, igual que los miembros de instancia. Esto permite restringir su acceso únicamente a la propia clase, evitando que otras clases modifiquen valores compartidos que podrían afectar al comportamiento global. De esta forma, la encapsulación se aplica tanto a los elementos individuales de cada objeto como a los elementos compartidos por toda la clase, manteniendo el control sobre la integridad del sistema.

## 12. Brevemente: ¿Tiene sentido que los constructores sean privados?

### Respuesta
Sí, tiene sentido que los constructores sean privados en ciertos diseños, aunque no sea lo más habitual. Un constructor privado impide que otras clases creen instancias directamente, lo que permite controlar completamente cómo y cuándo se generan los objetos. Esta técnica se utiliza cuando la creación libre de instancias podría romper alguna invariante o cuando se desea limitar el número de objetos existentes.

Un caso típico es el patrón Singleton, donde solo debe existir una única instancia de la clase. Al declarar el constructor como privado, se evita que el código externo cree nuevos objetos y se obliga a utilizar un método estático que devuelve siempre la misma instancia. También es útil en clases que proporcionan únicamente métodos estáticos o en aquellas donde la creación de objetos debe pasar por métodos de fábrica que aplican validaciones o configuraciones específicas.

Además, los constructores privados pueden emplearse para evitar que una clase sea instanciada cuando su propósito no es representar objetos, sino agrupar utilidades o constantes. En estos casos, el constructor privado actúa como una protección adicional frente a usos incorrectos. Por tanto, aunque no sea la opción más común, declarar constructores privados es una herramienta válida y útil dentro del diseño orientado a objetos.

## 13. ¿Cómo se indican los **miembros de clase** en Java? Pon un ejemplo, en la clase `Punto` definida anteriormente, para que incluya miembros de clase que permitan saber cuáles son los valores `x` e `y` máximos que se han establecido en todos los puntos que se hayan creado hasta el momento.

### Respuesta
En Java, los miembros de clase se indican utilizando la palabra clave static. Este modificador señala que el atributo o método pertenece a la clase en sí misma y no a cada instancia individual. Como consecuencia, existe una única copia compartida por todos los objetos creados, lo que permite almacenar información global o realizar operaciones que no dependen del estado particular de un objeto concreto. Este mecanismo resulta útil para mantener datos agregados o comportamientos comunes que deben ser accesibles sin necesidad de crear instancias.

En el caso de la clase Punto, puede añadirse dos miembros de clase que registren los valores máximos de x e y que se hayan asignado en cualquier punto creado. Para ello, se declaran como atributos static y se actualizan dentro del constructor cada vez que se crea un nuevo objeto. De esta forma, la clase mantiene un registro global sin exponer directamente los detalles internos de cada instancia. Además, estos miembros pueden declararse como private para mantener la encapsulación y ofrecer métodos públicos que permitan consultarlos.

public class Punto {
    private double x;
    private double y;

    private static double maxX = Double.NEGATIVE_INFINITY;
    private static double maxY = Double.NEGATIVE_INFINITY;

    public Punto(double x, double y) {
        this.x = x;
        this.y = y;

        if (x > maxX) maxX = x;
        if (y > maxY) maxY = y;
    }

    public static double getMaxX() {
        return maxX;
    }

    public static double getMaxY() {
        return maxY;
    }
}


## 14. Como sería un método factoría dentro de la clase `Punto` para construir un `Punto` a partir de dos coordenadas, pero que las redondee al entero más cercano. Escribe sólo el código del método, no toda la clase ¿Has usado `static`? 

### Respuesta
public static Punto crearRedondeado(double x, double y) {
    return new Punto(Math.round(x), Math.round(y));
}


## 15. Cambia la implementación de `Punto`. En vez de dos `double`, emplea un array interno de dos posiciones, intentando no modificar la interfaz pública de la clase.

### Respuesta
private double[] coords = new double[2];

public Punto(double x, double y) {
    coords[0] = x;
    coords[1] = y;
}

public double getX() {
    return coords[0];
}

public double getY() {
    return coords[1];
}

public double calcularDistanciaAOrigen() {
    return Math.sqrt(coords[0] * coords[0] + coords[1] * coords[1]);
}


## 16. Si un atributo va a tener un método "getter" y "setter" públicos, ¿no es mejor declararlo público? ¿Cuál es la convención más habitual sobre los atributos, que sean públicos o privados? ¿Tiene esto algo que ver con las "invariantes de clase"?

### Respuesta
Declarar un atributo como público no suele considerarse una buena práctica, incluso cuando se planea proporcionar métodos getter y setter. La razón principal es que, al exponer directamente el atributo, se pierde la posibilidad de controlar su acceso y de garantizar que el objeto mantenga siempre un estado válido. En cambio, los métodos permiten introducir validaciones, restricciones o transformaciones sin modificar la interfaz pública, lo que ofrece mucha más flexibilidad a largo plazo.

La convención más habitual en los lenguajes orientados a objetos, y especialmente en Java, es declarar todos los atributos como privados. Esta práctica forma parte del principio de encapsulación y se considera un estándar de diseño. Los atributos privados obligan a que cualquier acceso pase por métodos controlados, lo que facilita mantener la coherencia interna del objeto y evita dependencias innecesarias con el código externo.

Esta decisión está directamente relacionada con las invariantes de clase, que representan las condiciones que deben cumplirse para que un objeto sea válido. Si los atributos fueran públicos, cualquier parte del programa podría modificarlos sin restricciones, poniendo en riesgo esas invariantes. En cambio, al mantenerlos privados y controlar su modificación mediante setters, la clase puede asegurarse de que los valores asignados respeten siempre las reglas internas, preservando así la integridad del objeto.

## 17. ¿Qué significa que una clase sea **inmutable**? ¿qué es un método modificador? ¿Un método modificador es siempre un "setter"? ¿Tiene ventajas que una clase sea inmutable?

### Respuesta
Una clase inmutable es aquella cuyo estado no puede cambiar después de haberse creado el objeto. Esto implica que todos sus atributos deben inicializarse en el constructor y no existir métodos que modifiquen esos valores posteriormente. En este tipo de clases, cualquier operación que conceptualmente “cambie” el objeto devuelve una nueva instancia, manteniendo intacto el objeto original. Este enfoque resulta especialmente útil cuando se desea garantizar que los datos no se alteren accidentalmente y que el comportamiento del objeto sea completamente predecible.

Un método modificador es aquel que altera el estado interno del objeto, normalmente cambiando el valor de uno o varios atributos. Aunque los setters son un tipo de método modificador, no todos los métodos modificadores son setters. Por ejemplo, un método que actualiza varias propiedades a la vez, o que realiza una operación compleja que termina alterando el estado, también se considera modificador aunque no tenga la forma típica de un setter.

La inmutabilidad ofrece varias ventajas importantes. Al no poder cambiar el estado de los objetos, se evitan problemas relacionados con efectos secundarios, estados inconsistentes o dependencias inesperadas entre distintas partes del programa. Además, las clases inmutables son más fáciles de razonar, más seguras en entornos concurrentes y permiten mantener invariantes de clase de forma natural, ya que el estado no puede violarse después de la construcción. Por estas razones, la inmutabilidad es un recurso valioso dentro del diseño orientado a objetos.

## 18. ¿Es recomendable incluir métodos "setter" siempre y como convención?

### Respuesta
No es recomendable incluir métodos setter de manera automática ni como una convención general. Aunque puedan parecer una extensión natural de los getters, su presencia implica que el estado del objeto puede modificarse libremente desde el exterior, lo que reduce el control sobre la coherencia interna. Incluir setters sin necesidad real puede debilitar la encapsulación y hacer que la clase sea más difícil de mantener, ya que cualquier parte del programa podría alterar atributos que quizá deberían permanecer estables.

La práctica habitual en diseño orientado a objetos, especialmente en Java, es declarar los atributos como privados y proporcionar setters solo cuando exista una razón clara para permitir la modificación externa. Si un atributo no debe cambiar después de la construcción, o si su modificación requiere validaciones complejas, es preferible no ofrecer un setter. De este modo, la clase conserva un mayor control sobre su propio estado y se evita que el código externo introduzca inconsistencias.

Esta decisión está estrechamente relacionada con las invariantes de clase, que representan las condiciones que deben cumplirse para que un objeto sea válido. Permitir modificaciones indiscriminadas mediante setters puede poner en riesgo esas invariantes, mientras que restringir o eliminar los setters ayuda a preservarlas. Por ello, la inclusión de un setter debe ser una decisión consciente y justificada, no una convención aplicada de forma automática.

## 19. ¿La clase `String` en Java es mutable o inmutable? ¿Qué ocurre al concatenar dos cadenas? ¿Qué debemos hacer si vamos a hacer una operación que implique concatenar muchas veces para construir paso a paso una cadena muy larga?

### Respuesta
La clase String en Java es inmutable, lo que significa que una vez creada una cadena, su contenido no puede modificarse. Cada operación que parezca alterar una cadena, como concatenar o reemplazar caracteres, en realidad genera un nuevo objeto String, dejando intacto el original. Esta decisión de diseño aporta seguridad, evita efectos secundarios y facilita el uso de cadenas en estructuras como tablas hash.

Cuando se concatenan dos cadenas usando el operador +, Java crea internamente un nuevo objeto String que contiene el resultado. Esto implica que, si se realizan muchas concatenaciones sucesivas dentro de un bucle, se estarán creando múltiples objetos intermedios, lo que puede afectar al rendimiento. Aunque este comportamiento es transparente para el programador, puede resultar ineficiente en operaciones repetitivas o de gran volumen.

Para construir una cadena muy larga mediante concatenaciones repetidas, la práctica recomendada es utilizar clases mutables como StringBuilder o StringBuffer. Estas clases permiten modificar el contenido sin crear objetos nuevos en cada operación, lo que mejora significativamente la eficiencia. Una vez completada la construcción, puede obtenerse el resultado final mediante el método toString(), combinando así eficiencia interna con la inmutabilidad externa de String

## 20. En POO ¿Cómo se comparan objetos de una misma clase? ¿Por su contenido o por su identidad? ¿Qué es el método equals en Java? ¿Qué hace por defecto? ¿Cómo se deben comparar dos cadenas en Java? 

### Respuesta
En programación orientada a objetos, los objetos pueden compararse por identidad o por contenido, dependiendo de lo que se desee comprobar. La identidad se refiere a si dos referencias apuntan exactamente al mismo objeto en memoria, mientras que el contenido evalúa si ambos objetos representan la misma información aunque sean instancias distintas. En Java, el operador == compara identidad, por lo que solo devuelve true si ambas referencias señalan al mismo objeto.

El método equals es el mecanismo estándar en Java para comparar objetos por su contenido. Todas las clases heredan una versión por defecto de equals desde Object, pero esta implementación compara identidad, no contenido. Por ello, si se desea que dos objetos se consideren iguales cuando sus atributos coinciden, es necesario sobrescribir equals en la clase correspondiente. Este método permite definir qué significa “ser igual” para cada tipo de objeto, lo que resulta esencial en estructuras como listas, conjuntos o mapas.

En el caso de las cadenas, Java proporciona una implementación específica de equals en la clase String que compara el contenido carácter por carácter. Por este motivo, dos cadenas con el mismo texto deben compararse usando equals y no con ==, ya que este último solo indicaría si ambas referencias apuntan al mismo objeto. Así, la comparación correcta entre cadenas es:

if (cadena1.equals(cadena2)) {
    // Son iguales por contenido
}


## 21. ¿Qué son las clases "wrapper" en un lenguaje de programación orientado a objetos? ¿Cómo se hace? ¿Es un proceso automático? ¿Qué ventajas tienen? ¿Todos los lenguajes orientados a objetos tienen tipos primitivos y necesitan wrappers? 

### Respuesta
Las clases wrapper son clases que encapsulan un valor de un tipo primitivo dentro de un objeto. Su propósito es permitir que valores como int, double o boolean puedan utilizarse en contextos donde solo se aceptan objetos, como colecciones genéricas o ciertos mecanismos de la biblioteca estándar. En Java, cada tipo primitivo tiene su correspondiente clase wrapper, como Integer, Double o Boolean, lo que permite tratarlos como objetos sin perder su valor básico.

En Java, la conversión entre un tipo primitivo y su wrapper puede hacerse de forma explícita, creando un objeto a partir del valor primitivo, o de forma automática mediante autoboxing y unboxing. Esto significa que el lenguaje convierte automáticamente un int en un Integer cuando es necesario, y viceversa, sin que el programador tenga que escribir código adicional. Este proceso simplifica el uso de tipos primitivos en estructuras como ArrayList<Integer>, donde solo se aceptan objetos.

Las clases wrapper ofrecen ventajas como la posibilidad de almacenar valores nulos, utilizar métodos adicionales (por ejemplo, para convertir cadenas a números) y participar en estructuras de datos orientadas a objetos. Además, permiten unificar el tratamiento de valores primitivos y objetos en ciertos contextos, lo que facilita la programación genérica. Sin embargo, su uso excesivo puede tener un coste en rendimiento debido a la creación de objetos adicionales.

No todos los lenguajes orientados a objetos tienen tipos primitivos separados de los objetos. Lenguajes como Python o Ruby tratan todos los valores como objetos, por lo que no necesitan wrappers. En cambio, lenguajes como Java o C# mantienen tipos primitivos por razones de eficiencia, y por ello requieren clases wrapper para integrarlos en su modelo orientado a objetos.


## 22. ¿En POO qué es un **tipo de dato enumerado**? ¿En Java, un tipo de dato enumerado es una clase? ¿Qué ventajas tienen en términos de encapsulación los enumerados en Java?

### Respuesta
Un tipo de dato enumerado (o enum) en programación orientada a objetos es un tipo cuyos valores posibles están cerrados y predefinidos. Sirve para representar conjuntos finitos y bien definidos, como los días de la semana, los palos de una baraja o los estados de un proceso. Su objetivo es evitar valores inválidos y hacer el código más claro y seguro.

En Java, un enumerado es realmente una clase especial. Cada valor del enum es una instancia única creada automáticamente por el propio lenguaje. Además, un enum puede tener atributos, métodos, constructores privados e incluso implementar interfaces, lo que lo convierte en una herramienta mucho más potente que los enumerados tradicionales de otros lenguajes.

Los enumerados en Java aportan ventajas importantes en términos de encapsulación:

Conjunto cerrado de valores: no se pueden crear valores nuevos fuera del propio enum, lo que evita errores y garantiza que solo existan los valores válidos.

Constructor privado implícito: impide que el programador cree instancias adicionales, reforzando la integridad del tipo.

Posibilidad de añadir comportamiento: la lógica relacionada con cada valor puede encapsularse dentro del propio enum, evitando dispersar código por el programa.

Mayor seguridad semántica: evita el uso de enteros o cadenas para representar conceptos que tienen un conjunto limitado de opciones, reduciendo errores y mejorando la legibilidad.

## 23. Crea un tipo enumerado en Java que se llame `Mes`, con doce posibles instancias y que además proporcione métodos para obtener cuántos días tiene ese mes, el ordinal de ese mes en el año (1-12), empleando atributos privados y constructores del tipo enumerado. Añade además cuatro métodos para devolver si ese mes tiene algunos días de invierno, primavera, verano u otoño, indicando con un booleano el hemisferio (norte o sur, parámetro `enHemisferioNorte`). Es decir: `esDePrimavera(boolean esHemisferioNorte)`, `esDeVerano(boolean esHemisferioNorte)`, `esDeOtoño(boolean esHemisferioNorte)`, `esDeInvierno(boolean esHemisferioNorte)`

### Respuesta
public enum Mes {

    ENERO(31, 1),
    FEBRERO(28, 2),
    MARZO(31, 3),
    ABRIL(30, 4),
    MAYO(31, 5),
    JUNIO(30, 6),
    JULIO(31, 7),
    AGOSTO(31, 8),
    SEPTIEMBRE(30, 9),
    OCTUBRE(31, 10),
    NOVIEMBRE(30, 11),
    DICIEMBRE(31, 12);

    private final int dias;
    private final int ordinal;

    Mes(int dias, int ordinal) {
        this.dias = dias;
        this.ordinal = ordinal;
    }

    public int getDias() {
        return dias;
    }

    public int getOrdinal() {
        return ordinal;
    }

    public boolean esDePrimavera(boolean enHemisferioNorte) {
        if (enHemisferioNorte) {
            return this == MARZO || this == ABRIL || this == MAYO;
        } else {
            return this == SEPTIEMBRE || this == OCTUBRE || this == NOVIEMBRE;
        }
    }

    public boolean esDeVerano(boolean enHemisferioNorte) {
        if (enHemisferioNorte) {
            return this == JUNIO || this == JULIO || this == AGOSTO;
        } else {
            return this == DICIEMBRE || this == ENERO || this == FEBRERO;
        }
    }

    public boolean esDeOtono(boolean enHemisferioNorte) {
        if (enHemisferioNorte) {
            return this == SEPTIEMBRE || this == OCTUBRE || this == NOVIEMBRE;
        } else {
            return this == MARZO || this == ABRIL || this == MAYO;
        }
    }

    public boolean esDeInvierno(boolean enHemisferioNorte) {
        if (enHemisferioNorte) {
            return this == DICIEMBRE || this == ENERO || this == FEBRERO;
        } else {
            return this == JUNIO || this == JULIO || this == AGOSTO;
        }
    }
}

