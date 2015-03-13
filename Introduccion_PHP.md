#Tutorial de instalacion php
En este primer capítulo aprenderemos que es PHP, sus características y su funcionamiento. 

##¿Qué es PHP?
 (Acrónimo de “PHP: Hypertext Preprocessor”)

Es  un lenguaje de programación interpretado (scripts) contenido en páginas HTML y ejecutado en el servidor.

Características:

* PHP esta publicado bajo la Licencia PHP ( software libre).
* Los archivos de PHP se deben guardar la extensión .php. Ejemplo: (archivo.php).
* Puede ser desplegado en la mayoría de los servidores web como IIS y Apache.
* La última versión publicada es la php5.5.12.
* Permite aplicar técnicas de POO (Programación Orientada a Objetos).
* Permite ser incrustado en HTML (facilita el desarrollo de sitios web dinámicos).
* Tiene la capacidad de conectares a la mayoría de los motores de base de datos (MySQL, MongoDB, etc.).
* manipular archivos
* utilizar servidores de correos e interactuar con otros lenguajes.

##¿Cómo Funciona?
Explicaremos ahora lo que sucede cada vez que solicitamos al navegador ver una página en PHP

El cliente [el navegador web]:
Es el que ejecuta el script de PHP, haciendo la petición a un servidor web (se escribe la URL: lapagina.com/contactos.php).
El servidor web:
El servidor web recibe la petición y al verificar que la extensión es “php” hace una solicitud al intérprete de PHP para que este ejecute el script necesario.
Otra manera de expresarlo sería:
Ejecuta el código PHP solicitado y retorna el código HTML generado al Navegador. 
El intérprete de PHP:
Realiza la ejecución de todas las instrucciones o sentencias que se encuentran en el archivo solicitado mostrando los resultados en el servidor web.
El servidor web envía al cliente la respuesta que devolvió el script de php, el cliente muestra la respuesta en el formato que sea requerido (HTML, XML, PDF, JPEG, etc.).
En pocas palabras el programa PHP es ejecutado en el servidor y el resultado es enviado al navegador. El resultado es normalmente una página HTML.

###Manera de instalar PHP

