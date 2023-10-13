# Caracteres de globbin en Linux

Los caracteres de globbing o "comodines" son caracteres especiales que se utilizan para hacer referencia a un grupo de archivos o directorios. Se utilizan en los sistemas operativos Unix y Linux, así como en otros sistemas operativos que utilizan el shell Bash.

Los caracteres globbing más comunes son:

* **" ? "** Se utiliza para hacer coincidir un carácter cualquiera en una posición determinada. Es útil para buscar archivos con nombres similares que solo difieren en un carácter.


* **" : "** Se utiliza para hacer coincidir cualquier número de caracteres dentro de un nombre. Es útil para buscar archivos con nombres que contienen una palabra o una parte de ella.


* **" [] "** Se utiliza para hacer coincidir un carácter que pertenece a un rango o a un conjunto especificado. Es útil para buscar archivos con nombres que varían en algunos caracteres dentro de un rango o un conjunto.


* **" {} "** Se utiliza para hacer coincidir un grupo de caracteres que se separan por comas. Es útil para buscar archivos con nombres que tienen varias opciones posibles.


* **" * "** Se utiliza para hacer coincidir cualquier cadena, incluyendo el carácter "/", que normalmente separa los directorios. Es útil para buscar archivos en subdirectorios sin especificar la ruta completa.

* **" ! "** El signo de exclamación se utiliza en conjunto con los corchetes para negar un intervalo. Por ejemplo, el comando echo [!DP]* mostrará cualquier archivo que no comienza con D o P.

Claro, aquí tienes la información sobre las comillas dobles, comillas simples y la barra diagonal inversa en el contexto de los caracteres globbing:

* **( " )**
Las comillas dobles se utilizan para detener la interpretación de comodines y caracteres especiales en una cadena. 

* **( ´ )**
Las comillas simples se utilizan para evitar la interpretación de variables y caracteres especiales.

* **" \ "**
La barra diagonal inversa se utiliza antes de un carácter para citarlo y tratarlo como una comilla simple. 



## Asterisco " * "
El asterisco se utiliza para representar cero o más de cualquier carácter en un nombre de archivo. Por ejemplo, supongamos que quieres visualizar todos los archivos en el directorio /etc que empiecen con la letra "t":

```bash
$ echo /etc/t*
```

Resultado:

```
/etc/terminfo /etc/timezone
```

El patrón `t*` significa "cualquier archivo que comienza con el carácter 't' y tiene cero o más de cualquier carácter después de la letra 't'".

Puedes usar el asterisco en cualquier lugar dentro del patrón del nombre de archivo. Por ejemplo, para mostrar todos los archivos en /etc que terminan con ".d":

```bash
$ echo /etc/*.d
```

Resultado:

```
/etc/apparmor.d /etc/bash_completion.d  /etc/cron.d /etc/depmod.d   /etc/fstab.d /etc/init.d /etc/insserv.conf.d /etc/ld.so.conf.d /etc/logrotate.d /etc/modprobe.d /etc/pam.d 
```

## Signo de Interrogación " ? "
El signo de interrogación representa cualquier carácter único. Cada carácter de signo de interrogación coincide con exactamente un carácter, nada más y nada menos. Por ejemplo, si quieres visualizar todos los archivos en el directorio /etc que comienzan con la letra "t" y que tienen exactamente 7 caracteres después del carácter "t":

```bash
$ echo /etc/t???????
```

Resultado:

```
/etc/terminfo /etc/timezone
```

Los comodines pueden utilizarse juntos para encontrar patrones más complejos. Por ejemplo, el comando `echo /etc/*????????????????????` imprimirá solo los archivos del directorio /etc con veinte o más caracteres en el nombre del archivo.

## Corchetes " [] "
Los corchetes se utilizan para coincidir con un carácter único representando un intervalo de caracteres que pueden coincidir con los caracteres. Por ejemplo, `echo /etc/[gu]*` imprimirá cualquier archivo que comienza con el carácter 'g' o 'u' y contiene cero o más caracteres adicionales.

```bash
$ echo /etc/[gu]*
```

Resultado:

```
/etc/gai.conf /etc/groff /etc/group /etc/group- /etc/gshadow /etc/gshadow- /etc/ucf.conf /etc/udev /etc/ufw /etc/update-motd.d /etc/updatedb.conf
```

Los corchetes también pueden ser utilizados para representar un intervalo de caracteres. Por ejemplo, el comando `echo /etc/[a-d]*` mostrará todos los archivos que comienzan con cualquier letra entre 'a' y 'd'.

## Signo de Exclamación " ! "
El signo de exclamación se utiliza en conjunto con los corchetes para negar un intervalo. Por ejemplo, el comando `echo [!DP]*` mostrará cualquier archivo que no comienza con 'D' o 'P'.

Por supuesto, aquí tienes la información en español:

### Comillas dobles ( " ), Comillas simples ( ' ) y Barra diagonal inversa ( \\ )

## Comillas dobles ( " )


   Las comillas dobles se utilizan para detener la interpretación de caracteres especiales, incluyendo comodines. Dentro de las comillas dobles, el asterisco (*) es simplemente un asterisco, un signo de interrogación (?) es solo un signo de interrogación, y así sucesivamente.

   ```bash
   $ echo "Los caracteres de comodín son *, ? y [ ]"
   ```

   Resultado:

   ```
   Los caracteres de comodín son *, ? y [ ]
   ```

## Comillas simples ( ' )

   Las comillas simples evitan que el shell interprete caracteres especiales, incluyendo comodines, variables y otros caracteres especiales. Puedes utilizar una barra diagonal inversa (\\) antes del carácter que deseas citar para tratarlo como una comilla simple.

   ```bash
   $ echo 'El coche cuesta $100'
   ```

   Resultado:

   ```
   El coche cuesta $100
   ```

## Barra diagonal inversa ( \\ )

   Puedes utilizar una barra diagonal inversa (\\) antes del carácter que deseas quitar para que se trate como una comilla simple.

   ```bash
   $ echo El coche cuesta \$100
   ```

   Resultado:

   ```
   El coche cuesta 100
   ```

### Comilla Invertida (`)

Las comillas invertidas se utilizan para especificar un comando dentro de otro comando, lo que permite ejecutar un comando y usar su salida como parte de otro comando. Por ejemplo:

```bash
$ echo Hoy es `date`
```

Resultado:

```
Hoy es Lun Nov 2 03:40:04 UTC 2015
```

En este caso, el comando `date` se ejecuta y su salida se inserta en la cadena que se muestra como resultado. Las comillas invertidas permiten la sustitución de comando y son útiles para obtener información dinámica dentro de un comando.

