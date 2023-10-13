
# Instrucciones de Control
Las instrucciones de control te permiten utilizar varios comandos a la vez o ejecutar comandos adicionales, dependiendo del éxito de un comando anterior. Normalmente estas instrucciones de control se utilizan en scripts o secuencias de comandos, pero también pueden ser utilizadas en la línea de comandos.

**Punto y Coma (;):**

El punto y coma (`;`) permite ejecutar varios comandos uno después del otro, sin importar el resultado del comando anterior. Cada comando se ejecuta de forma independiente y consecutiva. Esto es útil cuando deseas ejecutar múltiples comandos en secuencia.

Ejemplo:

```bash
$ cal 1 2015; cal 2 2015; cal 3 2015
```

En este caso, los comandos `cal 1 2015`, `cal 2 2015` y `cal 3 2015` se ejecutarán en ese orden, independientemente de si alguno de ellos falla. Esto significa que incluso si uno de los comandos falla, los siguientes comandos se ejecutarán. En este ejemplo, se generarán los calendarios de enero, febrero y marzo de 2015, independientemente de si alguno de ellos tiene éxito o no.

**Ampersand Doble (&&):**

El ampersand doble (`&&`) actúa como un operador "y" lógico. Si el primer comando tiene éxito (es decir, no genera errores), entonces se ejecutará el segundo comando. Si el primer comando falla, el segundo no se ejecutará. Es útil cuando deseas ejecutar un comando dependiendo del éxito del anterior.

Ejemplo:

```bash
$ ls /etc/xml && echo success
```

En este ejemplo, si el directorio `/etc/xml` existe, se mostrará "success". Si no existe, el comando `echo success` no se ejecutará. Esto significa que el segundo comando se ejecuta condicionalmente, basado en el éxito del primero.

**Línea Vertical Doble (||):**

La línea vertical doble (`||`) actúa como un operador "o" lógico. Si el primer comando falla, se ejecutará el segundo comando. Si el primer comando tiene éxito, el segundo no se ejecutará. Esto es útil cuando deseas ejecutar un comando alternativo si el primero falla.

Ejemplo:

```bash
$ ls /etc/junk || echo failed
```

En este caso, si el directorio `/etc/junk` no existe (lo que provocará un fallo en el comando `ls`), se mostrará "failed". Si el directorio existe, el comando `echo failed` no se ejecutará. Esto permite ejecutar un comando alternativo cuando el primero falla.

Estos operadores son fundamentales en scripts de shell y automatización de tareas, ya que te permiten controlar el flujo de ejecución de comandos en función de sus resultados.