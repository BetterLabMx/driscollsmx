---
title: "LinuxDocker"
author: "Nelly"
date: "18 de noviembre de 2019"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# Bash y docker  
Linux es un sistema operativo como windows o mac mientras que Bash es el lenguaje de la terminal de linux que nos permite manipular muchos archivos a la vez. Docker en cambio es un empacador de programas de linux y sus dependencias que facilita compartir software de análisis científicos. En esta sección hablaremos de estas dos herramientas.   

## Manejo del sistema de directorios utilizando bash  
 Es un lenguaje muy antiguo que sigue siendo muy funcional y que permite manejar grandes cantidades de datos. En esta sección aprenderás a conocer tu ubicación, a crear directorios y a listar el contenido de ellos.  

Vamos a comenzar por crear un directorio de trabajo. Como primer paso, abre tu terminal de gitbash e identifica donde estás ubicado.
`pwd`  
`/home/minombre`  

Ahora determina el contenido de tu directorio utilizando el comando `ls`.   
`ls `  
Usualmente los comandos de linux suelen aceptar modificadores, por ejemplo que ocurre si escribes `ls -l` ahora prueba con `ls -ñ`.   

Crea un directorio de trabajo para tus prácticas de bash  
`mkdir bashpracticas`  

Vamos a mover todos los archivos de genomas a nuestro nuevo directorio.
Utilizando el comando `cd bashpracticas` ubícate en el directorio que creaste. Comprueba desde la terminal que estés dentro del directorio. ¿qué comando te sirve para ello?  
  
Comprueba que todos los archivos de genomas están ahi. ¿Qué comando utilizarías?   

Verifica el contenido de las primeras líneas de cada uno de ellos. 
`head *faa`

## Ejercicio Respaldo de los genomas    
1. Crea una carpeta respaldo  
2. Copia todos los genomas a la carpeta respaldo utilizando el comando `cp`  
## Edición de archivos  
Muchos programas pueden ejecutarse desde la terminal de linux, de hecho la mayoría de los programas bioinformáticos se ejecutan ahi.  

## Docker 
Docker es una plataforma de contenedores informáticos que facilita compartir software, procesos y datos. Dentro del mismo contenedor se instalan todas las dependencias y se facilitan las instalaciones en distintas máquinas. Cuenta con DockerHub una base de datos en donde se pueden buscar todas las tuberías deseadas. Aunque Docker es originalmente para linux también puede correr en Windows, y ya está instalado en su máquina.  

# Ejemplo 1  Hello world  
docker images  
docker run hello-world  

# Ejemplo Visualizar EvoMining.  
docker run 

En Windows docker corre en una terminal llamada powershell, donde se pueden utilizar los comandos de linux. Power shell tiene algunas particularidades. Vamos a correr EvoMining en Windows.  
# Ejercicio subir un genoma utilizando myRAST.    

Existen ensambladores genómicos empacados en docker, así como software para filtrado y supervisión de procesos de calidad.  
