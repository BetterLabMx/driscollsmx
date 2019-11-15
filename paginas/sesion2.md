# Sesión 6 Visualización y búsqueda de secuencias  

## 6.1 Visualización de secuencias  
### Datos de secuenciación  
Las muestras que producimos se secuenciaron en el Laboratorio de Servicios Genómicos del Laboratorio Nacional de Genómica Para La Biodiversidad. Se necesitan 20 µl de una reacción de PCR de cada muestra a una concentración mínima de ADN de 100 ng  totales. Esta secuenciación es por el método de Sanger (secuenciación por capilares) y para esto es necesario hacer un PCR con los primers usados para amplificar la región D-loop.  

### Análisis de calidad de resultados de la secuenciación   

La calidad de las secuencias, la extracción de las mismas y los electroferogramas se analizan con la ayuda del software Finch TV (versión 1.3.0) [Geospiza Inc. 2006](http://informatics.perkinelmer.com/Support/SupportNews/details/?SupportNews=124). En un cromatogroma la intensidad de la señal representa las cuatro bases en diferentes colores: verde para adenina, rojo para timina, negro para guanina y azul para citosina. Utilizaremos la versión de FinchTV que se encuentra en el escritorio de tu computadora. FinchTV es un programa que se inicia desde la terminal, asi que para comenzar a analizar tu secuencia necesitarás aplicar tus conocimientos de linux.  
  
#### Ejercicio   
> Visualizar la calidad de tu secuencia con FinchTV  
> Si no has descargado los archivos de tus secuencias descárgalos de tu correo y colócalos en la carpeta BetterLab.    

1. Abre una terminal y verifica en qué directorio estás. Si no estás en BetterLab utiliza `cd` para ubicarte en el directorio BetterLab.  
`$ pwd  `  

2. Confirma que los archivos de tu secuencia, están dentro de la carpeta BetterLab.  
`$ ls`  
Debes tener en tu directorio `/home/user/Desktop/BetterLab/` al menos dos archivos uno con extensión `ab1`, y otro con extensión `seq`. 

3. Cámbiate al directorio FinchTV. Para ello debes utilizar `cd`. Hasta ahora haz utilizado `cd` para entrar a un directorio, pero en este caso necesitas salir un nivel del un directorio. Tú te encuentras en  
  ![Directorios](Directorios.png)  
`/home/user/Desktop/BetterLab/`   
  
y quieres llegar a    
  
`/home/user/Desktop/FinchTv`    
    
Para ello debes puede utilizar el modificador `..` en el comando `cd` para salir de `BetterLab` y regresar a `Desktop`.  
Con `$ cd ..`  puedes salir un nivel del directorio en que te encuentras.  
  
`$ cd ..`  
`$ pwd `    
`/home/user/Desktop`      
  
El modificador `..`  en el comando `cd` sirve para retroceder un directorio.    
  
Verifica que estés en `/home/user/Desktop` y utiliza `cd` para llegar a `/home/user/Desktop/FinchTv`     
`$ cd FinchTv` 
 
5. Verifica que estés en FinchTv y visualiza su contenido.   
`$ pwd `   
`$ ls `    
  
6. Ahora desplázate a la carpeta /usr/bin  
`$ cd usr/bin`  
  
7. Verifica que el contenido de esta carpeta, contenga un archivo llamado finchtv, que es el ejecutable del programa visualizador de electroferogramas.  En el siguiente paso lo ejecutaremos cargándole el archivo ab1, que corresponde a la calidad de tu secuencia.  
`$ ls`  
  
8. Si te encuentras en `/home/user/Desktop/FinchTv/usr/bin` ejecuta el programa finchtv. En BASH para ejecutar un programa se agregan al principio los caracteres "./".  
`$ ./finchtv  /home/user/Desktop/BetterLab/misecuencia.ab1`   
¿Qué observas?  

![FinchTV](Finchtv.png)   
Si quieres analizar el electroferograma en tu computadora aquí puedes [descargar Finch TV](https://slackware.pkgs.org/14.1/slackonly-x86_64/finchtv-1.3.1-i386-1_slack.txz.html).  

Después de borrar de tu secuencia 
### Secuencia consenso  
Una vez que visualizaste tus secuencias forward y reverse, obtén una sola secuencia consenso con la cual te encuentres satisfecho de la calidad. Esta secuencia es la que utilizarás para posteriores análisis.  

  
      
## 6.2 Búsqueda de secuencias en bases de datos.    
### Blast  
La herramienta BLAST Basic Local alignment search tool es un alineador múltiple de secuencias que nos ayuda a encontrar otras secuencias parecidas. BLAST está disponible para realizar búsquedas en NCBI, pero también puedes descargarlo y realizar búsquedas en tus propias bases de datos. Existen distintas versiones de blast según el tipo de secuencia que tengas, por ejemplo están:  
  
- [Página principal de BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi)  Para análisis de secuencias de ADN y de proteínas. 

Ya que tenemos secuencias de ADN, utilizaremos BLASTn (n=nucleótidos)

Primero alinearemos las dos réplicas de la secuencia para identificar inconsistencias entre ellas.   

Selecciona 'Align two or more sequences'  

Utiliza el cromatograma de FinchTv para decidir cuál es la secuencia más probable. Y al final exporta tu archivo con terminación QCconsenso.seq


Hagamos blast en NCBI de tu secuencia mitocondrial curada. ¿A qué se parece? ¿Qué información obtuviste?    

¿Qué resultados encuentras cuando cambias la base de datos de búsqueda?


