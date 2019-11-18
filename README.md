# Biología computacional para DRISCOLLs
![DriscollsBerries](images/driscolls.jpeg)  

En este curso aprenderás un poco de biología computacional, adquirirás nociones de las herramientas linux, git, RAST y microreact.   

  
## Calendario   
  
<table>
    <tr>
        <td>Lunes 18 (Mañana)       </td> <td>   Noviembre 2019                 </td>
  </tr>  
  <tr><td> <a href="paginas/sesion1.md"> Sesión 1</a>  Datos y algoritmos bioinformáticos  (9:00 - 10:30 am)          </td>  
      <td>  <a href="paginas/sesion2.md"> Sesión 2</a> Metadatos y visualización (10:45 - 11:45 am)</td>
  </tr>
  <tr><td> <a href="paginas/sesion3.md"> Sesión 3</a> (12:00 - 1:00 am) <a href="http://rast.nmpdr.org/rast.cgi"> RAST </a> y Genomica Bacteriana
        </td><td></td></tr>        
    <tr><td> Comida (2:00-3:00)</td><td> Comida (2:00-3:00)</td></tr>
  <tr><td>  <a href="paginas/sesion4.md"> Sesión 4  </a> (3:00 - 04:00 pm)   Análisis de secuencias Introducción y <a href="https://swcarpentry.github.io/shell-novice-es/"> bash     y Docker </a> </td>
      <td>Sesión 5 (4:15-5:15) Perspectivas y temas de investigacion </td> </tr>
   </table>  
      
    
## Informacion General  
Aqui puedes encontrar un [documento colaborativo](https://etherpad.net/p/compbio  ) donde compartiremos información relevante, links, y respuestas a preguntas que surjan durante el taller. Dos de nuestras lecciones linux y git son parte del contenido habitual de [software carpentry](https://software-carpentry.org/) una organización dedicada a enseñar habilidades de cómuto para hacer más en menos tiempo y con menos sufrimiento, usaremos estas dos lecciones con su permiso. Las otras dos lecciones fueron pensadas de acuerdo a las necesidades específicas de nuestro centro de trabajo. Finalmente esta [presentación](https://docs.google.com/presentation/d/1ELPMuwxz9no_BEKIPr4la0CtLt4d1LMicqorxCdjjDs/edit) contiene el material utilizado en las pláticas. 

___     
  
## Instalaciones y requerimientos previos  
<h2 id="setup">Setup</h2>  

<p>
  Para participar en este taller necesitas acceso al siguiente software. Además necesitarás acceso a un navegador como chrome o firefox.   
  </p>
<p>
  Aqui hay una referencia de posibles problemas durante la instalación.  
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Wiki de problemas de instalación y sus soluciones. </a>.
</p>

<div id="shell">  
  <h3>El Bash Shell</h3>  
  <p>  
    Bash es un intérprete de comandosque te da poder de hacer tareas simples rápidamente.  
  </p>  

  <div class="row">  
    <div class="col-md-4">  
      <h4 id="shell-windows">Windows</h4>  
      <a href="https://www.youtube.com/watch?v=339AEqk9c-8">Video Tutorial</a>  
      <ol>  
        <li>Baja para windows <a href="https://git-for-windows.github.io/">el instalador de git </a>.</li>  
        <li>Corre el instalador y sigue los siguientes pasos:  
          <ol>  
            <li>Click en "Next".</li>  
            <li>Click en "Next".</li>    
            <li>  
              <strong>  
               Manten el "Use Git from the Windows Command Prompt" seleccioinado y  click en "Next".  
              </strong>  
                Si se te olvida hacer esto algunos programas que necesitarás no funcionaran correctamente.  
                Si esto te pasa regrésate al paso anterior del instalador y selecciona la opción correcta.  
            </li>  
            <li>Click en "Next".</li>
            <li>  
              <strong>  
                Mantén "Checkout Windows-style, commit Unix-style line endings" seleccionado y click en "Next".
              </strong>
            </li>
            <li>  
              <strong>  
                Mantén "Use Windows' default console window" seleccionado y click en "Next".  
              </strong>  
            </li>  
            <li>Click en "Install".</li>
            <li>Click en "Finish".</li>  
          </ol>  
        </li>  
        <li>  
          si tu variable de ambiente "HOME" no está lista (o no sabes qué es esto):
          <ol>
            <li>Abre el prompt (Abre el menu start, escribe <code>cmd</code> y presiona enter [Enter])</li>
            <li>
              Escribe la siguiente línea en la ventana del promt exactamente como se  muestra:  
              <p><code>setx HOME "%USERPROFILE%"</code></p>  
            </li>  
            <li>Presiona [Enter], debes de ver <code>SUCCESS: Specified value was saved.</code></li>
            <li>Para salir del prompr escribe <code>exit</code> y presiona enter [Enter]</li>
          </ol>
        </li>
      </ol>
      <p>Esto te dará ambos Git y Bash en el programa Git Bash.</p>
    </div>
    <div class="col-md-4">
      <h4 id="shell-macosx">macOS</h4>
      <p>
        El shell por default en todas las versiones de macOS es Bash, asi que no debes instalar nada.  Podrás accesar a Bash desde la Terminal
        (que se encuentra en        <code>/Applications/Utilities</code>).
        Para la instalación de Git aqui tenemos un <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
        for an example on how to open the Terminal.
        Tal vez quieras mantener la Terminal en tu dock para este taller.  
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="shell-linux">Linux</h4>
      <p>
        El shell es usualmente Bash, pero si tu máquina es diferente puedes abrir una terminal y escribir <code>bash</code>.  
        No se necesita intalar nada
      </p>
    </div>
  </div>
</div> 
