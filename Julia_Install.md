## Cómo instalar Juila o otros accesorios.

Aqui daremos las instrucciones para instalar Julia y otros accesorios.

### Instalando Julia:

La instalación de los binarios de Julia es bastante sencilla. Primero, vaya a la [página:](https://julialang.org/downloads/). Allí elija la instalación de acuerdo al sistema operativo de su computadora. Hoy en día casi todas las computadoras ya son de 64bits, pero por las dudas constate si no es de 32 bits, en tal caso use el apropiado. Siga las instrucciones de instalación de acuerdo a su sistema.
        
### Trabajando con Julia

Hay varias maneras de trabajar a la hora de escribir programas de cierta complejidad:
    
**1. Terminal o cónsola de Julia** Cuando iniciamos Julia, se abre una terminal o cónsola en donde podemos ejecutar comandos de Julia. La terminal de Julia luce algo así

    julia>
   
   Aquí podemos, por ejemplo, ingresar comandos o instrucciones numéricas tales como
   
    julia> 1 + 2
    3

   en donde vemos, tras presionar la tecla Enter, que Julia imprime el resultado de la instrucción ingresada. Para salir de la cónsola de Julia, ingrese el comando `exit()`.
    
**1. Editor de texto** Usualmente para trabajar con códigos un poquito complicados es mejor hacerlo usando un editor de texto apropiado (no de texto enriquecido como Word u Open Office). Para linux recomendamos `kate` o `geany`. Para Windows recomendamos [geany](https://www.geany.org/download/nightly-builds/) o [notepad++](https://notepad-plus-plus.org/downloads/v7.9.3/). Veamos un ejemplo. Cree con su editor de texto un archivo llamado `hola.jl` con el siguiente contenido

    println("Hola mundo!")
    
   Luego, inicie la cónsola de Julia e ingrese el siguiente comando
   
    include("hola.jl")
    Hola mundo!
    
   Vemos que Julia ha ejecutado las instrucciones indicadas en el archivo.
    
**2. Usando notebooks** Una vez que hayan adquirido un poco de experiencia es recomendable usar notebooks. 
    Los notebooks se trabajan en el browser que está configurado como principal es su sistema. 
    Recomendamos usar **Chrome**.
    Tienen la ventaja que los códigos se pueden ejecutar por partes (distintas celdas) y se pueden agregar comentarios usando 
    el código markdown, lo cual permite introducir fórmulas matemáticas de forma similar a LaTeX.
    
   Para Julia tenemos al menos 3 posibilidades: 
        
   a) `Ijulia`, (**recomendado**) es un notebook similar a Jupyter, pero nativo de Julia. Las instrucciones para su instalació
        instalación las pueden encontrar [aquí:](https://github.com/JuliaLang/IJulia.jl). Alternativamente, lea más abajo.
        
        
   b) `Jupyter`, es muy similar al anterior, pero su instalación es un poquito más compleja. **No lo recomendamos** como primera instalación. Tiene la ventaja que allí se pueden correr códigos en Python. Si ya lo tiene instalado entonces puede usar este directamente de acuerdo a lo que indican [aquí](https://datatofish.com/add-julia-to-jupyter/) (para Windows). Para Linux usar **anaconda** (ver [aquí](https://anaconda.org/)).
        
   c) `Pluto`, es un nuevo tipo de notebook que es muy intersante y tiene varias ventajas sobre los otros. Pero estas ventajas también lo hacen complicado para personas con poca experiencia en la escritura de códigos. Por lo tanto **No lo recomendamos**. 
   De todos modos, las instrucciones para instalarlos están [aquí](https://github.com/fonsp/Pluto.jl)
   
 ## Instalando IJulia
 
 Para ello debe instalar el *paquete* con el código necesario. Para ello, inicue unaa consola de Julia e ingrese las siguientes instrucciones
 
    julia> using Pkg
    julia> Pkg.add("IJulia")

 Veremos una larga lista de mensajes que Julia irá emitiendo a medida que se instalan las componentes necesarias.
 A continuación activaremos la notebook.

    using IJulia
    notebook()
    
La primera vez que ejecute este comando tomará un tiempo apreciable hasta que se complete el cargado del sofware y se compile el código. En particular, la primera vez le preguntará si desea instalar **Jupyter**, si no lo tiene ya instalado acceda a ello. En tal caso instalará otro paquete, llamado `Conda.jl`. 
Una vez completado el proceso le debería aparecer una página en su browser donde podrá comenzar a trabajar con su notebook.
Cada vez que desee inciar IJulia para crear o editar notebooks, deberá ingresar los dos últimos comandos antes mencionados en una cónsola de Julia.
