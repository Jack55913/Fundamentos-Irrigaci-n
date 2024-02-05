# Apuntes de la Ingeniería en Irrigación

## .gitignore

Es un archivo para evitar subir las carpetas build y .vscode, éstos no debe subirse a GitHub porque son carpetas de compilación local.

## La carpeta Chapters

Aquí será el espacio de trabajo. El número de carpeta (1) indica primer semestre, al abrirla, se tendrá acceso a las notas de cada materia.

## La carpeta tools

Contiene la carpeta **assets**, en la cuál, deberá ser almacenada todo tipo de imagen (Sólo en formato PNG, PDF y JPG).

En el archivo chapters.tex contiene todos los archivos ordenados por semestre.

sleek-lisstings y Stylelnd.ist sirven para darle formato al libro.

### - structure.tex

Aquí contendremos todos los paquetes utilizados.

*No es necesario modificar absolutamente nada de la carpeta tools, a menos que se agregue una imagen.*

### - Notas

Algunos comandos fueron usados para optimizar el tiempo de ésta obra,
favor de revisar la paleta de comandos.

## ¿Cómo usar éste repositorio?

Cada que queremos compilar, se debe de ingresar al archivo main.tex y luego modificar algo pequeño (Un espacio, un enter, etc).

En el archivo z.tex puedes escribir código más rápidamente, ya que VsCode al tener más de 500 líneas de código, empieza a hacerse lento, más que es un repositorio grande, así que para no estar esperando a que haga una compilación de 10 minutos (Como habitualmente lo haría con la versión final del libro), entonces en la carpeta tools/chapters selecciona todos los archivos y pulsa `ctrl + ]`, esto hace un bloque de comentarios, así que estarán inactivos, ahora sólo quítale el símbolo `\%` al archivo que quieres analizar.

En su defecto, puedes usar el comando `\template + enter` para crear lo siguiente: 

~~~
%%%%%%%%%%%%%%%%%%%%%%%%%%%%% Define Article %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\documentclass{article}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%%%%%%%%%%%%%%%%%%%%%%%%%%%% Using Packages %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\usepackage{geometry}
\usepackage{graphicx}
\usepackage{amssymb}
\usepackage{amsmath}
\usepackage{amsthm}
\usepackage{empheq}
\usepackage{mdframed}
\usepackage{booktabs}
\usepackage{lipsum}
\usepackage{graphicx}
\usepackage{color}
\usepackage{psfrag}
\usepackage{pgfplots}
\usepackage{bm}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

% Other Settings

%%%%%%%%%%%%%%%%%%%%%%%%%% Page Setting %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\geometry{a4paper}

%%%%%%%%%%%%%%%%%%%%%%%%%% Define some useful colors %%%%%%%%%%%%%%%%%%%%%%%%%%
\definecolor{ocre}{RGB}{243,102,25}
\definecolor{mygray}{RGB}{243,243,244}
\definecolor{deepGreen}{RGB}{26,111,0}
\definecolor{shallowGreen}{RGB}{235,255,255}
\definecolor{deepBlue}{RGB}{61,124,222}
\definecolor{shallowBlue}{RGB}{235,249,255}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%%%%%%%%%%%%%%%%%%%%%%%%% Define an orangebox command %%%%%%%%%%%%%%%%%%%%%%%%
\newcommand\orangebox[1]{\fcolorbox{ocre}{mygray}{\hspace{1em}#1\hspace{1em}}}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%%%%%%%%%%%%%%%%%%%%%%%%%%% English Environments %%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\newtheoremstyle{mytheoremstyle}{3pt}{3pt}{\normalfont}{0cm}{\rmfamily\bfseries}{}{1em}{{\color{black}\thmname{#1}~\thmnumber{#2}}\thmnote{\,--\,#3}}
\newtheoremstyle{myproblemstyle}{3pt}{3pt}{\normalfont}{0cm}{\rmfamily\bfseries}{}{1em}{{\color{black}\thmname{#1}~\thmnumber{#2}}\thmnote{\,--\,#3}}
\theoremstyle{mytheoremstyle}
\newmdtheoremenv[linewidth=1pt,backgroundcolor=shallowGreen,linecolor=deepGreen,leftmargin=0pt,innerleftmargin=20pt,innerrightmargin=20pt,]{theorem}{Theorem}[section]
\theoremstyle{mytheoremstyle}
\newmdtheoremenv[linewidth=1pt,backgroundcolor=shallowBlue,linecolor=deepBlue,leftmargin=0pt,innerleftmargin=20pt,innerrightmargin=20pt,]{definition}{Definition}[section]
\theoremstyle{myproblemstyle}
\newmdtheoremenv[linecolor=black,leftmargin=0pt,innerleftmargin=10pt,innerrightmargin=10pt,]{problem}{Problem}[section]
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% Plotting Settings %%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\usepgfplotslibrary{colorbrewer}
\pgfplotsset{width=8cm,compat=1.9}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% Title & Author %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\title{Title}
\author{Haoyun Qin}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\begin{document}
    \maketitle
    
\end{document}
~~~

Luego de eso, pegar lo que se había trabajado, sin embargo debe tomarse en cuenta las configuraciones de las imagenes, y bibliografía. [Ver el siguiente video: tutorial](https://youtu.be/jIh_gBND02U).

Finalmente las tablas las genero aquí: [table generator](https://www.tablesgenerator.com), todas las tablas del libro tienen el mismo formato, donde dice "Default table style", se debe cambiar al que dice "booktabs table style" seleccionando a toda la tabla.

Si se requiere visualizar ecuaciones, puedes ir al siguiente enlace: [Visualizar ecuaciones](https://editor.codecogs.com/?lang=es-es), en su defecto puedes pulsar: `ctrl+shift+p`, para abrir el navegador en la parte superior y luego escribir: **open math preview panel** y se abrirá el panel.

Por último, para ver cómo funciona el uso de github, revisa el siguiente tutorial: [tutorial de GitHub](https://youtu.be/hWglK8nWh60)