Para probar en forma local en nuestro lo que codifiquemos en PHP recomiendo utilizar uno de los combos instaladores, estos son los servidores los cuales contienen los paquetes con MySQL (manejador de base de datos), PHP y Perl. Estos instaladores llevan el nombre de AMPP(Apache, Mysql, PHP y Perl) facilitan el trabajo a la hora de tener un servidor de prueba. 
Estos pueden ser:

     SISTEMAS OPERATIVO     SERVIDORES     SITIOS DE DESCARGA
     Windows           WampServer:    [http://www.wampserver.com/en/#download-wrapper]
     Windows, GNU/Linux, Ubuntu, Solaris y Mac OS X.    XAMPP:     [https://www.apachefriends.org/es/index.html]
      Windows     AppServ:     [http://www.appservnetwork.com/?newlang=spanish]
     Windows y Linux     MAMP:    [http://www.mamp.info/en/]

#Sistema operativo en: Windows

###Manera de instalar wampserver
Cuando descargue  wampserver le pedirá actualización de visual Descarga visual estudio.

1.- Dependiendo los requerimientos de tu equipo descargamos y procedemos a ejecutar el instalador.
2.- Aceptamos los términos y condiciones elegimos donde se instalara nuestro servidor.
3.- Indicamos si queremos que se cree un ícono en el escritorio, le damos siguiente he instalar.
4.-Luego de instalarse nos solicita que navegador abrirá por defecto cuando ejecutemos el PhpMyAdmin (para la creación de la base de datos de MySQL): este puede ser Chrome, Explorer, Firefox  etc. 
5- En el siguiente diálogo dejamos los datos por defecto.
6.- Finalmente aparece el diálogo final donde se nos informa que se iniciará el WampServer (es decir que se cargará en memoria el Apache, el PHP y el servidor de base de datos MySQL) :

Ahora que hemos terminado la instalación de WampServer el icono de nuestro WampServer de ver de color verde esto quiere decir que está listo para usar.

 Si nuestro icono no se torna verde y en vez de ello se torna naranja nos debemos dirigir a nuestro apache.

Para resolver este conflicto, nos dirigimos a nuestro archivo httpd.conf 
Como se encuentra en la imagen, nos dirigimos  directo a nuestro servidor.
En nuestro menú nos dirigimos en Apache nos mostrara un submenú y nos dirigiremos a nuestro archivo httpd.conf
Otra manera para ir a este archivo de apache es irte por medio de esta dirección de tu equipo.
C:\wamp\bin\apache\apache2.4.9\conf/ httpd.conf

Después dentro del archivo httpd.conf  buscamos: ServerName localhost:80 
y lo cambiamos por : ServerName localhost:82 

Esta es la forma en que lo veremos en el navegador

##Sistema operativo en: Ubuntu
###Manera de instalar Xampp

Ahora vamos a ver como instalar la versión más actual, Xampp.

Nos dirigimos al sitio oficial de Xampp:
[https://www.apachefriends.org/es/download.html]
Descarga xampp dependiendo de el requerimiento de tu equipo, y ejecuta el instalador

Nos dirigimos a nuestra terminal 
El XAMPP se descargo en nuestra carpeta personal, no es necesario este paso, pero si lo hemos hecho en otra carpeta o directorio, debemos de colocarnos en dicha carpeta o directorio con el comando "cd". Por ejemplo, si ha sido en "Descargas", sería:
```sh
$ cd descargas
```
Los permisos que le damos para poder ejecutarlo:
```sh
$ sudo chmod 755 xampp-linux-x64-1.8.3-1-installer.run
```
Lo instalamos con:
```sh
$ sudo ./xampp-linux-x64-1.8.3-1-installer.run
```
Aparecerá un instalador le daremos siguiente
Al finalizar salimos de nuestra terminal 
1 – nos dirigimos donde  tenemos el XAMPP 
2- nos vamos a la carpeta opt
3-Encontraremos la carpeta llamada lampp dentro de esta nos dirigiremos a la carpeta htdocs dentro de esta carpeta crearemos nuestros proyectos en PHP.

##Sistema operativo en: Linux
###Manera de instalar MAMP
Ahora vamos a ver como instalar MAMP
Nos dirigimos al sitio oficial:
[http://www.mamp.info/en/]
Seleccionamos el MAMP simple
Descargamos el MAMP
Como podemos ver en la imagen del lado derecho se encuentra las distintas versiones de PHP
Debemos tener un archivo.pkg el cual le daremos doble click 
Nos mostrara un contenido como este, nos dirigimos en continuar
Al termino de su instalación nos dirigimos a la carpeta de nuestras aplicaciones
Por defecto nos instalara el MAMP PRO ya que nos lo dan en forma de prueba por algunos días.
La carpeta que vamos a utilizar será el MAMP simple.
Seleccionamos el icono de MAMP simple y entramos a la interface de MAMP.
Seleccionamos el botón de Arrancar MAMP
Nos vamos a iniciar el servidor como muestra la imagen. 
Para ver donde crearemos nuestros proyectos en php nos dirigimos a preferencias y de esto seleccionamos la pestaña apache
En el MAP al ir al área local lo puede mostrar de la siguiente manera
Seleccionamos ir al puerto y cambiamos el área del puerto apache 
####Estos pasoso son opcionales  
#Nuestro Primer Script PHP
Para crear nuestro querido hola mundo  necesitamos tener editores de texto  estos pueden ser:
* Netbeans (Multiplataforma)
* Sublime Text 2 (Multiplataforma)
* Notepad ++ (Windows)
Cualquier editor de texto es bueno para utilizar, en especial si tiene un editor o IDE (Entorno de Desarrollo Integrado)  el cual nos ayuda en nuestros errores.
Nuestro archivo de PHP necesita principalmente su etiqueta de inicio y final:
```sh
<?php /*Etiqueta d inicio*/
?>/*Etiqueta Terminal*/
```

Lo primero que haremos será utilizar la función "echo".
"echo" se usa para imprimir datos en un documento en php. Con uno “echo” podemos imprimir cualquier dato o palabra.

Anteriormente se usaba “print”
Actual mente al usar un framework ya no es recomendable utilizar “echo” en algunos y estos se cambiaron por llaves dobles {[ }} 

Ahora bien el echo siempre debe de ir con comillas simples o dobles 
(Preferible simples si nuestro dato es padre ) y un punto y coma “ ; “ para indicar que esa función se cerro.
```sh
<?php 
echo "Hola Mundo";
?>
```
Ahora lo guardo en mi carpeta el cual lo he llamado php1 y nuestro archivo que acabamos de crear lo guardamos con el nombre hola_mundo.php 
No olviden que al guardar debe lleva la extensión .php 

Para ver el resultado nos dirigimos a nuestro el navegador en la ruta donde se encuentra nuestro archivo
 http://localhost:82/php1/hola_mundo.php.

Ahora un script mas util
```sh
<?php
   $edad = 10;
   if( $edad >= 20)
   {
      echo "Eres mayor de edad!";
   }
   else
   {
      echo "Eres menor de edad!";
   }
?>
```









* [Express] - fast node.js network app framework [@tjholowaychuk]
* [Gulp] - the streaming build system
* [keymaster.js] - awesome keyboard handler lib by [@thomasfuchs]
* [jQuery] - duh

### Installation

You need Gulp installed globally:

```sh
$ npm i -g gulp
```

```sh
$ git clone [git-repo-url] dillinger
$ cd dillinger
$ npm i -d
$ mkdir -p public/files/{md,html,pdf}
$ gulp build --prod
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins

* Dropbox
* Github
* Google Drive
* OneDrive

Readmes, how to use them in your own application can be found here:

* plugins/dropbox/README.md
* plugins/github/README.md
* plugins/googledrive/README.md
* plugins/onedrive/README.md

### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantanously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma start
```

### Todo's

 - Write Tests
 - Rethink Github Save
 - Add Code Comments
 - Add Night Mode

License
----

MIT


**Free Software, Hell Yeah!**

[john gruber]:http://daringfireball.net/
[@thomasfuchs]:http://twitter.com/thomasfuchs
[1]:http://daringfireball.net/projects/markdown/
[marked]:https://github.com/chjj/marked
[Ace Editor]:http://ace.ajax.org
[node.js]:http://nodejs.org
[Twitter Bootstrap]:http://twitter.github.com/bootstrap/
[keymaster.js]:https://github.com/madrobby/keymaster
[jQuery]:http://jquery.com
[@tjholowaychuk]:http://twitter.com/tjholowaychuk
[express]:http://expressjs.com
[AngularJS]:http://angularjs.org
[Gulp]:http://gulpjs.com
