# Guia rapida de docker file

## Indice

- [Que es?](#Que-es?)
- [Formato de las instrucciones](#Formato-de-las-instrucciones)
- [Up](#Guia-rapida-de-docker-file)

---

## Que es?

Es un archivo en el cual escribimos una secuencia de instrucciones para facilitar el proceso de construccion de una imagen evitando tener que pasar estas como parametros al usar el comando build.

Tosdos los Dockerfiles comienzan con la instruccion **FROM**  
Esta instruccion le dice a Docker que base va a utilizar para crear el contenedor.

Se agregara un ejemplo de dockerfile en el futuro

[Up](#Guia-rapida-de-docker-file)

---

## Formato de las instrucciones

```bash
# Comment
INSTRUCTION arguments
```

[Up](#Guia-rapida-de-docker-file)

---

## Instrucciones

### **From**

```bash
FROM [--platform=<platform>] <image> [AS <name>]
FROM [--platform=<platform>] <image>[:<tag>] [AS <name>]
FROM [--platform=<platform>] <image>[@<digest>] [AS <name>]
```

Debe ser de la primera instruccion de montaje que aparezca en el Dockerfile y debe indicar la ruta de una imagen local o de algun repositorio

---

### **RUN**

```bash
RUN <instruction> <command> 
#shell form, the command is run in a shell, which by default is /bin/sh -c on Linux or cmd /S /C on Windows

RUN ["<executable command>", "<param1>", "<param2>"] 
# exec form
```

Ejecuta comando que crean capas nuevas a la imagen que se esta construyendo.

Este tiene dos modos de invocarse

- Exec Form:
  - Puede ejecutar un parametro a la vez de manera convencional (existe una forma adicional )
  - Comandos escritos en notacion Arra de JSON
- Shell Form:
  - Puede ejecutar varios comandos en secuencia
  - Comandos escritos en notacion de Shell
asdasd

### **RUN**

## Reemplazo de variables de entoro

Las variables de entorno de cada contenedor pueden ser manipuladas a traves de este archivo.

---
## Glosario

Contexto: El el conjunto de archivos en una ruta especifica (local | url) que se utilizaran en el proceso de construccion de una imagen.

---

[Home](#Guia-rapida-de-docker-file) / [Up](#Guia-rapida-de-docker-file)