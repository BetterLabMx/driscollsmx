# Metadatos y Visualización  

## Metadatos  
Los metadatos son datos sobre los datos usualmente vienen en una tabla de excel. Por ejemplo la latitud y la longitud del muestreo son metadatos que vienen en el archivo BaseMitocondrial que descargaste. Hay una serie de consejos sobre buenas prácticas de toma de metadatos. En cuanto a los datos, las buenas prácticas nos dicen que siempre conservemos los datos originales.    

### [Microreact  ](https://microreact.org/)  un visualizador de datos y metadatos  

Microreact es una plataforma de visualización de datos que está especializada en epidemiología genómica. En particular Microreact ayuda a explorar árboles filogenéticos conectándolos con mapas señalando los lugares dónde ocurrieron las infecciones.  

Nosotros utilizaremos esta plataforma primero para ver los lugares y años donde nacimos todos nosotros!   

####   Ejercicio primera parte
Llena con tus datos la [Hoja de cáculo de google drive ](https://docs.google.com/spreadsheets/d/1IyFEEVDgBtfRb9rUEX9JePTl7ARiHAxyR3n1RKtk_OQ/edit?usp=sharing)
  
Para agregar las coordenadas de tu lugar de nacimiento:
1) Abre [Google Maps  ](https://www.google.com.mx/maps)  
2) Busca tu lugar de nacimiento  
3) Da click derecho sobre el lugar del que quieres extraer las coordenadas. Debe aparecer un cuadrito en la parte inferior del mapa    (Si no aparece utiliza click derecho -> ¿Qué hay aquí?)
4) Pulsa sobre las coordenadas que están abajo del cuadro  
5) Copia y pega la latitud y longitud en las columnas de la hoja de cálculo que abriste en el paso   
6) Usa el link del documento compartido en la red para visualizarlo en microreact  https://docs.google.com/spreadsheets/d/e/2PACX-1vRQRvlM_T_Ftohl23cWvs8hT9FVqCp2K8441-Ce0V1aA_RvRYLOjFJg_L_ilvALM_zBiVvJy4w0RevT/pub?output=csv
### Recuerda que cuando se llena la hoja de cálculo se deben seguir las buenas prácticas de colecta de metadatos.

####   Ejercicio segunda parte
a) Abre [Microreact  ](https://microreact.org/)  
b) Inicia sesión utilizando tu cuenta de gmail  
c) Da click en Upload  
d) Ve a la hoja de cálculo y copia el link que está en 'File->Publish' o 'Archivo->Publicar'  
e) Pega el link donde pide un archivo .csv  
f) da click en continue (without tree)  
g) Ingresa el título de tu proyecto de visualización  
h) Visualiza tus resultados!  

### Visualización simultánea de árboles y mapas
Ahora regresa a la página principal de microrreact.  
Selecciona el proyecto 'Zika virus in the Americas', discute con tu compañero de al lado y escriban sus respuestas en el documento colaborativo.  
¿En dónde se tuvo el primer registro de este virus?  
¿Cuál fue el primer lugar de América en el que se detectó zika?  
¿En qué año fue la epidemia que se describe en este artículo?  
¿Cuál es el ancestro más cercano a los virus de la epidemia?  
¿Cuántos sitios de microencefalia en Brasil reportaron?
¿Cuáles virus tienen el genoma más grande y más chico?

