# Bash y docker  
Linux es un sistema operativo como windows o mac mientras que Bash es el lenguaje de la terminal de linux que nos permite manipular muchos archivos a la vez. Docker en cambio es un empacador de programas de linux y sus dependencias que facilita compartir software de análisis científicos. En esta sección hablaremos de estas dos herramientas.   

## Bash  
### El sistema de directorios  
 Es un lenguaje muy antiguo que sigue siendo muy funcional y que permite manejar grandes cantidades de datos. En esta sección aprenderás a conocer tu ubicación, a crear directorios y a listar el contenido de ellos.  

Vamos a comenzar por crear un directorio de trabajo. Como primer paso, abre tu terminal de gitbash e identifica donde estás ubicado.
`pwd`  
`/home/minombre`  

Ahora determina el contenido de tu directorio utilizando el comando `ls`.   
`ls `  
Usualmente los comandos de linux suelen aceptar modificadores, por ejemplo que ocurre si escribes `ls -l` ahora prueba con `ls -ñ`.   

Crea un directorio de trabajo para tus prácticas de bash  
`mkdir bashpracticas`  

Vamos a mover desde windows todos los archivos de genomas a nuestro nuevo directorio.
Utilizando el comando `cd bashpracticas` ubícate en el directorio que creaste. Comprueba desde la terminal que estés dentro del directorio. ¿qué comando te sirve para ello?  
  
Comprueba que todos los archivos de genomas están ahi. ¿Qué comando utilizarías?   

Verifica el contenido de las primeras n líneas de cada uno de ellos utilizando el comando head. 
`head *faa`

### Ejercicio Respaldo de los genomas    
1. Crea una carpeta respaldo  
2. Copia todos los genomas a la carpeta respaldo utilizando el comando `cp path-inicio path-final`  
  
### El poder de linux  
Muchos programas pueden ejecutarse desde la terminal de linux, de hecho la mayoría de los programas bioinformáticos se ejecutan ahi. Hagamos un ejemplo, haremos nuestro propio programa y lo correremos en muchos archivos.  
Supón que tienes muchos archivos fasta y no sabes cuáles corresponden a genomas y cuáles a plásmidos. Posiblemente conocer el tamaño de los archivos te ayudaría a decidir. Linux tiene el comando para ti. Con `wc` obtendrás el número de líneas y caracteres de un archivo. Para ver la salida de este comando ejecuta `wc 48664.132.faa`   

nano contador.sh
`wc $1`  
control O para salvar  
control x para salir

Ahora ejecuta tu script 
`bash contador.sh 48664.132.faa`  
¿Qué te queda? 

¿Qué te queda si ejecutas ` ls *faa | while read line; do bash contador.sh $line ;done` ?  
  

## Docker 
Docker es una plataforma de contenedores informáticos que facilita compartir software, procesos y datos. Dentro del mismo contenedor se instalan todas las dependencias y se facilitan las instalaciones en distintas máquinas. Cuenta con DockerHub una base de datos en donde se pueden buscar todas las tuberías deseadas. Aunque Docker es originalmente para linux también puede correr en Windows, y ya está instalado en su máquina.  

# Ejemplo 1  Hello world  
siempre empezamos con la palabra docker, para indicarle a power shell que ejecutaremos un comando de docker, a continuación el comando que queremos correr, por ejemplo run, posiblemente algunos modificadores, y finalmente el nombre de la imagen de docker a correr. Corre los siguientes ejemplos, ¿Qué pasa?    
`docker run hello-world  `  
`docker images ` 

# Ejemplo Visualizar EvoMining.  
En Windows docker corre en una terminal llamada powershell, donde se pueden utilizar los comandos de linux. Power shell tiene algunas particularidades. Vamos a correr EvoMining en Windows variando un poco el tutorial de EvoMining en [GitHub](https://github.com/nselem/evomining)      

`docker run --rm -i -t -v $(pwd):/var/www/html/EvoMining/exchange -p 80:80 nselem/evomining:latest /bin/bash`  
  
# Ejercicio subir un genoma utilizando myRAST.    
Sigue el tutorial en la página de [myRAST](https://github.com/nselem/myrast)  

Existen ensambladores genómicos empacados en docker, así como software para filtrado y supervisión de procesos de calidad.  
  
