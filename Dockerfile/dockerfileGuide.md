# Guia rapida de docker file

Formato de las instrucciones
```bash
# Comment
INSTRUCTION arguments
```
Tosdos los Dockerfiles comienzan con la instruccion **FROM**  
Esta instruccion le dice a Docker que base va a utilizar para crear el contenedor.

---
## Instrucciones

### **From**
```bash
FROM < image>
FROM < image>:< tag>
FROM < image>@< digest>
```

FROM must be the first non-comment instruction in the Dockerfile.

FROM can appear multiple times within a single Dockerfile in order to create multiple images. Simply make a note of the last image ID output by the commit before each new FROM command.


The tag or digest values are optional. If you omit either of them, the builder assumes a latest by default. The builder returns an error if it cannot match the tag value.

### **RUN**

```bash
RUN <command> 
#shell form, the command is run in a shell, which by default is /bin/sh -c on Linux or cmd /S /C on Windows

RUN ["<executable>", "<param1>", "<param2>"] 
# exec form
```

### **RUN**

## Reemplazo de variables de entoro

Las variables de entorno de cada contenedor pueden ser manipuladas a traves de este archivo 


