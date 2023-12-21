<template>
    <div class="full">
        <div class="app w-full px-20 pt-4 flex flex-row justify-between">
            <div class="left_col_main">
                <div class="cont1_left ">
                    <nav class="navbar max-w-4xl ">
                        <div class="nav_top_deco w-full bg-black h-1 "></div>
                        <ul class="nav_bottom flex flex-row w-full justify-between">
                            <div class="li">Modular</div>
                            <div class="li">Serif</div>
                            <div class="li">Variable</div>
                            <div class="li">Versatile</div>

                        </ul>
                    </nav>
                </div>
                <div class="font_showcase">
                    <div class="display_text_container relative h-fit flex justify-center text-9xl py-20 whitespace-nowrap">
                        <div class="text1_container text-[14rem] leading-[7.8rem] w-full top-0 right-80 mx-auto"
                            :style="textStyles('PIXER-MODULAR-VF', slider1Value, slider2Value)">Junicode</div>
                    </div>
                    <div class="sliders_container flex flex-col gap-8">
                        <div class="slider_1 w-60">
                            <div class="slider_title w-full">Square</div>
                            <div class="slider_1_container">
                                <input type="range" min="0" max="100" class="slider" id="slider1" v-model="slider1Value">
                            </div>
                            <div class="slider_info flex flex-row justify-between jus">
                                <div class="slider_unit1">0</div>
                                <div class="slider_unit2">100</div>

                            </div>
                        </div>

                        <div class="slider_2 w-60">
                            <div class="slider_title">Deviation (+-)</div>
                            <div class="slider_2_container">
                                <input type="range" min="-100" max="100" class="slider" id="slider2" v-model="slider2Value">
                            </div>
                            <div class="slider_info flex flex-row justify-between">
                                <div class="slider_unit1">-100</div>
                                <div class="slider_unit2">0</div>
                                <div class="slider_unit3">100</div>


                            </div>
                        </div>
                    </div>

                </div>
            </div>
            <div class="right_col_main">






                <div class="expl_box mt-24">
                    <div class="w-[67ch] min-h-[12rem]">Este proyecto no nace con el fin de componer una tipografía a base de módulos sino con la idea de descomponer cualquier tipografía en pequeñas secciones de igual forma y tamaño para después reconfortar la tipografía inicial con la capacidad de ser variable tratando de forma individual cada uno de los módulos obtenidos en la división. Mi intención proponiendo este proyecto no es el de construir una tipografía desde cero o derivada de una existente, es generar un software capaz de dado un archivo de fuente estandarizado (ttf, otf…) hacer uso de sus formas como contornos a rellenar o dividir y obtener entonces la versión modular de la tipografía inicial con la capacidad de presentar todos los ejes de variación que se desee partiendo de los módulos en los que dividirla. 


Una idea fija desde una fase bastante inicial del proyecto es la de hacer un esfuerzo en la cantidad de módulos que conforman cada uno de los glifos con la intención de obtener una tipografía variable que en un estado inicial o basal sea lo más parecido posible a la tipografía base. 

La que considero hipótesis principal de este proyecto es si un trabajo tan abierto como si se tratase de un filtro por el que pasar un archivo de fuente puede abrir un nuevo plano de evolución o experimentación haciendo uso de las tipografías ya creadas desde scripts o monoespaciadas a sistemas de iconos. 


Es posible que el hecho de partir de tipografías existentes pueda llevar a un posible conflicto con el sistema de registro y derechos de autoría de la tipografía, más aún en el momento concreto de cambio de paradigma en el que se encuentra la situación con la implementación de distintos sistemas de pago (mensualidades, alquileres…). En un inicio el proyecto es open-source y hace uso de una tipografía de estas características. 

Una limitación más técnica es que no tengo la certeza de que el proceso que requiere cualquier uso (más aún la variación) de una fuente con la cantidad de nodos que supone construir de esta manera sea eficiente con la tecnología a la que tenemos acceso y principalmente que está implementada en la web actualmente. 

A la hora de desarrollar esta idea me encuentro la programación como gran barrera limitante. Aunque encuentro muy interesante toda la parte técnica que se propone en el desarrollo después de algo de investigación centrada en lenguajes de programación y trabajos similares considero que se aleja bastante del nivel al que pueda llegar en el periodo de desarrollo para el proyecto. Sin embargo como punto de partida a un proyecto orientado en estos términos propongo realizar de forma relativamente manual la composición de una tipografía basándome en otra existente con los mismos conceptos de la idea inicial, sirviendo así como un primer acercamiento a esta composición modular y un campo de pruebas. 
Me resulta interesante de la misma manera por la versatilidad que suponía en un primer momento el hecho de darle la vuelta al ejercicio y proponer un trabajo de manera más global en el campo de la tipografía, sin rechazar la experimentación. Otro factor ligeramente influyente en la elección de mantener esta vía de desarrollo es la observación de la tendencia actual en el mundo de la imagen compuesta, más concretamente en la tipología de imágenes que se trabajan desde el diseño gráfico. La composición modular o particular es una tendencia al alza actualmente en parte debido al revival de los orígenes del medio web que se observa desde algunos años atrás. 