## Metadatos con tus secuencias de Xanthomonas.  
Ahora vamos a crear una visualización de microreact que incluya tanto las coordenadas de latitud y longitud donde se tomó la muestra de Xanthomonas como el árbol filogenético de las secuencias. 
1. Utiliza como árbol el archivo newick de [16s de Xanthomonas](Xanthomonas-BioNJ_tree). 
2. Para los metadatos ve a NCBI y observa los archivos genebank de genomas de Xanthomonas. 
3. Crea una hoja de cálculo de google docs, que contenga la base de datos que ya descargaste y además tu secuencia con tus metadatos [Ejemplo](https://docs.google.com/spreadsheets/d/1tMbJYiF7cR1BSrCJ_PRm3ozaBx_QNZrfMKlQBmpIAvw/edit?usp=sharing).   
Link publicado  
https://docs.google.com/spreadsheets/d/e/2PACX-1vSZSbMYiLj2D0mHt4jUjJ22SrC63mgzb-443QTPRiDibLdSVkOJvMAddbSLBaPhD_KdbcICJOd2fedM/pub?output=csv
4. Crea tu visualización en Microreact de Xanthomonas. ¿Qué observas? ¿Qué tan parecidas son las secuencias? Tip: Puedes utilizar BLAST también para comparar dos secuencias? ¿Cómo puedes mejorar la resolución de tu árbol?

## De donde viene la siguiente secuencia
   
>Secuencia_misteriosa  
AGTGAACGCTGGCGGCAGGCCTAACACATGCAAGTCGAACGGCAGCACAGTAAGAGCTTGCTCTTATGGG
TGGCGAGTGGCGGACGGGTGAGGAATACATCGGAATCTACTCTTTCGTGGGGGATAACGTAGGGAAACTT
ACGCTAATACCGCATACGACCTACGGGTGAAAGCGGAGGACCTTCGGGCTTCGCGCGATTGAATGAGCCG
ATGTCGGATTAGCTAGTTGGCGGGGTAAAGGCCCACCAAGGCGACGATCCGTAGCTGGTCTGAGAGGATG
ATCAGCCACACTGGAACTGAGACACGGTCCAGACTCCTACGGGAGGCAGCAGTGGGGAATATTGGACAAT
GGGCGCAAGCCTGATCCAGCCATGCCGCGTGGGTGAAGAAGGCCTTCGGGTTGTAAAGCCCTTTTGTTGG
GAAAGAAAAGCAGTCGGTTAATACCCGATTGTTCTGACGGTACCCAAAGAATAAGCACCGGCTAACTTCG
TGCCAGCAGCCGCGGTAATACGAAGGGTGCAAGCGTTACTCGGAATTACTGGGCGTAAAGCGTGCGTAGG
TGGTGGTTTAAGTCTGTTGTGAAAGCCCTGGGCTCAACCTGGGAATTGCAGTGGATACTGGGTCACTAGA
GTGTGGTAGAGGGTAGCGGAATTCCCGGTGTAGCAGTGAAATGCGTAGAGATCGGGAGGAACATCAGTGG
CGAAGGCGGCTACCTGGACCAACACTGACACTGAGGCACGAAAGCGTGGGGAGCAAACAGGATTAGATAC
CCTGGTAGTCCACGCCCTAAACGATGCGAACTGGATGTTGGGTGCAATTTGGCACGCAGTATCGAAGCTA
ACGCGTTAAGTTCGCCGCCTGGGGAGTACGGTCGCAAGACTGAAACTCAAAGGAATTGACGGGGGCCCGC
ACAAGCGGTGGAGTATGTGGTTTAATTCGATGCAACGCGAAGAACCTTACCTGGTCTTGACATCCACGGA
ACTTTCCAGAGATGGATTGGTGCCTTCGGGAACCGTGAGACAGGTGCTGCATGGCTGTCGTCAGCTCGTG
TCGTGAGATGTTGGGTTAAGTCCCGCAACGAGCGCAACCCTTGTCCTTAGTTGCCAGCACGTAATGGTGG
GAACTCTAAGGAGACCGCCGGTGACAAACCGGAGGAAGGTGGGGATGACGTCAAGTCATCATGGCCCTTA
CGACCAGGGCTACACACGTACTACAATGGTAGGGACAGAGGGCTGCAAACCCGCGAGGGCAAGCCAATCC
CAGAAACCCTATCTCAGTCCGGATTGGAGTCTGCAACTCGACTCCATGAAGTCGGAATCGCTAGTAATCG
CAGATCAGCATTGCTGCGGTGAATACGTTCCCGGGCCTTGTACACACCGCCCGTCACACCATGGGAGTTT
GTTGCACCAGAAGCAGGTAGCTTAACCTTCGGGAGGGCGCTTGCCACGGTGTGGCCGATGACTGGGGTGA
AGTCGTAACAAGGTAGCCGTATCGGAAGGTGC



