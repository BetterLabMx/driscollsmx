# Sesión 5 Datos genómicos y Bioinformática   

## 5.1 ¿Qué es la bioinformática?  
Bioinformática es un conjunto de técnicas y algoritmos computacionales aplicadas a datos biológicos. Es una nueva área de estudio que combina biología molecular con ciencias computacionales. Un reto mayor que la bioinformática enfrenta es organizar la gran cantidad de información obtenida gracias a las nuevas tecnologías de secuenciación. Veamos ¿qué es la bioinformática? en esta [presentación](https://docs.google.com/presentation/d/1YVe0m1G_4EgnF9--HmRjnNluNHYqXNrpozsXTktSNgc/edit?usp=sharing)    

### La información Biológica se almacena en grandes bases de datos.  
Las bases de datos que almacenan información biológica pueden ser públicas o privadas. En ellas, los usuarios acumulan información de los organismos. Esta información es usualmente procesada por algún paquete de análisis para proporcionar una visualización.  

#### [The National Center for Biotechnology Information NCBI](https://www.ncbi.nlm.nih.gov/)  
NCBI es una de las grandes bases de datos biológicas contiene información de una extensa variedad de organismos incluyendo genes, genomas, proteinas, clasificación taxonómica, etc.  

Ejemplo de búsqueda en NCBI:
1. Búsqueda individual
   Ve a la página de NCBI y escribe mitochondrial en el buscador  
   ¿Qué resultados te salen?  
   
2. Búsqueda con modificadores AND y NOT   
 De hecho NCBI agrupa varias bases de datos, vamos a explorar taxonomy y nucleotide. Selecciona Nucleotide como base de datos y realiza la siguiente búsqueda.   
   
`"mitochondrial" [title]AND "D-loop"[title] NOT "segment"[title] AND "homo" [organism]  `    
  
¿Qué obtienes?  

### El formato fasta  
En bioinformática los formatos de los archivos son importantes para su posterior tratamiento. Nosotros necesitaremos el formato fasta para posteriores análisis. Por ello haremos un ejercicio para que te familiarices con él. Este formato consiste en una línea con el símbolo '>' antes del nombre identificador de la secuencia, y después un salto de línea y la secuencia como tal.  
  
Ejercicio  
  
De los resultados que visualizaste en tu segunda búsqueda, obtén la secuencia fasta de un D-loop mitocondrial y anótala en el documento colaborativo. Para ello debes hacer click en algún resultado de tu interés y después seleccionar FASTA en la parte superior izquierda.  

Descarga tu secuencia de tu correo y colócala en el Escritorio. ¿Es la secuencia de NCBI idéntica a la tuya?, ¿Qué diferencias ves? Anota tu conclusión en el documento colaborativo.  

## 5.2 La terminal de linux  

Para visualizar la calidad de nuestras secuencias vamos a visualizar un electroferograma. Para ello necesitamos iniciar el visualizador desde una terminal de linux. Por ello, a continuacion estudiaremos un poco de bash, el lenguaje de linux. Ahora bien, ¿Qué es una terminal de Linux?  
  
  La terminal es un medio para que el usuario interactúe con la computadora. Una terminal es un programa cuyo trabajo es ejecutar otros programas. La terminal más popular de linux se llama bash, aunque es antigua sigue siendo muy útil. Utilizar la terminal permite realizar acciones sobre muchos archivos, esto puede ahorrar una cantidad inimaginable de tiempo y errores manuales y al final puede ser la diferencia entre terminar o no una investigación. Para conocer más sobre la terminal de linux te recomendamos <a href="https://swcarpentry.github.io/shell-novice-es/"> Software Carpentry </a>  

### Moverse en el sistema de directorios  

> En esta introducción a BASH aprenderás a moverte en el sistema de directorios:  
> - Conocer tu ubicación en el sistema de directorios (pwd)  
> - Conocer el contenido del directorio en el que te encuentras.   
> - Cambiarte de directorio.  
  
Los tres comandos basicos para ubicarte y moverte en la estructura de directorios son:  
`cd `Cambio de directorio.    
`ls` Listado del contenido del directorio.    
`pwd`"Path to working directory" Muestra la ubicación del directorio.    

Abre una terminal y vamos a verificar en qué directorio estás :  
`$ pwd`  
 
El resultado debe ser algo similar a:   
`/home/usuario`  

Ese es el path absoluto donde estás ubicado. En este caso `home`  es el directorio raíz, que contiene a `usuario`.  

Ahora que ya sabemos nuestra ubicación, vamos a ver el contenido del directorio `/home/usuario`  
`$ ls `
`Desktop    Downloads         Music     Public  src        Videos`  
   
El resultado contiene varios nombres, por ejemplo puede contener Downloads, Desktop, examples.desktop y Documents. Muchos comandos de linux tienen modificadores. `ls` por ejemplo puede modificarse con `-F` y con `-l`. Con `ls -F` se añade una diagonal a todos los directorios, dejando sin diagonal a los elementos de la lista que son archivos. Con `ls -l` se obtiene una descripción más detallada de la fecha de creación del elemento, y de los permisos que tienen los uduarios. No tienes  que aprenderte todos los comandos ni modificadores, ni pasa nada si te equivocas. 
  
### Ejercicio 
Teclea el siguiente comando en la terminal
`$ ls -ñ`  
¿Qué pasa?   

Finalmente, necesitamos ubicarnos en el Desktop, que es el lugar donde vamos a trabajar. Para ello utilizaremos el comando `cd`.
1. Verifica que Desktop esté dentro del directorio `/home/usuario` ¿Qué comando utilizarías?  
2. Dirígete a directorio Desktop  
`$ cd Desktop`  
3. Verifica que estás ahí.  
`$ pwd`  
`/home/usuario/Desktop`  

¿Cuál es el contenido de Desktop? Ahora vamos a crear un directorio llamado BetterLab que es dónde trabajaremos de ahora en adelante. ¿Cómo crearías un directorio utilizando BASH?    

### Ejercicio 
Utiliza google para encontrar el comando crear un directorio en BASH.  

### Crear directorios
> Aprenderás a crear un directorio  

### Ejercicio  
Crea el directorio BetterLab  

1. Verifica que estás en el Desktop  
`$ pwd`  
`/home/usuario/Desktop`  
2. Verifica el contenido de Desktop  
`$ ls `  
3. Crea el directorio BetterLab  
`$ mkdir BetterLab`  
4. Verifica que se haya creado el nuevo directorio  
`ls `  
Debe aparecer ahora BetterLab como parte del contenido de `/home/usuario/Desktop`  
5. Ahora cámbiate al directorio BetterLab. Teclea exactamente  
`$ cd betterlab`  
¿Qué pasa?  

Linux es sensible a mayúsculas y minúsculas debes tener cuidado con ello. Tampoco se recomienda usar ñ,.,~ u otros caracteres que no sean alfanuméricos. De hecho cuando estás escribiendo bien un nombre puedes utilizar la tecla autcompletar (la de las dos flechas ubicada del lado izquierdo del teclado), y bash autompletará el nombre correcto. Otra recomendación es utilizar las flechas del teclado para recuperar los comandos escritos con anterioridad.  
  
Estamos listos para la siguientel lección, la visualización del electroferograma.   


# Generación de base de datos Fusarium 

## Búsqueda de secuencias en NCBI 

Entra al sitio web de [NCBI](https://www.ncbi.nlm.nih.gov/) y busca el gen de interés con el que se realizará el árbol, específicando en primer lugar el organismo, en este ejemplo: Fusarium 16s  

![FusariumNCBI](Fusarium18s.png)

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


