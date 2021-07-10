Elige tus series favoritas 📺
Este proyecto es una incipiente pueba del desarrollo de una aplicación web de búsqueda de series a través de la API en abierto de TVMaze para
búsqueda de series. Te permite des/marcar las series como favoritas y guardarlas en local storage. 

Comenzando 🚀 Para utiilizarla solo necesitas cargar el enlace y....tendrás todas las series a tu disposición y a un clic de distancia. 

Instalación 🔧 Solo necesitas un navegador y ganas de pasar un buen rato. 

Construido con 🛠️ JavaScript (JS), HTML y CSS.

Contribuyendo 🖇️ Este proyecto solo ha sido posible gracias al apoyo y la sabiduría de Dayana, Iván y Miguel de Adalab.

Se aceptan expresiones de gratitud tales como una cerveza 🍺 o un café ☕ 

Este repo tiene incluído el Starter Kit creado en node y gulp. ¿Y qué es un Starter kit? Pues es una plantilla de proyecto con funcionalidades preinstaladas y preconfiguradas.

Este Kit incluye un motor de plantillas HTML, el preprocesador SASS y un servidor local y muchas cosas más. El Kit nos ayuda a trabajar más cómodamente, nos automatiza tareas.

Hay 3 tipos de ficheros y carpetas:

Los ficheros que están sueltos en la raíz del repositorio, como gulpfile.js, package.json... Son la configuración del proyecto.
La carpeta src/: son los ficheros de la página web, como HTML, CSS, JS...
Las carpetas public/ y docs/, que son generadas automáticamente cuando arrancamos el proyecto. El Kit lee los ficheros que hay dentro de src/, los procesa y los genera dentro de public/ y docs/.
Guía de inicio rápido
NOTA: Instalar previamente Node JS para trabajar con este repo:

Pasos a seguir para arrancar el proyecto desde tu ordenador:
No clonar este repo (porque no podrás añadir commits), descargarlo.
Crear un repo nuevo y añadir los archivos descargados.
Abre una terminal en la carpeta raíz de tu repositorio.
Instala las dependencias locales ejecutando en la terminal el comando:
npm install
Una vez hemos instalado las dependencias, vamos a arrancar el proyecto. El proyecto hay que arrancarlo cada vez que lo abras Para ello ejecuta el comando:

npm start
Este comando:

Abre una ventana de Chrome y muestra la página web, al igual que hace el plugin de VS Code Live Server (Go live).
También observa todos los ficheros que hay dentro de la carpeta src/, para que cada vez que modifiques un fichero refresca tu página en Chrome.
También procesa los ficheros HTML, SASS / CSS y JS y los genera y guarda en la carpeta public/. Por ejemplo:
Convierte los ficheros SASS en CSS.
Combina los diferentes ficheros de HTML y los agrupa en uno o varios ficheros HTML.
Después de ejecutar npm start ya puedes empezar a editar todos los ficheros que están dentro de la carpeta src/ y programar cómodamente.

Pasos para publicar el proyecto en GitHub Pages:
Para generar la página para producción ejecuta el comando:

npm run docs
Y a continuación:

Sube a tu repo la carpeta docs/ que se te acaba de generar.
git add -A
git commit -m "commit message"
git push
Entra en la pestaña settings de tu repo.
Y en el apartado de GitHub Pages activa la opción master branch /docs folder.
Además, los comandos:

npm run push-docs
o

npm run deploy
son un atajo que nos genera la versión de producción y hace push de la carpeta docs/ del tirón.

Flujo de archivos con Gulp
Estas tareas de Gulp producen el siguiente flujo de archivos:

Gulp flow

gulpfile.js y config.json
Nuestro gulpfile.js usa el fichero config.json de configuración con las rutas de los archivos a generar / observar.

De esta manera separarmos las acciones que están en gulpfile.js de la configuración de las acciones que están en config.json.

Estructura de carpetas
La estructura de carpetas tiene esta pinta:

src
 ├─ api // los ficheros de esta carpeta se copian en public/api/
 |  └─ data.json
 ├─ images
 |  └─ logo.jpg
 ├─ js // los ficheros de esta carpeta se concatenan en el fichero main.js y este se guarda en public/main.js
 |  ├─ main.js
 |  └─ events.js
 ├─ scss
 |  ├─ components
 |  ├─ core
 |  ├─ layout
 |  └─ pages
 └─ html
    └─ partials
Funcionamiento de la web
Búsqueda Se escribe en el input vacío creado para la búsqueda y al hacer click con el ratón sobre Search, la aplicación se conectará al API abierto de TVMaze para búsqueda de series. Obtenemos como respuesta un listado de elementos filtrados según lo que hayamos escrito en el input.

Favoritos Una vez aparecen los resultados de búsqueda, podremos indicar cuáles son nuestras series favoritas. Para hacer una serie favorita hacemos click sobre ella. Esta serie seleccionada cambiará su color de fondo y, además, se añadirá al listado de la izquierda donde veremos todas nuestras series marcadas como favoritas.

Almacenamiento local Hay que almacenar el listado de favoritos en el localStorage, de esta forma, al recargar la página, el listado de favoritos se mantiene como estaba.

BONUS: Borrar favoritos Como bonus, se propone añadir la opción de borrar los favoritos. Al hacer click sobre la "x" de la serie que queremos eliminar en el listado de la izquierda. Además añadir o quitar como favorito al hacer click sobre una serie del lado derecho y que si realizamos una nueva búsqueda y sale una serie que ya es favorita aparezca resaltada en los resultados. Incluir botón de reset para eliminar todos los favoritos a la vez.

BONUS: Afinar Maquetación Libertad para dar estilo a la página.

Falta algo?
Cualquier duda o sugerencia será bienvenida.

