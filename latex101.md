# Uso de LaTeX y notas varias al respecto


Al principio __LaTeX__ (creado por 	Leslie Lamport, ver <https://www.latex-project.org//>, <https://github.com/latex3/latex2e>) puede resultar complejo si no estamos acostumbrados a usarlo, pero es por lejos mucho mejor que otras metodologías WSWYG (what you see is what you get) como el Word. 
Por lejos es muy superior, especialmente para excribir textos técnicos y complejos, además nos permite modificar el estilo completo de nuestro texto simplemente modificando el encabezado del proyecto (el lugar donde indicamos cómo queremos que se vea todo).

Otra opción, que tiene un poco de ambos mundos, es el __Markdown__ (método en el que está escrito este texto). Este lo hicieron John Gruber and Aaron Swartz, (<https://daringfireball.net/projects/markdown/>,<https://ashki23.github.io/markdown-latex.html>,<https://www.markdownguide.org/>) y es un lenguaje que se lee fácil al escribir y en el resultado de compilación. Se usa en muchos lugares, ej wiki e infinidad de blogs. De paso si no la conocen la historia de Swartz es muy interesante y se cuenta en el documental Internet´s own boy  (<https://en.wikipedia.org/wiki/The_Internet%27s_Own_Boy>).

## LaTeX

Volviendo al quid de la cuestión, LaTeX es muy bueno y es ideal que uno lo use, para ello la forma actual más sencilla es utilizar el omnipresente _Overleaf_(<www.overleaf.com>). Esto evita tener que instalar cosas en la pc y preocuparse por compatibilidades y editores al principio.

La idea de este texto es incluir cosas que se pueden necesitar normalmente, pero no ser completo, para esto hay muchos mejores introducciones.


En _Overleaf_ está la posiblididad de hacer corrección ortográfica en el idioma que uno quiera yendo a _menu_, como se muestra en la siguiente imagen 
![Idioma Overleaf](/figures/overleafIdioma.png "Elegir idioma en overleaf")
y de allí se pueden seleccionar varias cosas, el idioma entre ellas.

Además, se puede elegir el archivo .tex principal que uno utiliza, esto es importante cuando estamos haciendo varias versiones. Si no cambiamos acá va a seguir compilando con el viejo.

### Paquetes de LaTeX

Para incluir paquetes usamos en el prefacio, antes de que empiece el documento con '\begin{document}', la sentencia '\usepackage{PAQUETE}'. 
En general la página de Overleaf tiene muchos y buenos ejemplos de los distitntos paquetes. Pero cada paquete tiene su repo en CTAN <https://ctan.org/> y nos indica cómo usarlo. 

A continuación una lista de aquellos usuales que son importantes poner, no dudes en incluir otros y hacer un comit para que se sumen a este texto:


1. __siunitx__ Este paquete te sirve para incluir unidades en el SI, <https://ctan.org/pkg/siunitx?lang=en>, <https://texdoc.org/serve/siunitx/0>. En el segundo link se muestra todo lo relacionado al paquete y dan ejemplos de cómo usarlo.
2. __graphicx__ Para inclusión de gráficos.
3. __hyperref__ Para hacer hipervínculos entre secciones y gráficos. Se pueden elegir colores y muchas más cosas


