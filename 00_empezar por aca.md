# Leeme antes de empezar  

2021-10  
_Mariano A Real_

<!-- TOC -->

1. [Leeme antes de empezar](#leeme-antes-de-empezar)
      1. [Cuaderno](#cuaderno)
         1. [Markdown](#markdown)
         2. [LaTeX](#latex)
      2. [Repositorio/webcloud:](#repositoriowebcloud)
      3. [Papers, libros y mantener bibliografía](#papers-libros-y-mantener-bibliografía)
         1. [Sistema non-santo:](#sistema-non-santo)
      4. [Metrología](#metrología)

<!-- /TOC -->



Este documento tiene información importante y mucha que seguro ya conoce el lector, sepa disculpar eso y concéntrese en lo que no conocía. Otras cosas seguro las conoce, pero es importante que se repitan, ejemplo el cuaderno de laboratorio.

Además, es un archivo que cambia y que si le agrega cosas que crea que vayan a servirle al prójimo, nos vendría re bien que las incluya. Gran parte de este texto está pensado en estudiantes de grado.

Obsérvese que este documento está escrito en Markdown, y lo puede descargar de https://github.com/realmariano/wiki_labo. Más abajo se incluye info acerca de este sistema.


### Cuaderno
Para el laboratorio tenés que llevar un cuaderno, esto hoy en día se está transformado en digital de a poco.  
Es fundamental que todos los días de laboratorio lleves un buen recuento de lo que vas haciendo, no va sólo lo que funciona, también de lo que no anduvo, ya que muchas veces evita que dupliques errores (vos o alguien que lo utilice luego). Además dentro de lo posible tiene que ser algo que otra persona pueda entender y seguir.  

Si utilizás un cuaderno en papel utilizá siempre el mismo y sólo para el laboratorio. Y todos los días hay que tomarse el trabajo de completarlo de forma correcta, no dejes de poner lo que hiciste, ideas, cuentas, todo lo que necesites.  
Además, es uno de los objetivos de la materia, tener un buen cuaderno de laboratorio (labo 6 y 7).  
En nuestro el laboratorio por ejemplo cada sistema tiene su cuaderno, y llevamos en él un recuento de los arreglos, mediciones y demás situaciones que se dieron en cada sistema.  

También es posible utilizar un cuaderno digital, tiene sus ventajas y desventajas.  
En caso de usar esta opción, podés usar cualquier sistema que te resulte conveniente (abajo te dejo dos opciones sólo por si no los conocés), sin embargo creo que es fundamental que siempre te generes una salida en pdf que pueda ser leída por cualquier persona. 
Estos archivos muchas veces son muy dependientes del programa y si deja de existir o no tenés más licencia perdés todo (ej word, onenote, sistemas google, etc). El pdf es de lo más universal dentro de los formatos de salida compleja que existen hoy. 


#### Markdown

Un lenguaje muy utilizado hoy y bien sencillo para tomar notas rápidas es Markdown. Lo utilizan en infinidad de páginas web (ej. Wikipedia, GitHub) hoy en día y te deja generar salidas de diferentes tipos (pdf, html, etc) muy legibles.
https://markdown.es/
En el repositorio de abajo hay un ejemplo sencillo de uso:
https://github.com/realmariano/uso-Markdown/blob/master/Notas%20Markdown.md


Podés usar cualquier editor de texto para generarlo y simplemente salvar usando .md

Varios editores traen además un visor Markdown que te muestra la salida en forma bonita (ej  Notepad++, VSC, jupyter notebook, jupyterlab, etc)

#### LaTeX

Por supuesto otra opción es LaTeX. Es de lo más completo que podés encontrar y es muy sencillo generar un archivo que te permita armar un cuaderno de laboratorio a tu gusto. 
En este caso tenés dos opciones: a- usar versión local (instalar) o b- usar versión web:

__a- Versión local__

Instalar MikTeX o TeXlive y luego un editor que te guste.  
 
_Instalar LaTeX_

[MikTeX](https://miktex.org/)   
[TeX live](https://www.tug.org/texlive/)  

La gran diferencia entre ellos (al menos al momento de escribir esto) es que el MikTeX deja bajar un mínimo de cosas e instalar _on the fly_ (cuando se usan). En cambio el TexLive baja un mega conjunto de paquetes.

_Editores:_

* [TeXstudio](www.texstudio.org) 
* [Texmaker](https://www.xm1math.net/texmaker/) 
* [TeXnicenter](https://www.texniccenter.org/) 
* [LyX](https://www.lyx.org/Home)	Este es bastante distinto a los otros, usa una mezcla de WYSWYG (estilo Word) con LaTeX.  
* [VSCcode](https://code.visualstudio.com/)  Este deja programar lo que sea, para que ande el LaTeX hay que bajar desde el sistema de marketplace que tiene el [LaTeX workshop extension](https://link-url-here.org), que además necesita tener instalado el [TeX live](https://www.tug.org/texlive/)
  
Infinidad de otros que se pueden encontrar en la web.  


__b- Versión web__

Otra opción muy buena es [Oveleaf](https://www.overleaf.com/) la ventaja es que podés hacerlo colaborativo (restringido si no se paga) y compartirlo muy fácil. Además ya te queda en la web. También, tiene infinidad de modelos de presentaciones, y todo anda, en el sentido que no es necesario preocuparse por la parte de compatibilidad y compilación, se encarga el server web de todo esto.

Otra opción son las notebooks de [Jupyter](https://jupyter.org/) o [Jupyterlab](https://jupyterlab.readthedocs.io/en/stable/), o de [Google Colab](colab.research.google.com/) que te deja armarte un Notebook que además te permite mezclar código, figuras, Markdown, Latex y exportar en el formato que más te convenga. 

#### Incluir bibliografía

Seguro usar bibTeX, una buena opción es usar natbib de backend, ver 
[natbib1](https://gking.harvard.edu/files/natbib2.pdf)
[natbib2](http://merkel.texture.rocks/Latex/natbib.php?lang=en) para opciones y estilos

### Repositorio/webcloud:  

Es muy importante que tengas un buen respaldo y control de versión para lo que programes, midas y hagas.
__Git__, que fue ideado y programado por Linus Torvalds (el mismo del kernel de Linux), es uno de los mejores.
En esta direccion hay varios servicios:
[GitHub](https://github.com) es la opción más usual. Sirve sólo para que subas programas, notas o similar (texto) que no incluya mediciones muy grandes o muchas imágenes (creo te dan de baja la cuenta si lo hacés, y no es la idea del servicio). 
Otra ventaja es que es muy sencillo compartir cosas de esta forma.  

Del mismo estilo (más controlable) es [GitLab](https://about.gitlab.com).

Otras opciones son subversion, por ejemplo.
Y por supuesto sistemas como Gdrive, OneDrive, Mega, Box, Dropbox, o directamente un servidor.


__Si usás un cuaderno digital, es fundamental que todo lo tengas respaldado en algún lado de tu preferencia.__ 


### Papers, libros y mantener bibliografía

Hoy en día los lugares sine qua non de búsqueda bibliográfica (para física y electrónica al menos) son:

* scholar.google.com (hacete un perfil), google empezó así, Sergey y Larry trabajaban en el page rank que aplicaron a bases de datos de papers inicialmente. Hoy en día tiene muchos adicionales. La posiblidad de asociar un ___perfil___, donde guarda ___tus publicaciones___ y presentaciones a congresos con referato. También tiene la posibilidad de salvar papers en ___tu biblioteca___ etiquetar y ordenar. Podés exportar citas en diferentes formatos, en particular en .bib tanto de trabajos individuales como en bulk con el botón exportar.
* arXiv.org (repositorio de pre-prints de Cornell). Acá la gente suele poner sus pre-prints, el paper casi listo para enviar a revisión de publicación. Para que la gente le diga si está bueno o si tiene errores antes de enviarlo. Pero también para que todos podamos acceder. Cuando buscás en scholar algo, te aparece abajo la opción de “otras versiones” ahí suele estar la versión arXiv. Es libre y abierto. Y una vez publicado un paper luego se indica la versión final allí.

Luego está la biblioteca de [MinCyT](https://repositoriosdigitales.mincyt.gob.ar/vufind/)

Y si estás conectado desde instituciones tipo universidades o el INTI tenés acceso a las revistas que paga el estado para bajar los papers y libros en cuestión. Varias revistas están suscritas desde el ministerio, pero no específicamente a INTI (un ejemplo PRL), en caso de que esto pase basta tomar el DOI del artículo en cuestíon y solicitar un "préstamo" en la página de la biblioteca digital [servicio de préstamos](https://biblioteca.mincyt.gob.ar/prestamo).

Finalmente, INTI tiene una muy linda biblioteca con gente muy dispuesta y capaz, siempre que tengan dudas o necesiten algún libro pueden ir a verlos o escribirles a biblio@inti.gob.ar

#### Sistema non-santo: 

SCI-HUB, creado por Alexandra Elbakyan, quien si no merece el premio nobel por avanzar la ciencia mundial le pega en el palo. 

Se buscan mirrors por la web y se ingresa el DOI de la revista deseada. También tiene un bot en Telegram excelente que te permite hacerlo más sencillo.

LibGen, idem anterior para libros digitales. También tiene un bot en Telegram con la misma función.

Ahora bien, uno se baja una banda de papers. Que se asume leimos y entendemos aunque lo segundo y muchas veces lo primero, no siempre sucede. Y surgen dos problemas: mantenerlos ordenados y citarlos en nuestros escritos sin que sea un incordio. Para esto se usan los gestores de librerías, se pueden buscar todos los que hay en Wiki, yo probé los siguientes:

[Mendeley](https://www.mendeley.com/) gratis, multiplataforma y te permite mantener coordinación con varias máquinas. Tiene el problema que si la base se vuelve grande se pone lento y medio complicado. No es abierto y pertenece a Elsevier. Te asocia los pdf a los registros de cita y te los ordena de la forma que desees. Además si le indicás una carpeta te busca todos los trabajos que hay ahí mira en la web la información y te la adosa automáticamente. Es muy completo e hyper sencillo de usar. En mi caso, lo dejé de usar hace un tiempo porque se me puso muy pesado y me generaba problemas con algunas referencias, sé que ha mejorado mucho desde esa época.

[Zotero](https://www.zotero.org/): abierto, multiplataforma, portable, etc, etc, etc. Lo podés llevar en un pendrive por ejemplo y correrlo desde ahí. La desventaja que le vi es que la base de datos y el manejo de los pdf se vuelve un tanto complicada, si uno pierde la info o tiene algún problema. Los pdf quedan asociados a una entrada de la base (es un número) y no están todos juntos en algún lugar, queda cada uno dentro de una subcarpeta con el número de la base de datos. Es extremadamente probable que haya soluciones elegantes y sencillas a los problemas que le ví. 

[JabRef](https://www.jabref.org/): similar a Zotero, abierto, multiplataforma, portable y funciona bien y rápido. Tiene sus bemoles respecto a importación de cosas. También te busca todos los trabajos que hay en una carpeta determinada automáticamente. Y sumás las referencias muy fácil con el formato bib. Además para muchos papers te da referencias de otros que son de temáticas similares y te pueden interesar.

Bibliografía de la bibliografía: cuando uno tiene un paper tiene un montón de referencias, la única forma que encontré por el momento de bajarlas

### Metrología

El INTI es un organismo de metrología, tecnología e industria. 

Páginas importantes relevantes al respecto:

* __BIPM__: www.bipm.org. Acá vas a encontrar un montón de información de metrología y varios artículos y documentos relevantes.
* __CODATA__ Bbase de datos de constantes fundamentales físicas, la mantiene NIST y es EL lugar donde buscar la información relevante de constantes universales, https://physics.nist.gov/cuu/Constants/ 

Equivalentes del INTI en el mundo
*	NIST - USA	https://www.nist.gov/  
*	PTB - Alemania https://www.ptb.de/   
*	NPL - GB https://www.npl.co.uk/   
*	METAS - Suiza https://www.metas.ch/metas/en/home.html   
*	AIST - Japón https://www.aist.go.jp/aist_e/dept/en_nmij.html   
*	NIM - China https://en.nim.ac.cn/   
*	CENAM - México https://www.cenam.mx/servicios/   
*	INMETRO - Brasil https://www.gov.br/inmetro/pt-br  
*   KRISS - Corea del Sur https://www.kriss.re.kr/
*   NRC - Canadá https://nrc.canada.ca/en/research-development/research-collaboration/research-centres/metrology-research-centre
*   INM - Colombia https://minciencias.gov.co/content/uae-instituto-nacional-metrologia-inm
*   CEM - España  https://www.cem.es/es  
*   INRiM - Italia https://www.inrim.eu/  
*   VSL - Países BAjos https://www.vsl.nl/en

Y un montón más.  

### Patentes y propiedad intelectual
* [Google Scholar](scholar.google.com) poniendo a la izquierda _mostrar sólo patentes_ o también en 
* [Google Patents](patents.google.com)
* [OMPI/WIPO]( https://www.wipo.int/about-ip/es/index.html) base de datos internacional de patentes
* [Patent Scope](https://patentscope.wipo.int/search/es/search.jsf)
      • Página oficial de la WIPO / OMPI
      • +84 millones de documentos, + 42 países
      • Búsquedas multilingües
      • Sistema de traducción automática (Wipo Translate)
      • CLIR (Cross-Lingual Information Retrieval)
      • Título, Resumen, Reivindicaciones, Texto completo, CIP
      • Búsqueda por figuras
      • Graficas estadísticas
      • Función stemming (acid: acidity, acidic)
      • RSS
* [INPI](https://www.argentina.gob.ar/inpi) oficina Arg. de patentes
* [INPI búsqueda](https://www.argentina.gob.ar/inpi/patentes/buscar-e-investigar-patentes)
* [USPTO](https://www.uspto.gov/) oficina USA de patentes
* [OEPM](https://www.oepm.es/es/index.html) oficina española de patentes
* [Espacenet](https://worldwide.espacenet.com) oficina europea de patentes
* [Lens](https://www.lens.org/)
      • +96M, +90 países
      • Búsqueda por palabras en varios idiomas
      • Título, Resumen, Reivindicaciones (en forma individual o en conjunto)
      • Incorpora documentos científicos (PUBMED)
      • Buscador de clasificaciones CPC / CIP
      • Gráficas estadísticas (muy bunas)
      • Función stemming (acid: acidity, acidic)     
    
