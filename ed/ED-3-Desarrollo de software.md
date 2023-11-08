#curso23_24 #ED [estado:: Working] 

## Licencias de software

En Derecho, una licencia es un contrato mediante el cual una persona recibe de otra el derecho de uso, de copia, de distribución, de estudio y de modificación (en el caso del Software Libre) de varios de sus bienes, normalmente de carácter no tangible o intelectual, pudiendo darse a cambio del pago de un monto determinado por el uso de los mismos. Estos activos son propiedad del otorgante, y pueden ser bienes de propiedad intelectual como una marca, patentes o tecnologías. También pueden ser objeto de licencia otros bienes de carácter intangible como la distribución de obras intelectuales.

En la práctica, si un software carece de licencia el receptor del mismo no tiene derecho ni si quiera a ejecutarlo, ya que no tiene otorgado el permiso para ello.

Por ejemplo, MacOs se distribuye con una licencia que impide su instalación y ejecución en cualquier equipo que no sea directamente hardware de Apple Inc, por lo que su virtualización está implícitamente prohibida.

Entrando en tipos de licencias nos encontramos los distintos palabros: Copyright, Freeware, Open Source, GPL, MIT, Apache, BSL, entre muchas otras.

Vamos a definir a grandes rasgos las mismas:
+ Copyright: sólo lo otorgado expresamente. Windows, MacOs o Office son un ejemplo.
+ Freeware: puedes ejecutarlo gratuitamente, pero tendrá limitaciones temporales o de funcionalidades.
+ Open Source: se distribuye el código fuente, pero su modificación o ejecución sigue siendo de pago.
+ Software libre: aquel que respeta las 4 libertades:
  1.  La libertad de ejecutar el software como te plazca y con cualquier objetivo.
  2.  La libertad de estudiar como funciona el programa y cambiarlo a tu gusto. Esto implica el poder acceder a su código fuente.
  3.  La libertad de poder redistribuir copies del programa a los demás.
  4.  La libertad de poder distribuir también tus mejoras al programa original.
+ GPL (General Public License) (ver referencia). Obliga que el software derivado se distribuya también con la misma licencia, no así las modificaciones.
+ BSD: El software derivado no requiere ser liberado bajo la misma licencia.
+ MIT: *casi* de dominio público.
+ Apache: ...
+ BSL (Business Source License): es gratis y abierto mientras no le hagas la competencia al creador... aceptan tus mejoras y se las quedan 😠.

