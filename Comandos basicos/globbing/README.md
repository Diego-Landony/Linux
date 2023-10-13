# Caracteres de globbin en Linux

Los caracteres de globbing o "comodines" son caracteres especiales que se utilizan para hacer referencia a un grupo de archivos o directorios. Se utilizan en los sistemas operativos Unix y Linux, así como en otros sistemas operativos que utilizan el shell Bash.

Los caracteres globbing más comunes son:

* **" ? "** Se utiliza para hacer coincidir un carácter cualquiera en una posición determinada. Es útil para buscar archivos con nombres similares que solo difieren en un carácter.


* **" : "** Se utiliza para hacer coincidir cualquier número de caracteres dentro de un nombre. Es útil para buscar archivos con nombres que contienen una palabra o una parte de ella.


* **" [] "** Se utiliza para hacer coincidir un carácter que pertenece a un rango o a un conjunto especificado. Es útil para buscar archivos con nombres que varían en algunos caracteres dentro de un rango o un conjunto.


* **" {} "** Se utiliza para hacer coincidir un grupo de caracteres que se separan por comas. Es útil para buscar archivos con nombres que tienen varias opciones posibles.


* **" * "** Se utiliza para hacer coincidir cualquier cadena, incluyendo el carácter "/", que normalmente separa los directorios. Es útil para buscar archivos en subdirectorios sin especificar la ruta completa.


# Ejemplos de uso: 



## " ? " 
Para buscar archivos con nombres similares que solo difieren en un carácter, puedes usar el carácter `?`. Por ejemplo, si tienes archivos con nombres como `file1.txt`, `file2.txt`, y `file3.txt`, puedes buscar todos los archivos que contienen la palabra "file" y un carácter adicional con el siguiente comando:

```bash
$ ls file?.txt
```

Resultado:

```
file1.txt  file2.txt  file3.txt
```

## " * "
Para buscar archivos con nombres que contienen una palabra o una parte de ella, puedes usar el carácter `*`. Por ejemplo, si tienes archivos con nombres como `document1.txt`, `document2.txt`, y `document3.txt`, puedes buscar todos los archivos que contienen la palabra "document" con el siguiente comando:

```bash
$ ls document*.txt
```

Resultado:

```
document1.txt  document2.txt  document3.txt
```

## " [] "
Para buscar archivos con nombres que varían en algunos caracteres dentro de un rango o un conjunto, puedes usar el carácter `[]`. Por ejemplo, si tienes archivos con nombres como `file1.txt`, `file2.txt`, y `file3.txt`, puedes buscar todos los archivos que contienen la palabra "file" y un número del 1 al 3 con el siguiente comando:

```bash
$ ls file[1-3].txt
```

Resultado:

```
file1.txt  file2.txt  file3.txt
```

## " {} "
Para buscar archivos con nombres que tienen varias opciones posibles, puedes usar el carácter `{}`. Por ejemplo, si tienes archivos con nombres como `image1.jpg`, `image2.jpg`, y `image3.jpg`, puedes buscar todos los archivos que contienen la palabra "image" y los números 1 y 2 con el siguiente comando:

```bash
$ ls image{1,2}.jpg
```

Resultado:

```
image1.jpg  image2.jpg
```

## " * "
Para buscar archivos en subdirectorios sin especificar la ruta completa, puedes usar el carácter `*`. Por ejemplo, si tienes un archivo llamado `example.txt` en un subdirectorio llamado `subdir`, puedes buscarlo con el siguiente comando:

```bash
$ ls subdir/*.txt
```

Resultado: (Si existe el archivo `example.txt` en el subdirectorio `subdir`)

```
subdir/example.txt
```