# Tomar notas con Markdown

<!-- TOC -->

- [Tomar notas con Markdown](#tomar-notas-con-markdown)
  - [Tabla de contenidos (TOC)](#tabla-de-contenidos-toc)
  - [Ecuaciones](#ecuaciones)
  - [Importar archivos](#importar-archivos)

<!-- /TOC -->

## Tabla de contenidos (TOC)

La tabla de contenidos se inserta fácilmente en forma  
`<!-- TOC -->` 
`- [Tomar notas con Markdown](#tomar-notas-con-markdown)`
`<!-- TOC -->`
acá puse sólo un ejemplo de una línea, pero en el código original (arriba de todo) hay un ejemplo completo de esta página.
Otra forma es bajar herramientas de Markdown, si usas el [markdown extension pack](https://marketplace.visualstudio.com/items?itemName=bat67.markdown-extension-pack#review-details) ya lo tenés, click derecho y seleccionás `Markdown TOC: insert/update`, te la va insertar en el lugar que lo hagas. Para hacer el update hacés lo mismo.

También adicioné [Markdown Shortcuts](https://marketplace.visualstudio.com/items?itemName=mdickin.markdown-shortcuts). Este permite ir haciendo toggle (cambiar rápidamente) texto a un formato específico de markdown. Por ejemplo pasar a una tabla valores, icluir bullets en un texto, etc.

En mi caso uso VSC (visual studio code) para escribir, en este caso desde una actualización reciente resulta que hay un problema con el código de fin de línea. Si usás VSC entonces seguí leyendo, sino no creo que te vaya a interesar este párrafo.

Resulta que el VSC modificó el fin de línea a `file.eol` a `auto` esto te va a aparecer cuando uses el TOC automático, para evitarlo hay que cambiar el setting de  `file.eol` a `\n` esto es desde el user settings ponés en la búsqueda `file.eol` y te aparece la opción de modificación. Todo esto está descripto en el repo de [Alan Walk markdown-toc](https://github.com/AlanWalk/markdown-toc/issues/65).
No me queda claro si esto puede generar otros problemas, ya que se está modificando una variable global, aún no me generó problemas pero puede pasar.

## Ecuaciones

Para meter ecuaciones simplemente se usa latex
`$$ \alpha = \frac{e^2}{4\pi\varepsilon_0\hbar c} = \frac{\mu_0 e^2 c}{4 \pi \hbar} = \frac{c \mu_0}{2 R_K} = \frac{1}{137} $$` :

$$ \alpha = \frac{e^2}{4\pi\varepsilon_0\hbar c} = \frac{\mu_0 e^2 c}{4 \pi \hbar} = \frac{c \mu_0}{2 R_K} = \frac{1}{137}
$$

## Importar archivos

Con el Markdown all in one es sencillo meter figuras, puede ser de carpetas en otros lugares, en el mismo o de la web. Pueden ser imágenes, PDF, y muchos otros, simplemente:

`@import "/figures/prueba dibujo 01.jpg"`

Y te sale la imagen: 

@import "/figures/prueba dibujo 01.jpg"


