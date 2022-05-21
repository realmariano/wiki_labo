# Contribuir a un repositorio de terceros (para principiantes)
created by @OleksiyRudenko [original english vesion](https://gist.github.com/OleksiyRudenko/236c3046fbba028e0555fa847dae7001)
translated to Spanish @realmariano


## Tabla de contenido

* [Requisitos previos ]( #requisitos previos)
* [Que vas a aprender]( #que-vas-aprender)
* [Un buen flujo de trabajo para empezar ]( #un-buen-flujo-de-trabajo-para-empezar)
	- [Inicializar cosas]( #inicializar-cosas)
	- [Agrega tus cambios]( #agrega-tus-cambios)
	- [Inicializar una rama de función]( #initialize-a-feature-branch)
	- [Ciclo de desarrollo de características ]( #ciclo-de-desarrollo-de-características)
	- [Limpiando ]( #limpiando)
* [Flujo de trabajo visualizado]( #workflow-visualizado)


## Requisitos previos

Conoces y usas comandos básicos de git como
`init`, `clone`, `add`, `commit`, 
`branch`, `checkout`, `merge`, `pull`, `push`.

Probablemente conoces y usas comandos de git como
`fetch`, `pull --rebase`, `rebase`, `cherry-pick`.

Quiere contribuir a un repositorio al que no tiene acceso de escritura.

No sabes o no te sientes seguro trabajando
con repositorios a los que no tiene acceso de escritura.

No sigue ningún flujo de trabajo firme trabajando con el suyo propio.
repos o repos no tiene acceso de escritura.

## Que aprenderás

* Cómo mantener tu bifurcación sincronizada con un repositorio fuente
* Cómo minimizar los riesgos de conflictos
* Cómo mantener el árbol del historial de su repositorio lo más limpio posible
* Cómo contribuir adecuadamente a través de solicitudes de extracción

## Un buen flujo de trabajo para empezar

Algunas definiciones:
- **upstream** es un repositorio al que desea contribuir
- **origin** o **fork** es tu propia bifurcación de un upstream
- **local** es un clon de origen local
- **master** es una rama predeterminada (`master` para repositorios más antiguos o `main` para repositorios más recientes)

### Inicializar cosas

1. Bifurque un flujo ascendente : en GitHub, navegue hasta el flujo ascendente y haga clic en el botón **Fork**.
1. `git clone <origin-url>.git <project-directory>`
en su máquina para clonar su bifurcación    on your machine to clone your fork
1. `cd <project-directory>`
1. `git remote add <upstream-url>.git` para habilitar acciones relacionadas con el flujo ascendente

### Agregue sus cambios

Es importante tener su bifurcación sincronizada con upstream,
emplear sucursales y seguir cierto flujo de trabajo
para minimizar los riesgos de conflictos y mantener el árbol histórico de git del proyecto lo más limpio posible.

#### Inicializar una branch (rama) de características

1. sincronización local y origen con upstream
    `git checkout master && git pull upstream master && git push origin master`
1. crea una rama de características con un nombre significativo
    `git checkout -b <feature-branch-name>`
    
> Hay muchas convenciones de nombres de sucursales. Algunos para mencionar son:
> * comenzar con las iniciales del autor para que otros colaboradores sepan quién
> inicializó la rama y también encontró ramas por autor, por ejemplo , `or-feature- portview`
> * use barras para denominar ámbitos, por ejemplo , `feature/ api /rest`, `bugfix/sleep`
> * use el ticket/número/epic/story id, por ejemplo , `feat/epic123/story128/search-people`



Alias útil:

`git config --global alias.sync -master '!git checkout master && git pull upstream master && git push origin master'`

Uso: `git sync-master`
 
#### Ciclo de desarrollo de características

1. haz lo que quieras en una rama de funciones dedicada
1. comete a menudo: `git add. && git commit -m "Agregar método REST api PATCH"`
1. squash eventualmente agrupando confirmaciones según corresponda:
`git rebase - i <REF>`
([Haciendo uso de git rebase]( https://gist.github.com/OleksiyRudenko/232e1ebe6ed0780fc69d7391723cc75b))
1. sincronizar eventualmente la rama local, de origen y de funciones con upstream
* `git checkout master && git pull upstream master && git push origin master`
* `git checkout - && git merge master`
* resuelve conflictos usando tu IDE o línea de comando
* cuando termine `git add. && git commit -m "Se resolvió el conflicto de fusión incorporando ambas sugerencias"`
* ver también
[Resolución de un conflicto de fusión mediante la línea de comandos]( https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/)
1. ir a `#1`
1. Eventualmente empujar al origen: `git push origin <feature-branch-name>`

Alias útil:

`git config --global alias.sync -branch '!git sync-master && git checkout - && git merge master'`

Uso: `git sync-branch` (también hace `sync-master` como parte del flujo)

**Mensaje de Commit (confirmación)**

Hay varias convenciones de estructura de mensajes de commit.
Por mencionar algunos:
* comenzar con el entorno de commit, por ejemplo, uno de los siguientes ` feat|fix|docs|style|refactor|test| chore`
* agregar función/arreglar alcance, por ejemplo, `( api )`
* use modo imperativo en la línea de asunto, por ejemplo, uno de `Add|Change|Fix|Refactor|Remove|Bump version|Release version`
 
Si resuelve un problema (en upstream o bifurcación --fork--), es útil tener una nota sobre la resolución del problema.

Su mensaje de confirmación puede parecerse al siguiente
```
fix ( foo api ): Fix ABC component render conditions

Resolves: #12
See also: #34, #78
```

Otras lecturas:
* [Commits convencionales 1.0.0-beta. 2]( https://www.conventionalcommits.org/en/v1.0.0-beta.2/)
*[Como escribir un mensaje de commit de Git ] (https://chris.beams.io/posts/git-commit/)
* [5 consejos útiles para un mejor mensaje de commit] ( https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
 * [ Semántica lanzamiento ] (https://github.com/semantic-release/semantic-release)
 * [aún más...](https://www.google.com/search?q=escribiendo+un+buen+mensaje+de+compromiso)

**NO HACER**

¡No aplastes ni hagas rebase de lo que ya está en el remoto!

¡No sobrescriba la historia de los remotos!
**NB**

Lo anterior no cubre el caso cuando trabajas en la misma branch (rama)
con alguien más,
en ese caso es preferible `git pull --rebase` sobre `git pull`.

### Contribuir a través de una solicitud de extracción (pull request)

Contribuir no es necesariamente obligatorio.
Puedes desarrollar tu tenedor para tus propios fines.
(cumpliendo con las condiciones de la licencia upstream).

De lo contrario, siga el siguiente flujo de trabajo de contribución:

1. `git push origin <feature-branch-name>` para enviar la rama de funciones al origen.
1. Navegue hasta el hub de git en la nube (p. ej., GitHub o Gitlab)
1. Use la interfaz de usuario en la nube para crear el PR
1. Pase por el proceso de revisión de código hasta que su
los cambios se fusionan o rechazan
    
Una vez que su rama de funciones se fusione, encontrará sus confirmaciones
en la próxima sincronización con upstream. Por lo tanto, no necesita fusionar esos
a su `master` localmente.

Sin embargo, deberá fusionarse con `master` si no contribuye al upstream o su PR es rechazado y desea
guardarlos para usted.

### Limpiar

Una vez que su PR sea aprobado y fusionado, puede deshacerse de su rama de características:
- `git branch -D feature-branch` localmente
- `git push --delete origin feature-branch` en tu control remoto

## Un mejor flujo de trabajo

<detalles><summary>Trabajo en curso bajo el corte</summary>

1. Mantén las cosas sincronizadas
1. Cuando la rama base (`maestro`) se actualice, rebase (cree una nueva base) la rama de características en ella
	- ¡NB! Si una rama de función ya está en remoto, entonces después de la reorganización
	Se requiere `push --force` para actualizar el control remoto; USE CON PRECAUCIÓN
	- una solución alternativa: bifurcarse desde el maestro (nueva bifurcación) y
	elegir individualmente desde la rama vieja o cambiar la base de la rama vieja a la nueva rama;
	eliminar la rama antigua tanto de forma local como remota
1. Cuando esté listo para actualizar `master`
	- selección idividual o rebase en maestro y squash (usando, por ejemplo, PR)
	- eliminar la rama de función
   
</detalles>


## Flujo de trabajo visualizado

[Flujo de trabajo básico de contribución de git visualizado](https://docs.google.com/presentation/d/13dati5gvA5f_hQFgxJPhPicjF5CRKu1e75RSsahmEaU)