Desde la implementación de la retícula moderna como herramienta en el diseño que nace con el siglo XX se desarrolla el diseño modular tanto en lo gráfico como en las distintas disciplinas del diseño, arquitectura y mobiliario son muy buenos ejemplos. 
Este proyecto está muy influenciado por un trabajo experimental e inacabado de  la diseñadora gráfica y programadora Lorraine Li nombrado Font-remix, una descripción del proyecto es; un experimento basado en la web que propone el proceso de configurar las formas de las letras en tiempo real y generar un archivo de fuente personalizado para su descarga. Utilizando opentype.js y realizando operaciones booleanas en las formas vectoriales de las letras, se combinan dos tipografías de código abierto según un conjunto de rejillas predefinidas. Considero muy interesante y con posibilidades de uso fuera también del ámbito experimental la reutilización de tipografías diseñadas. Tras investigar sobre él paso a realizar una serie de pruebas con la librería que menciona la autora de la que hace uso en su trabajo. OpenType.js es una biblioteca JavaScript que permite trabajar con fuentes tipográficas OpenType en el navegador web. Permite cargar, manipular y renderizar fuentes OpenType, lo que brinda flexibilidad para realizar operaciones específicas con las letras, como cambiar su forma, tamaño o aplicar efectos. Se trata de una herramienta muy potente que permite acceder con javascript al trazo y a puntos concretos de cada glifo y funciona principalmente mediante la etiqueta canvas renderizando por tanto no trabaja el archivo de la fuente en sí o de la manera que es interesante para el proyecto inicial.

Otra referencia que encuentro muy interesante es el trabajo de la diseñadora Lena Weber, que también hace mucho uso de la programación y comparte con el ejemplo anterior proyectos orientados a ser herramientas. Ambas trabajan la idea de aportar una herramienta de software que permite al usuario intervenir y obtener un resultado a su medida.


La primera tarea en este procesamiento de la tipografía es la elección de una base,creo más interesante comenzar con una tipografía con serifas por su construcción de dibujo más complejo y observar así cómo se comportará reaccionando a la variación propuesta. Junicode se trata de un proyecto de código abierto de reconstrucción de la tipografía a partir del ejemplar escaneado de Linguarum vett. septentrionalium thesaurus grammatico-criticus et archaeologicus (Oxford, 1703–5) de George Hickes. Esta publicación sigue la tradición del momento compuesta por distintas familias tipográficas en función de la lengua. El nacimiento de esta tipografía digitalizada cuenta con la ayuda de La Iniciativa de Fuente Medieval Unicode (Medieval Unicode Font Initiative), un grupo de trabajo sin fines de lucro compuesto por académicos y diseñadores de fuentes que desean encontrar una solución común a un problema experimentado por muchos estudiosos medievales: la codificación y visualización de caracteres especiales en textos medievales escritos en el alfabeto latino.

Haciendo uso de las herramientas que ofrece Fontlab y para poder compatibilizar el proyecto, una vez definidos los objetivos dentro de la primera entrega comienzo con la construcción de la tipografía de forma manual tras definir el tamaño del módulo creado en la galería de elementos. Esta parte del proceso es la que más tiempo toma hasta el momento, es muy repetitiva pero principalmente es debido al desconocimiento del programa y la condición de trabajo (tamaño y número de módulos, al cometer errores en fases previas las soluciones suponen un repaso módulo por módulo). Una vez construida la tipografía sobre la base se pasa a trabajar la variabilidad desde el módulo haciendo uso de las funciones de referenciación de fontlab por las cuales en un mismo máster la variación de un módulo cuyas copias sí se encuentran referenciadas se trasladará a todas ellas. Hasta el momento están funcionando el eje que define si el módulo es cuadrado o presenta esquinas redondeadas bajando el tono tipográfico y la mancha de texto, y un eje llamado Deviation que responde a valores de -100 a 100 con el que el módulo se estira en el eje x. Hasta el momento la fuente presenta problemas en la exportación de caracteres concretos y se ve afectado el uso por su peso y la falta de optimización causando procesos con esperas mayores a las deseadas en tipografía variable.

Al tratarse la construcción de un proceso muy mecánico y altamente repetitivo los errores con los que me he encontrado a más avanzado el proyecto suponían más tiempo para corregir, esto sumado a que se trata del primer contacto con el software (Fontlab) ha sido la causa principal de retrasos en las fechas y la falta de tiempo para un desarrollo mayor en la primera entrega del proyecto. Una vez construida de forma modular paso a desarrollar las variaciones sencillas y vistosas a tamaños medios y grandes.