![BSL](https://luiscastelar.duckdns.org/2023/assets/ED/UT3-licencia-bsl.jpg)


**Referencias:** [licencias - picodotdev](https://picodotdev.github.io/blog-bitix/2021/02/licencias-de-software-libre-y-diferencias-con-software-privativo-y-de-codigo-abierto/)

## Ciclo de vida
[evotic](https://evotic.es/software-a-medida/ciclo-de-vida-del-software/)

### Modelelos de desarrollo:

+ En cascada: \
![en cascada](https://www.ionos.mx/digitalguide/fileadmin/_processed_/0/8/csm_wasserfallmodell-ES-1_f6eb5b1dc6.webp)
+ En V: \
![en v](https://www.datocms-assets.com/17507/1616761097-captura-de-pantalla-2021-03-25-a-las-10-43-22.png?fit=max&fm=webp&q=60&w=736)
+ En espiral: \
  ![espiral](https://3.bp.blogspot.com/-uEYkRrdS0cI/W9nbKU0XxCI/AAAAAAAAABo/0_pqo68Sn-kuBGcnOgSaa4ZB4TNYrYKWQCLcBGAs/s1600/iaaaarasrsat.png)
+ Incremental (métodos `Agile`): Scrum y Kanban

### KANBAN


![kanban board](https://www.ionos.es/digitalguide/fileadmin/_processed_/1/a/csm_kanban_a62fb56a0a.webp)

1. [Qué es - ionos](https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/que-es-kanban/)
2. [Gestion de proyectos con KANBAN - YT: Marta Falcón](https://www.youtube.com/watch?v=WP6Nt5XV980)
3. [kanboard](https://kanboard.luiscastelar.duckdns.org/board/1) o [WeKan](https://github.com/wekan/wekan)
4. [Kanban en Github](https://libliboom.medium.com/how-to-use-automated-kanban-in-github-cf073f18a6c8)

Ejemplo de Kanboard para desarrollo:

![kan](https://luiscastelar.duckdns.org/2023/assets/ED/UT3-kanboard.jpg)

#### Tarea 1: 
Crea un repositorio NUEVO y conviértelo en un KanBoard siguiendo los pasos indicados en el enlace 4.


### Scrum

![scrum](https://luiscastelar.duckdns.org/2023/assets/ED/UT3-srum.jpeg)
![scrum](https://luiscastelar.duckdns.org/2023/assets/ED/UT3-ScrumBoard.jpeg)
**Referencias:**
+ [Scrum en 10 minutos - YT:Juan Carlos Marin](https://www.youtube.com/watch?v=PlLHc60egiQ)
+ [Qué es SCRUM - YT: EDTeam](https://www.youtube.com/watch?v=sLexw-z13Fo)


#### Tarea 2: 
~~Crea un repositorio NUEVO y conviértelo en un Scrum Board~~ (ver [ejemplo](https://github.com/users/itzrick620/projects/4/views/1))


## PoC, Prototipo y PMV

1. Prueba de Concepto (PoC): es algo mínimo que nos indica la posibilidad o no de realizar algo. Por ejemplo, el “Hola mundo” que realizamos los programadores es una PoC sobre la viabilidad de utilizar ese lenguaje o FrameWork.
2. Prototipos: Más habitual en otras industrias, por ejemplo automoción o aviación.
3. Proyecto Mínimo Viable: es la cantidad mínima de funcionalidades o “Historias de Usuario” que necesitamos implementar para poner en el mercado nuestro producto.


## Códigos fuente, objeto y ejecutable
 + [ ] Código fuente, código objeto y código ejecutable; tecnologías de virtualización.

+ Nuestro lenguaje de alto nivel (C) `hola.c`

  Cojamos un un `HolaMundo.java` que conocemos (*o casi*):
  ```java
  void main(){
    System.out.println( "Hola mundo" );
  }
  ```
  *Para ejecutar el código anterior: `java --enable-preview --source 21 hola.java`*.

  Y veamos las similitudes con su homólogo en C:
  ```C
  #include <stdio.h>

  int main(){
    printf( "Hola mundo." );
    return 0;
  }
  ```


  
+ Código ensamblador <- `gcc -S hola.c` => `hola.s`

+ Código máquina
  + Desde código fuente: `gcc -c hola.c` 
  + Desde ensamblador: `as hola.s -o hola.o`
  
+ Código máquina enlazado (creación de proceso) <- `gcc hola.c -o hola.exe`
![multiproceso](https://luiscastelar.duckdns.org/2023/assets/ED/UT3/pcb.png)
  
  ![multiproceso](https://luiscastelar.duckdns.org/2023/assets/ED/UT3/memoria_ppal.png)
También desde el código no enlazado `ld /usr/lib/x86\_64-linux-gnu/crti.o /usr/lib/x86\_64-linux-gnu/crtn.o /usr/lib/x86\_64-linux-gnu/crt1.o -lc hola.o -dynamic-linker /l  
ib64/ld-linux-x86-64.so.2 -o hola.exe`.

***Truco:*** *imposible acordarse de todo... man, comando --help y cheat.sh son vuestros amigos*.


## Paradigmas de la programación:
+ Paradigma imperativo:
  + Diseño estructurado: Diseño de datos, diseño arquitectónico, diseño de interfaz y diseño procedimental (secuencial, condicional, repetitiva).
  + Diseño orientado a objetos: agregación y composición.
+ Programación funcional \
  > En informática, la programación funcional es un paradigma de programación declarativa basado en el uso de verdaderas funciones matemáticas. En este estilo de programación las funciones son ciudadanas de primera clase, porque sus expresiones pueden ser asignadas a variables como se haría con cualquier otro valor; además de que pueden crearse funciones de orden superior.
  > Fuente: [Wikipedia](https://es.wikipedia.org/wiki/Programaci%C3%B3n_funcional).
  + Características:
    + sólo funciones (sin repetitividad)
    + sin variables
  + *Repetitividad* vs *Recursividad*
  + [Su presencia en `Java`](https://blog.codmind.com/que-es-la-programacion-funcional-en-java/)

## Compilación/Interpretación y ejecución
 + Java
 
 *Requisito Vagrant*
 + PHP y Python
 
 + javascript
 + [C++ en VS Code](https://code.visualstudio.com/docs/cpp/config-mingw) y [C++ con MinGW](https://es.wikihow.com/compilar-un-programa-en-C-usando-el-compilador-GNU-%28GCC%29)
 + [C#](https://desarrolloweb.com/articulos/primer-programa-csharp)



## Continuación:
+ [Desarrollo de software - fases](https://github.com/jamj2000/DAW1-ED-Apuntes/blob/master/1.ELEMENTOS.md#desarrollo-de-software)
+ [Lenguajes de programación](https://github.com/jamj2000/DAW1-ED-Apuntes/blob/master/1.ELEMENTOS.md#lenguajes-de-programaci%C3%B3n)