Sobre el resultado considero que sin todavía tener un acabado que cumpla los estándares de uso que tenía en mente para este proyecto y sin tener en cuenta limitaciones técnicas (falta de potencia y memoria en equipos y conocimientos básicos en programación) la tipografía resultante y la forma de trabajo que permite la construcción sí prueba el punto inicial del proyecto, de obtener una fuente con un estilo muy parecido pero aportando variabilidad de una forma relativamente sencilla dada la sencillez del módulo que es donde se diseñan las variaciones (masters).
Gráficamente lo considero interesante y coherente con el origen de la idea, demuestra que una variación simple con esta manera de construir pasa a ser rápidamente muy distinta con poco cambio. La reducción en tamaño del módulo da un resultado tipográfico con un tono menos intenso, algo explorable para conseguir un eje de variación que permita trabajar con la mancha tipográfica en conjunto. 


En el corto plazo los avances más próximos e interesantes son dos, el uso de un módulo de mayor tamaño y la búsqueda de una tipografía de distintas características a la de base para procesar de la misma manera. El uso de un módulo de mayor tamaño supone una pérdida de definición, algo que choca con un objetivo inicial pero supone una reactividad mucho más notable en la variación que se desarrolla. Al tener la unidad mínima variable mayor tamaño las modificaciones en esta serán mucho más visibles, probablemente sin perder las formas originales puesto que el trabajo realizado hasta el momento ha partido de un módulo de unas dimensiones muy reducidas. 
Otra línea de desarrollo muy interesante es una vez conocido algo mejor el programa la experimentación y el juego con las variantes de los módulos. Este proyecto tiene sentido desde la propuesta por lo abierto a la mejora que se propone en esta vía. Para mayor juego con los módulos sería muy interesante optimizar y estudiar la manera de reducir el peso del archivo de fuente. 
Como futura línea y más interesante pongo la idea de la que nace el proyecto, una vez testado con estas fuentes prototipo el sentido y la viabilidad del proyecto lo más interesante desde mi punto de vista es la investigación para llevar la idea a un software versátil del que obtener un sinfín de fuentes modificadas y variables. 
</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "YourComponentName",
    data() {
        return {
            slider1Value: 100,
            slider2Value: 0,
        };
    },
    watch: {
        slider1Value: function (newValue) {
            this.updateSliderBackground(newValue, "slider1");
            this.updateTextStyles();
        },
        slider2Value: function (newValue) {
            this.updateSliderBackground(newValue, "slider2");
            this.updateTextStyles();
        },
    },
    methods: {
        updateSliderBackground(value, sliderId) {
            const slider = document.getElementById(sliderId);
            const percentage = ((value - slider.min) / (slider.max - slider.min)) * 100;
            slider.style.background = `linear-gradient(to right, #d9d9d9 ${percentage}%, #fff ${percentage}%)`;
        },
        textStyles(fontFamily, fontWeight, DEVI) {
            return {
                fontFamily: fontFamily,
                fontWeight: fontWeight,
                fontVariationSettings: `"SQUA" ${fontWeight}, "DEVI" ${DEVI}`,
            };
        },

        updateTextStyles() {
            this.textStyles1 = this.textStyles('PIXER-MODULAR-VF', this.slider1Value, this.slider2Value, 'SQUA');
            this.textStyles2 = this.textStyles('PIXER-MODULAR-2-VF', this.slider3Value, this.slider4Value, 'DEVI');
        }


    },
};
</script>

<style lang="sass" scoped>
/* Estilos específicos del componente, si es necesario */
@font-face
  font-family: "PIXER-MODULAR-VF"
  src: url("/assets/fonts/junicode_prueba_xport1.otf") format("opentype")

.slider
  font-family: "PIXER-VARIABLE-VF"
  appearance: none
  height: 8px
  width: 100% 
  outline: solid 1px
  margin: 10px 0
  border: none
  border-radius: 2px

  &::-webkit-slider-thumb
    -webkit-appearance: none
    appearance: none
    width: 20px
    height: 20px
    border-radius: 0

  &::-moz-range-thumb
    width: 40px
    height: 40px
    background: black
    cursor: pointer
    border-radius: 0


.slider_title
    font-weight: bold
    font-size: 2rem
.text1_container
  font-family: "PIXER-MODULAR-VF"

.expl_box
  padding: .8rem
  font-size: .8rem
  border: 1px solid #ccc 
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1)
  border-radius: 8px
  width: 100%
  height: 400px
  overflow-y: scroll
  overflow-x: hidden


</style>