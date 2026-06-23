# Proyecto de vibraciones mecánicas - Presentación de resultados para Dinámica

> Conversión de PDF a Markdown para uso como contexto en Claude. Se conserva el contenido textual, títulos, tablas y leyendas de figuras en la medida en que fueron extraídos del PDF. Las figuras se mantienen como leyendas/descripciones textuales, no como imágenes incrustadas.

**Fuente:** `Presentación de resultados para Dinámica.pdf`  

**Curso:** IC-0502, Dinámica  

**Universidad:** Universidad de Costa Rica, Escuela de Ingeniería Civil  

**Año indicado en portada:** 2026

---


<!-- Página 1 -->

Universidad de Costa Rica

Facultad de Ingeniería

Escuela de Ingeniería Civil

IC-0502, Dinámica

Proyecto de vibraciones mecánicas

Presenta:

Adrián Castro Ramírez C21930

Daniel Josué Quirós Ampiée C26160

Leonardo Castillo Céspedes C11760

Natalia Campos Umaña C11594

Oscar Durán Venegas C12618

Profesor:

DPhil. Ing. Guillermo Santana

Ciudad Universitaria Rodrigo Facio

Costa Rica

Julio, 2026


<!-- Página 2 -->

RESUMEN

TABLA DE CONTENIDOS

PORTADA .................................................................................. ¡Error! Marcador no definido.

RESUMEN ................................................................................................................................ 2

TABLA DE CONTENIDOS .......................................................................................................... 2

LISTA DE FIGURAS ................................................................................................................... 3

LISTA DE TABLAS...................................................................................................................... 3

LISTA DE SÍMBOLOS Y NOMENCLATURA ................................................................................. 3

INTRODUCCIÓN ...................................................................................................................... 4

MARCO TEÓRICO .................................................................................................................... 6

Sistemas de un grado de libertad ....................................................................................... 6

Sistemas de múltiples grados de libertad ........................................................................... 7

Vibración libre y amortiguamiento ..................................................................................... 8

Vibración forzada y resonancia ........................................................................................... 9

Método del decremento logarítmico ............................................................................... 10

Integral de Duhamel ......................................................................................................... 12

Modelos de edificios como sistemas discretos ................................................................ 13

DESCRIPCIÓN DEL MODELO FÍSICO ...................................................................................... 15

Descripción general de los edificios ................................................................................. 15

Especificaciones geométricas ........................................................................................... 16

Materiales y propiedades mecánicas ............................................................................... 19

Sistema de masas ............................................................................................................. 20

METODOLOGÍA EXPERIMENTAL ........................................................................................... 22

Prueba de vibración libre .................................................................................................. 22

Identificación de frecuencias naturales ............................................................................ 23

Identificación del amortiguamiento ................................................................................. 24

Prueba de vibración forzada ............................................................................................. 25

Prueba sísmica en mesa vibratoria ................................................................................... 26


<!-- Página 3 -->

MODELO MATEMÁTICO ........................................................................................................ 26

Ecuaciones de movimiento ............................................................................................... 26

Determinación de parámetros dinámicos ........................................................................ 28

Calibración del modelo ..................................................................................................... 29

SIMULACIÓN NUMÉRICA ...................................................................................................... 30

Método de la Integral de Duhamel................................................................................... 30

Registros sísmicos utilizados ............................................................................................. 30

Resultados de la simulación ............................................................................................. 30

RESULTADOS EXPERIMENTALES ............................................................................................ 30

COMPARACIÓN Y ANÁLISIS DE RESULTADOS ........................................................................ 73

CONCLUSIONES Y RECOMENDACIONES ............................................................................... 73

REFERENCIAS BIBLIOGRÁFICAS............................................................................................. 75

APÉNDICES ............................................................................................................................ 76

LISTA DE FIGURAS

(Contenido pendiente)

LISTA DE TABLAS


**Tabla 1. Resumen de simbología empleada en el documento ............................................... 2**


**Tabla 2. Especificaciones geométricas comparativas de los dos modelos de edificio ......... 15**


**Tabla 3. Distribución del sistema de masas en los dos modelos .......................................... 17**

LISTA DE SÍMBOLOS Y NOMENCLATURA

La siguiente tabla recoge los símbolos empleados en el presente informe, organizados en

letras latinas y, a continuación, letras griegas. Las unidades indicadas corresponden al

Sistema Internacional, salvo indicación en contrario.


**Tabla 1. Resumen de simbología empleada en el documento.**

Símbolo

Descripción y unidades

> Comentado [ACR1]: Lo voy a colocar hasta el final porque

no sé cómo hacerlo automático


<!-- Página 4 -->

𝐴

Área de la sección transversal de una

columna [m²]

𝑐

Coeficiente de amortiguamiento viscoso

[N·s/m]

[𝐶]

Matriz de amortiguamiento del sistema de

múltiples GDL [N·s/m]

𝐷𝐴𝐹

Factor de amplificación dinámica (Dynamic

Amplification Factor) [adimensional]

𝐸

Módulo de elasticidad del material de las

columnas [Pa]

𝑓

Frecuencia natural cíclica del sistema [Hz]

𝐹(𝑡)

Fuerza externa aplicada al sistema en

función del tiempo [N]

ℎ

Altura de piso o entrepiso [m]

𝐼

Momento de inercia de la sección

transversal de la columna [m⁴]

𝑘

Rigidez del resorte o rigidez lateral del

entrepiso [N/m]

[𝐾]

Matriz de rigidez del sistema de múltiples

GDL [N/m]

𝐿

Longitud o altura libre de la columna [m]

𝑚

Masa concentrada del sistema [kg]

[𝑀]

Matriz de masa del sistema de múltiples

GDL [kg]

𝑇

Periodo natural de vibración del sistema [s]

𝑥

Desplazamiento del grado de libertad [m]

ẋ

Velocidad del grado de libertad [m/s]

ẍ

Aceleración del grado de libertad [m/s²]

𝛿

Decremento logarítmico [adimensional]

𝜉

Razón de amortiguamiento respecto al

crítico [adimensional]

𝜔ₙ

Frecuencia natural circular no amortiguada

[rad/s]

𝜔𝑑

Frecuencia natural circular amortiguada

[rad/s]


# Introducción

El estudio del comportamiento dinámico de las estructuras constituye uno de los pilares

fundamentales de la ingeniería sísmica moderna. A diferencia de las cargas estáticas, las

solicitaciones de origen sísmico son de naturaleza transitoria y dependen del tiempo, por lo


<!-- Página 5 -->

que su efecto sobre una edificación no puede comprenderse únicamente a partir de la

magnitud de las fuerzas aplicadas, sino que requiere caracterizar las propiedades dinámicas

del sistema, su masa, su rigidez y su amortiguamiento. Estas propiedades determinan las

frecuencias naturales de vibración y los modos en que la estructura responde ante el

movimiento del terreno, de manera que el diseño sismorresistente busca evitar que dichas

frecuencias coincidan con el contenido frecuencial dominante de los sismos esperados,

fenómeno conocido como resonancia [1], [2]. En regiones de elevada amenaza sísmica,

como Costa Rica y el resto de Centroamérica, el análisis dinámico estructural deja de ser un

ejercicio académico para convertirse en una herramienta indispensable de protección de la

vida y la inversión [2], [3].

Dada la dificultad y el costo de ensayar estructuras a escala real, el empleo de modelos

físicos reducidos representa una estrategia ampliamente aceptada para la caracterización

experimental del comportamiento dinámico. Un modelo a escala, ensayado sobre una mesa

vibratoria, permite reproducir de forma controlada los mecanismos esenciales de la

respuesta estructural —vibración libre, vibración forzada, amortiguamiento y resonancia—

y contrastar las predicciones analíticas con mediciones reales. Aunque la similitud dinámica

completa exige respetar relaciones de escalamiento entre masa, rigidez y aceleración, los

modelos didácticos resultan especialmente valiosos para evidenciar de manera tangible los

conceptos que las ecuaciones de movimiento describen en abstracto, y para desarrollar

destrezas de instrumentación, medición e identificación de parámetros dinámicos [3].

El presente proyecto aborda el estudio experimental y numérico de dos edificios en

miniatura construidos en madera de balsa, cada uno con dos pisos y, por lo tanto, dos grados

de libertad traslacionales. Ambos modelos comparten una tabla base común que se monta

sobre una mesa vibratoria, lo que permite someterlos a las mismas excitaciones. Los

edificios fueron concebidos deliberadamente con geometrías contrastantes: uno alto y

esbelto, con una altura total de 80 a 100 cm, y otro bajo y chato, con entrepisos de 15 a 20

cm. Las columnas se ejecutan con secciones máximas de 6 mm × 6 mm en madera balsa, y

en cada nivel se incorporan masas concentradas de 0,5 kg, para un total aproximado de 2 a

3 kg por edificio. Esta diferencia de esbeltez induce rigideces laterales y, en consecuencia,

frecuencias naturales notoriamente distintas entre ambos modelos, lo que permite

observar comportamientos dinámicos diferenciados ante una misma solicitación sísmica.

El objetivo general del proyecto es determinar experimentalmente la ecuación de

movimiento dinámica amortiguada de cada uno de los dos edificios de madera balsa y

simular su respuesta ante registros sísmicos mediante la Integral de Duhamel,

contrastando los resultados analíticos con los obtenidos en el laboratorio. Para alcanzar

este propósito se plantean los siguientes objetivos específicos:


<!-- Página 6 -->

- Construir dos modelos físicos de edificios de dos grados de libertad en madera balsa,

con geometrías contrastantes en cuanto a esbeltez.

- Caracterizar la respuesta en vibración libre de cada modelo para identificar sus

frecuencias naturales y su razón de amortiguamiento mediante el método del

decremento logarítmico.

- Evaluar la respuesta en vibración forzada y localizar las condiciones de resonancia de

cada estructura.

- Formular el modelo matemático del sistema y calibrar sus parámetros dinámicos de

masa, rigidez y amortiguamiento a partir de las mediciones experimentales.

- Simular numéricamente la respuesta sísmica de los modelos empleando la Integral

de Duhamel sobre registros sísmicos representativos.

- Realizar pruebas sísmicas en mesa vibratoria y comparar los resultados

experimentales con las predicciones analíticas y numéricas.

El alcance de este estudio se reduce al análisis lineal de dos sistemas de dos grados de

libertad bajo excitación en una sola dirección horizontal, considerando comportamiento

elástico de los materiales y amortiguamiento de tipo viscoso, añadiendo también un

arriostramiento en sentido perpendicular al eje de movimiento. No se contempla el

comportamiento no lineal, la fluencia o el daño de los elementos, ni efectos de torsión,

interacción suelo-estructura, fatiga del material o componentes verticales del movimiento.

Las masas se idealizan como concentradas en cada nivel y las columnas como elementos de

rigidez lateral, despreciando la masa propia de la madera balsa frente a las masas añadidas.

La fidelidad de la representación está condicionada por las tolerancias de construcción

artesanal de los modelos, la precisión de la instrumentación disponible y las limitaciones de

la mesa vibratoria empleada.


# Marco Teórico


## Sistemas de un grado de libertad

El sistema de un grado de libertad (GDL a partir de ahora) constituye la unidad básica del

análisis dinámico estructural y permite introducir los conceptos fundamentales que se

generalizan posteriormente a sistemas más complejos. El modelo idealizado consiste en una

masa concentrada m, conectada a un soporte rígido mediante un resorte lineal de rigidez k

y un amortiguador viscoso de coeficiente c, restringida a desplazarse según una única

coordenada x(t) [1]. Cuando sobre la masa actúa una fuerza externa F(t), el equilibrio

dinámico instantáneo, expresado a través de la segunda ley de Newton, establece que la

> Comentado [ACR2]: Acá podemos considerar eliminar

alguna para no tener un análisis tan extenso


<!-- Página 7 -->

suma de las fuerzas de inercia, amortiguamiento y elástica iguala a la fuerza aplicada, dando

lugar a la ecuación diferencial ordinaria de segundo orden:

𝑚· 𝑥̈(𝑡) + 𝑐· 𝑥̇(𝑡) + 𝑘· 𝑥(𝑡) = 𝐹(𝑡)

(1)

Esta ecuación describe el balance instantáneo de cuatro contribuciones: la fuerza inercial

proporcional a la aceleración ẍ, la fuerza disipativa proporcional a la velocidad ẋ, la fuerza

restauradora proporcional al desplazamiento x, y la excitación externa F(t). La frecuencia

natural circular del sistema no amortiguado, que representa la rapidez con la que la masa

oscilaría en ausencia de disipación, se define como [4]:

𝜔𝑛 = √

𝑘

𝑚

(2)

La frecuencia natural cíclica fₙ = ωₙ/(2π) tiene unidades de hertz y constituye una propiedad

intrínseca del sistema, independiente de la excitación. El amortiguamiento se cuantifica

mediante el coeficiente crítico c_cr = 2mωₙ, valor para el cual el sistema retorna al equilibrio

sin oscilar, y se adimensionaliza definiendo la razón de amortiguamiento ξ como el cociente

entre el amortiguamiento real y el crítico [1]:

𝜉 =

𝑐

𝑐𝑐𝑟 =

𝑐

2·𝑚·𝜔𝑛

(3)

En la práctica, los valores típicos de ξ para estructuras civiles oscilan entre 0,02 y 0,10,

dependiendo del material y del nivel de daño esperado [5]. Dividiendo la ecuación (1) entre

m y empleando las definiciones anteriores, se obtiene la forma canónica adimensional ẍ +

2ξωₙẋ + ωₙ²x = F(t)/m, que será la base para el posterior análisis de vibración libre y forzada

en las secciones siguientes.


## Sistemas de múltiples grados de libertad

Las estructuras reales presentan generalmente más de un grado de libertad, ya que su masa

se distribuye espacialmente y, al deformarse, lo hace mediante varios modos

independientes. Para una estructura con n grados de libertad, las ecuaciones de movimiento

adoptan la forma matricial [1], [5]:

[𝑀] · 𝑥̈(𝑡) + [𝐶] · 𝑥̇(𝑡) + [𝐾] · 𝑥(𝑡) = 𝐹(𝑡) (4)

donde x(t) es el vector de desplazamientos de orden n × 1, F(t) es el vector de fuerzas

externas y [M], [C], [K] son las matrices de masa, amortiguamiento y rigidez, todas de

dimensión n × n. Esta formulación constituye una generalización directa del caso de 1 GDL

y conserva la estructura física del balance entre inercia, disipación, restauración elástica y

excitación. Las matrices [M] y [K] son normalmente simétricas y positivas definidas, mientras


<!-- Página 8 -->

que [C] suele construirse como una combinación lineal de [M] y [K] (amortiguamiento de

Rayleigh) [5].

Para un edificio de dos pisos modelado como un sistema de corte (shear building1) con masa

concentrada en cada nivel y columnas axialmente rígidas, la matriz de masa resulta diagonal,

pues cada masa se asocia a un único grado de libertad traslacional horizontal:

[𝑀] = [𝑚1

0

0

𝑚2]

(5)

donde m₁ y m₂ son las masas concentradas del primer y segundo piso, respectivamente. La

matriz de rigidez, obtenida ensamblando las contribuciones de las columnas que conectan

cada nivel con el adyacente, adopta la forma tridiagonal característica del edificio de corte:

[𝐾] = [𝑘1 + 𝑘2

−𝑘2

−𝑘2

𝑘2 ]

(6)

donde k₁ es la rigidez lateral combinada de las columnas del primer entrepiso (entre la base

y el primer piso) y k₂ es la rigidez lateral combinada de las columnas del segundo entrepiso

(entre el primer y segundo piso). El acoplamiento extradiagonal −k₂ refleja físicamente que

las columnas del segundo entrepiso conectan los dos grados de libertad, transmitiendo

fuerza de uno a otro cuando se produce un desplazamiento relativo [5], [6]. El sistema

resultante de dos ecuaciones diferenciales acopladas constituye el punto de partida del

análisis modal y de la simulación dinámica del presente trabajo.


## Vibración libre y amortiguamiento

La vibración libre corresponde al movimiento que experimenta un sistema dinámico cuando

se le retira la excitación externa después de haber sido perturbado de su posición de

equilibrio. Imponiendo F(t) = 0 en la ecuación (1) y empleando la forma canónica

adimensional introducida al final de la sección 8.1, se obtiene la ecuación homogénea:

𝑥̈ + 2 · 𝜉· 𝜔𝑛· 𝑥̇ + 𝜔𝑛

2 · 𝑥 = 0 (7)

Esta es una ecuación diferencial lineal de coeficientes constantes cuya solución general

depende de las raíces de su ecuación característica 𝑠2 + 2𝜉𝜔ₙ𝑠+ 𝜔ₙ2 = 0, dadas por 𝑠=

−𝜉𝜔ₙ ± 𝜔ₙ√(𝜉2 −1). El signo del discriminante (𝜉2 −1) determina tres regímenes

1 Un shear building es un modelo simplificado de edificio en el cual la respuesta dinámica

lateral se representa mediante desplazamientos horizontales concentrados en cada nivel.

Este modelo supone losas rígidas, masas concentradas en los pisos y rigidez lateral aportada

principalmente por las columnas, despreciando las deformaciones axiales y rotacionales de

los elementos


<!-- Página 9 -->

cualitativamente distintos del comportamiento dinámico [6], [4]: el caso sobreamortiguado

(𝜉> 1), en el cual las raíces son reales y distintas y la masa retorna asintóticamente al

equilibrio sin oscilar; el caso críticamente amortiguado (𝜉= 1), con una raíz real doble que

constituye la frontera entre el comportamiento oscilatorio y no oscilatorio, regresando al

equilibrio en el menor tiempo posible; y el caso subamortiguado (𝜉< 1), con raíces

complejas, en el cual la respuesta es oscilatoria con amplitud decreciente

exponencialmente.

El caso subamortiguado es el de interés práctico para las estructuras civiles, ya que sus

razones de amortiguamiento son usualmente muy inferiores a la unidad. Para 𝜉 < 1, la

solución general puede escribirse como:

𝑥(𝑡) = 𝑒−𝜉·𝜔𝑛·𝑡· [𝐴· 𝑐𝑜𝑠(𝜔𝑑· 𝑡) + 𝐵· 𝑠𝑖𝑛(𝜔𝑑· 𝑡)]

(8)

donde A y B son constantes determinadas por las condiciones iniciales de desplazamiento

𝑥(0) y velocidad ẋ(0), y 𝜔𝑑 es la frecuencia natural amortiguada, ligeramente inferior a 𝜔ₙ

debido a la presencia de disipación:

𝜔𝑑 = 𝜔𝑛· √1 − 𝜉2 (9)

El factor exponencial 𝑒(−𝜉𝜔ₙ𝑡) actúa como una envolvente que reduce progresivamente la

amplitud de las oscilaciones armónicas, mientras que la frecuencia𝜔𝑑 gobierna el periodo

aparente del movimiento. Para valores pequeños de ξ —como los esperables en los modelos

de balsa del presente proyecto—, 𝜔𝑑 ≈ ωₙ y la diferencia entre ambas frecuencias es

despreciable a efectos prácticos [1]. El periodo amortiguado correspondiente es 𝑇𝑑=

2𝜋/𝜔𝑑, y su medición directa a partir del registro temporal de la vibración libre constituye

uno de los procedimientos experimentales más simples para estimar la frecuencia natural

del sistema.


## Vibración forzada y resonancia

Cuando un sistema dinámico es sometido a una excitación armónica de la forma 𝐹(𝑡) =

𝐹0 · 𝑠𝑖𝑛(𝜔· 𝑡), siendo 𝐹0 la amplitud de la fuerza y ω su frecuencia circular, la respuesta se

compone de un transitorio que decae exponencialmente —asociado a la solución

homogénea analizada en la sección anterior— y una respuesta en estado estacionario que

persiste mientras la excitación esté presente. Tras la disipación del transitorio, la masa oscila

con la misma frecuencia que la excitación, pero con un desfase 𝜑 y una amplitud 𝑥 que

dependen de la relación entre ω y la frecuencia natural ωₙ [1], [5]:

𝑥(𝑡) = 𝑋· 𝑠𝑖𝑛(𝜔· 𝑡−𝜑)

(10)


<!-- Página 10 -->

La amplitud de la respuesta en estado estacionario, normalizada respecto al desplazamiento

estático que produciría una fuerza F₀ aplicada estáticamente (𝑥𝑠𝑡= 𝐹0/𝑘), define el factor

de amplificación dinámica (DAF, Dynamic Amplification Factor2), que cuantifica cuántas

veces es mayor la respuesta dinámica que la estática:

𝐷𝐴𝐹 =

𝑋

𝑥𝑠𝑡 =

1

√(1−𝑟2)2 + (2·𝜉·𝑟)2

(11)

donde 𝑟 = 𝜔/𝜔ₙ es el cociente de frecuencias entre la excitación y la natural del sistema.

El ángulo de desfase entre fuerza y desplazamiento queda dado por 𝜑= 𝑎𝑟𝑐𝑡𝑎𝑛[2𝜉𝑟/(1 −

𝑟2)]. La representación gráfica del DAF en función de r constituye la curva de respuesta en

frecuencia (a partir de ahora FRF), una herramienta esencial para caracterizar

experimentalmente el comportamiento dinámico de la estructura [7], [4].

La condición de resonancia ocurre cuando la frecuencia de excitación se aproxima a la

frecuencia natural del sistema (𝑟→1). En esta situación, el denominador de la ecuación

(11) se reduce a 2𝜉, de modo que el DAF alcanza su valor máximo aproximado:

𝐷𝐴𝐹𝑚á𝑥 ≈

1

2·𝜉

(12)

Para razones de amortiguamiento típicas de estructuras civiles (ξ entre 0,02 y 0,05), el DAF

en resonancia puede alcanzar valores entre 10 y 25, lo que implica amplitudes de respuesta

una a dos órdenes de magnitud superiores a la respuesta estática equivalente. Este

fenómeno reviste especial importancia en ingeniería sísmica porque los registros sísmicos

contienen energía distribuida en un amplio rango de frecuencias, y la probabilidad de que

el contenido frecuencial dominante del sismo se aproxime a alguna de las frecuencias

naturales de la estructura es significativa [1], [2]. El diseño sismorresistente busca

precisamente alejar las frecuencias naturales de la estructura del contenido espectral del

sismo de diseño, o bien incrementar el amortiguamiento mediante dispositivos disipadores,

con el fin de limitar la amplificación dinámica.


## Método del decremento logarítmico

El método del decremento logarítmico es una técnica clásica y robusta para la identificación

experimental de la razón de amortiguamiento 𝜉 a partir del registro temporal de la respuesta

en vibración libre subamortiguada de un sistema [1], [6]. Su fundamento se apoya en la

propiedad observable de que, en un movimiento oscilatorio amortiguado, los picos

sucesivos de desplazamiento decrecen siguiendo una progresión geométrica gobernada

exclusivamente por el factor exponencial 𝑒(−𝜉𝜔ₙ𝑡). Esto significa que el cociente entre dos

2 El DAF (Dynamic Amplification Factor) es un coeficiente que compara la respuesta máxima de una estructura

ante una carga dinámica con la respuesta que tendría ante una carga estática equivalente.


<!-- Página 11 -->

picos consecutivos separados un periodo amortiguado 𝑇𝑑 depende únicamente de las

propiedades dinámicas del sistema, y no de las condiciones iniciales con que se generó la

perturbación.

Si se denota por 𝑥ᵢ la amplitud del i-ésimo pico positivo del registro y por 𝑥ᵢ+1 la del pico

inmediatamente posterior, el decremento logarítmico 𝛿 se define como el logaritmo natural

del cociente entre ambas amplitudes y, mediante la solución (8), puede expresarse en

función de 𝜉:

𝛿= 𝑙𝑛(

𝑥𝑖

𝑥𝑖+1) =

2𝜋·𝜉

√1 − 𝜉2

(13)

Despejando 𝜉 de la ecuación anterior se obtiene la fórmula directa para la razón de

amortiguamiento en términos del decremento medido:

𝜉 =

𝛿

√4𝜋2 + 𝛿2 (14)

Para sistemas ligeramente amortiguados, situación habitual en estructuras civiles donde

𝜉 ≪ 1, la expresión anterior puede aproximarse mediante 𝜉≈𝛿/(2𝜋), aproximación cuyo

error no excede el 1 % para 𝜉 < 0,10 y resulta muy conveniente para estimaciones rápidas

en laboratorio [4].

El procedimiento experimental consiste en imponer al sistema un desplazamiento inicial

controlado o un impulso, liberarlo desde esa configuración y registrar la respuesta x(t) hasta

que las oscilaciones se hayan amortiguado significativamente. Sobre el registro adquirido se

identifican los instantes y las amplitudes de los picos positivos sucesivos, lo que permite

calcular 𝛿 directamente y, a partir de él, estimar 𝜉. Adicionalmente, midiendo el intervalo

de tiempo entre picos se obtiene el periodo amortiguado 𝑇𝑑 y, en consecuencia, la

frecuencia amortiguada 𝜔𝑑= 2𝜋/𝑇𝑑.

Para reducir la incertidumbre experimental asociada a la lectura individual de picos —

especialmente cuando el sistema está poco amortiguado y la diferencia entre picos

consecutivos es pequeña—, se recomienda emplear el decremento promedio sobre N

ciclos. En este caso, comparando un pico xᵢ con el pico 𝑥ᵢ+𝑁 separado 𝑁 periodos, se define

- [5], [6]:

𝛿=

1

𝑁· 𝑙𝑛(

𝑥𝑖

𝑥𝑖+𝑁)

(15)

Este promedio sobre múltiples ciclos amplifica la diferencia de amplitudes y atenúa el efecto

del ruido de medición y de las imprecisiones en la lectura de picos individuales, mejorando

significativamente la calidad de la estimación de 𝜉. Esta es la estrategia que se aplicará en el


<!-- Página 12 -->

presente proyecto para identificar el amortiguamiento de ambos modelos a partir de las

pruebas de vibración libre.


## Integral de Duhamel

La Integral de Duhamel constituye una herramienta analítica de gran generalidad para

determinar la respuesta de un sistema lineal de un grado de libertad ante una excitación

arbitraria 𝐹(𝑡), sin requerir que esta sea armónica, periódica o expresable mediante una

forma cerrada [1], [8]. Su deducción se apoya en el principio de superposición, válido para

sistemas lineales, y en la idea de descomponer cualquier excitación temporal como una

secuencia continua de impulsos infinitesimales.

Si en el instante 𝜏 se aplica al sistema un impulso de magnitud 𝐹(𝜏) · 𝑑𝜏, la masa adquiere

instantáneamente un incremento de velocidad 𝑑𝑣= 𝐹(𝜏) · 𝑑𝜏/𝑚. A partir de ese instante

y en ausencia de excitación posterior, el sistema realiza una vibración libre con condición

inicial de desplazamiento nulo y velocidad dv. La respuesta en el instante 𝑡 > 𝜏 debida

exclusivamente a ese impulso elemental es, en virtud de la solución (8) particularizada a

dichas condiciones iniciales:

𝑑𝑥(𝑡) =

𝐹(𝜏)·𝑑𝜏

𝑚·𝜔𝑑· 𝑒−𝜉·𝜔𝑛·(𝑡−𝜏) · 𝑠𝑖𝑛(𝜔𝑑· (𝑡−𝜏))

(16)

Integrando las contribuciones de todos los impulsos elementales aplicados entre el instante

inicial y el instante 𝑡, se obtiene la respuesta total ante la excitación 𝐹(𝑡), conocida como

integral de Duhamel o integral de convolución [5], [8]:

𝑥(𝑡) =

1

𝑚·𝜔𝑑· ∫𝐹(𝜏) · 𝑒−𝜉·𝜔𝑛·(𝑡−𝜏) · 𝑠𝑖𝑛(𝜔𝑑· (𝑡−𝜏))𝑑𝜏

𝑡

0

(17)

Esta expresión es exacta para sistemas lineales de 1 GDL y supone condiciones iniciales nulas

(𝑥(0) = 0𝑦ẋ(0) = 0). En caso contrario, la respuesta total se obtiene superponiendo la

solución homogénea (8) con condiciones iniciales no nulas y la respuesta forzada dada por

la integral de Duhamel. El núcleo ℎ(𝑡−𝜏) = [1/(𝑚𝜔𝑑)] · 𝑒(−𝜉𝜔ₙ(𝑡−𝜏)) · 𝑠𝑖𝑛(𝜔𝑑(𝑡−𝜏))

recibe el nombre de respuesta al impulso unitario y caracteriza completamente las

propiedades dinámicas del sistema en el dominio del tiempo.

Salvo para excitaciones particularmente simples, la integral (17) no admite solución analítica

cerrada y debe evaluarse numéricamente. Para ello se discretiza la excitación en intervalos

uniformes de duración 𝛥𝑡, con 𝑡ᵢ = 𝑖· 𝛥𝑡 y Fᵢ = 𝐹(𝑡ᵢ), y se aproxima la integral mediante

una regla de cuadratura, típicamente la regla trapezoidal o de Simpson [6], [4]. La forma

discreta de la integral toma la estructura:

𝑥𝑛 =

𝛥𝑡

𝑚·𝜔𝑑· ∑

𝐹𝑖· 𝑒−𝜉·𝜔𝑛·(𝑡𝑛−𝑡𝑖) · 𝑠𝑖𝑛(𝜔𝑑· (𝑡𝑛−𝑡𝑖))

𝑛

𝑖=0

(18)


<!-- Página 13 -->

La evaluación iterativa de la ecuación (18) para n = 0, 1, 2, ..., N proporciona el historial

completo de desplazamientos en los instantes discretos del registro. La derivación numérica

de 𝑥(𝑡) permite obtener adicionalmente las historias de velocidad y aceleración. Existen

formulaciones recursivas más eficientes —basadas en la solución analítica entre dos

instantes consecutivos suponiendo variación lineal de 𝐹(𝑡) en cada paso— que evitan la

acumulación de la convolución completa y resultan mucho más económicas en términos

computacionales [1], [8].

En el contexto de la excitación sísmica, la fuerza efectiva sobre el sistema no es una fuerza

aplicada directamente sobre la masa, sino una fuerza inercial inducida por el movimiento

de la base. Si ẍ𝑔(𝑡) denota la aceleración del terreno registrada por un acelerógrafo, la

ecuación de movimiento del sistema de 1 GDL referida al desplazamiento relativo 𝑥(𝑡) =

𝑥𝑡𝑜𝑡𝑎𝑙(𝑡) −𝑥𝑔(𝑡) adopta la forma 𝑚· ẍ+ 𝑐· ẋ+ 𝑘· 𝑥= −𝑚· ẍ𝑔(𝑡). Esto equivale a

aplicar al sistema una fuerza ficticia 𝐹(𝑡) = −𝑚· ẍ𝑔(𝑡), de modo que la integral de

Duhamel proporciona directamente la respuesta sísmica relativa de la estructura:

𝑥(𝑡) = −

1

𝜔𝑑· ∫𝑥𝑔̈ (𝜏) · 𝑒−𝜉·𝜔𝑛·(𝑡−𝜏) · 𝑠𝑖𝑛(𝜔𝑑· (𝑡−𝜏))𝑑𝜏

𝑡

0

(19)

La ecuación (19) constituye la base del cálculo del espectro de respuesta de desplazamientos

para un registro sísmico dado y será la herramienta numérica fundamental empleada en el

capítulo de Simulación Numérica del presente trabajo.


## Modelos de edificios como sistemas discretos

Los edificios reales son estructuras continuas con masa y rigidez distribuidas espacialmente.

Sin embargo, para fines de análisis dinámico, resulta habitual y razonable representar el

edificio como un sistema discreto de pocos grados de libertad. Esta idealización, conocida

como modelo de masas concentradas o lumped-mass model, asume que la mayor parte de

la masa del edificio se concentra en las losas de entrepiso —tradicionalmente mucho más

pesadas y rígidas en su plano que las columnas— y que la masa propia de las columnas es

despreciable frente a la masa del entrepiso [1], [5]. En consecuencia, cada nivel del edificio

se modela como una masa puntual cuyo desplazamiento horizontal constituye un grado de

libertad traslacional, y las columnas se idealizan como elementos elásticos sin masa que

aportan exclusivamente rigidez lateral.

Bajo esta hipótesis, un edificio de n pisos posee n grados de libertad horizontales (uno por

nivel, asumiendo análisis planar en una sola dirección). El modelo resultante recibe el

nombre de edificio shear building cuando se admite además que las losas son axialmente

rígidas e infinitamente rígidas a flexión en su plano, lo que impide la rotación de los nudos

viga-columna. En este modelo, las columnas se deforman exclusivamente en doble


<!-- Página 14 -->

curvatura entre niveles, comportándose como elementos bi-empotrados 3sometidos a un

desplazamiento relativo entre sus extremos [5].

La rigidez lateral de una columna empotrada en ambos extremos, sometida a un

desplazamiento relativo Δ entre sus extremos, se obtiene de la teoría elemental de vigas

como [6], [4]:

𝑘𝑐𝑜𝑙 =

12·𝐸·𝐼

𝐿3 (20)

donde E es el módulo de elasticidad del material de la columna, I es el momento de inercia

de su sección transversal respecto al eje de flexión correspondiente y L es la altura libre del

entrepiso. Para una columna de sección rectangular 𝑏 × ℎ flexionada en torno a su eje

débil o fuerte, 𝐼= 𝑏· ℎ3/12. La rigidez lateral total del entrepiso se obtiene sumando las

rigideces de todas las columnas que lo componen, lo que para 𝑛𝑐𝑐𝑜𝑙𝑢𝑚𝑛𝑎 columnas idénticas

conduce a 𝑘𝑝í𝑠𝑜 = 𝑛𝑐𝑐𝑜𝑙𝑢𝑚𝑛𝑎· 12𝐸𝐼/𝐿3.

Para un edificio de dos pisos como los del presente proyecto, el modelo discreto se reduce

a un sistema de dos grados de libertad cuyas matrices de masa y rigidez fueron presentadas

en las ecuaciones (5) y (6). Las masas m₁ y m₂ corresponden a las masas concentradas

añadidas en cada nivel, mientras que las rigideces k₁ y k₂ se obtienen aplicando la ecuación

(20) a las columnas del primer y segundo entrepiso, respectivamente. La ecuación de

movimiento del sistema toma entonces la forma:

[𝑚1

0

0

𝑚2] [𝑥1̈

𝑥2̈ ] + [𝑘1 + 𝑘2

−𝑘2

−𝑘2

𝑘2 ] [

𝑥1

𝑥2] = [𝐹1(𝑡)

𝐹2(𝑡)]

(21)

donde se ha omitido temporalmente la matriz de amortiguamiento, que se introducirá en

el capítulo del modelo matemático mediante una formulación de Rayleigh consistente con

los amortiguamientos modales identificados experimentalmente.

La simplificación al caso planar se justifica en el presente proyecto por la simetría

geométrica y de masas de los modelos respecto al eje longitudinal de la tabla base. Al excitar

la mesa vibratoria en una sola dirección horizontal coincidente con un eje principal de la

estructura, no se inducen modos torsionales ni acoplamiento con la dirección perpendicular,

de modo que el análisis bidimensional captura adecuadamente la respuesta de los edificios

sin pérdida significativa de fidelidad. Los efectos de segundo orden, la deformación axial de

las columnas y la flexión de las losas de balsa se consideran despreciables dado el rango de

desplazamientos esperados y la rigidez relativa entre los elementos del modelo [1], [5].

3 Un elemento bi-empotrado es un elemento estructural cuyos dos extremos están restringidos contra

traslación y rotación.


<!-- Página 15 -->


## Amortiguamiento de Rayleigh

El amortiguamiento de Rayleigh es un modelo de amortiguamiento viscoso proporcional

utilizado en dinámica estructural, en el cual la matriz de amortiguamiento se aproxima como

una combinación lineal de la matriz de masa y la matriz de rigidez del sistema. Según la

formulación presentada por Chopra [1], este modelo permite representar la disipación de

energía de una estructura mediante dos coeficientes: uno asociado a la masa y otro asociado

a la rigidez.

Para un sistema dinámico estructural, la ecuación de movimiento se expresa como:

𝑴𝑢̈ + 𝐶𝑢̇ + 𝐾𝑢= 𝑃(𝑡)

En el modelo de Rayleigh, la matriz de amortiguamiento se define como:

𝑪= α𝑀+ β𝐾

donde 𝛂 es el coeficiente proporcional a la masa y 𝛃 es el coeficiente proporcional a la

rigidez. La razón de amortiguamiento modal para el modo 𝒏 se obtiene como:

ξ𝑛=

α

2ω𝑛

+ βω𝑛

2

donde ω𝑛 es la frecuencia circular natural del modo 𝑛. Estos coeficientes suelen

determinarse a partir de dos modos de vibración seleccionados, de manera que el

amortiguamiento se ajuste a valores objetivo en dichas frecuencias.


# Descripción Del Modelo Físico


## Descripción general de los edificios

El sistema físico construido para el presente estudio está compuesto por dos modelos a

escala reducida de edificios de dos pisos, ambos solidariamente fijados a una tabla base

común de madera, de dimensiones aproximadas 45,72 cm × 40 cm × 1,25 cm. Esta tabla

base se monta a su vez sobre la plataforma de la mesa vibratoria, lo que garantiza que ambos

modelos experimenten exactamente la misma excitación en cada uno de los ensayos. La

elección de una base común busca, además, eliminar diferencias en las condiciones de

borde y permitir una comparación directa de la respuesta dinámica de los dos edificios bajo

idéntica solicitación.

El primer edificio, denominado en lo sucesivo edificio esbelto, se concibió con una

geometría alta y de baja huella en planta. Posee dos pisos cuya altura individual se

encuentra en el rango de 40 a 50 cm, lo que conduce a una altura total comprendida entre

> Comentado [ACR3]: Acá hay que poner el modelo de la

mesa de lab


<!-- Página 16 -->

80 y 100 cm. Esta configuración produce un modelo con frecuencias naturales bajas y

deformaciones laterales notables, característico de edificios flexibles o de gran altura. El

segundo edificio, denominado edificio chato, presenta por contraste una geometría baja y

compacta: ambos pisos tienen una altura individual entre 15 y 20 cm, de modo que su altura

total no excede los 40 cm. Su mayor relación de aspecto en planta y la menor longitud libre

de sus columnas le confieren una rigidez lateral sustancialmente superior y, en

consecuencia, frecuencias naturales más elevadas que las del modelo esbelto.

Ambos edificios responden al mismo esquema estructural: un sistema de tipo marco

constituido por cuatro columnas verticales de madera balsa, dispuestas en las esquinas de

la huella en planta, que conectan dos losas horizontales —el primer piso y el techo o

segundo piso— con la tabla base. La unión entre las columnas y las losas se diseña como un

empotramiento perfecto, materializado mediante la combinación de adhesivo y elementos

de fijación adicionales en los nudos, de manera que la hipótesis de columnas bi-empotradas

adoptada en el marco teórico resulte aceptablemente cumplida en la práctica [5], [4].

En la dirección de aplicación del movimiento de la mesa vibratoria —que constituye el eje

principal de análisis— los edificios no incluyen ningún tipo de arriostre diagonal ni pared de

relleno, de modo que la rigidez lateral del sistema queda íntegramente provista por la flexión

de las columnas. En la dirección perpendicular, en cambio, se incorporan arriostres

transversales que rigidizan los marcos no resistentes al sismo, suprimiendo así los modos de

vibración fuera del plano de análisis y asegurando que la respuesta de los modelos pueda

interpretarse correctamente como un sistema bidimensional de dos grados de libertad, en

plena coherencia con el modelo.


## Especificaciones geométricas

La Tabla 2 resume las dimensiones nominales y los rangos geométricos de diseño de ambos

modelos. Las mediciones fueron efectuadas al terminar la construcción por lo que son

medidas finales y definitivas. El elemento shear builiding fue construido según las

especificaciones brindadas y el modelo presente en las instrucciones, figura 1, 2 y 3.


<!-- Página 17 -->


**Figura 1. Dimensiones en la elevación para los dos edificios. a) edificio esbelto, b) edificio**

chato. [9]


**Figura 2. Dimensiones máximas y mínimas en planta de los 2 edificios, uno esbelto y otro**

chato. [9]


<!-- Página 18 -->


**Figura 3. Sistemas de arriostramiento en el sentido transversal al movimiento. [9]**


**Tabla 2. Especificaciones geométricas comparativas de los dos modelos de edificio.**

Parámetro geométrico

Edificio esbelto

Edificio chato

Huella en planta (largo ×

ancho)

16cm x 16cm

16cm x 15cm

Altura de piso (entrepiso)

40cm

16cm

Número de pisos

2

2

Altura total del edificio

80cm

32cm

Sección

transversal

de

columnas (b × h)

6 mm x 6 mm

6 mm x 6 mm

Número de columnas por

piso

4 (una en cada esquina)

4 (una en cada esquina)

Arriostres en dirección de

movimiento

Ninguno

Ninguno

Arriostres

en

dirección

transversal

Sí, en x

Sí, en x

Según lo especificado se obtuvo el siguiente resultado presente en la figura 4.


<!-- Página 19 -->


**Figura 4. Modelo resultante para estudio dinámico. Autoría propia.**


## Materiales y propiedades mecánicas

El material constitutivo principal de las columnas y losas de ambos modelos es madera

balsa, seleccionada por su baja densidad, su trabajabilidad y su comportamiento

aproximadamente elástico-lineal en el rango de deformaciones esperado durante los

ensayos. La madera balsa presenta una variabilidad apreciable en sus propiedades

mecánicas, atribuible al grado de humedad, al sentido de la fibra y a la procedencia de la

pieza. Para fines de prediseño se adoptan los siguientes valores de referencia, reportados

en la literatura técnica de materiales ligeros: densidad típica entre 100 y 200 kg/m³, módulo

de elasticidad longitudinal (paralelo a la fibra) en el rango de 3 a 4 GPa, y resistencia a la

flexión del orden de 10 a 20 MPa [10].

Dada la importancia que el módulo de elasticidad E reviste en el cálculo de la rigidez lateral

de las columnas (ecuación 20) [4], su valor definitivo se determinará de dos formas

complementarias durante la fase experimental. En primer lugar, se solicitarán al proveedor

las propiedades certificadas del lote de madera empleado, cuando estas se encuentren

disponibles. En segundo lugar, se realizarán ensayos auxiliares de flexión sobre probetas

testigo recortadas del mismo material y direccionalidad que las columnas, lo que permitirá

> Comentado [ACR4]: Buscar cita, la perdí

> Comentado [ACR5]: Buscar cita, la perdí


<!-- Página 20 -->

ajustar el valor de E al material efectivamente utilizado. Cualquier discrepancia significativa

entre el valor adoptado en el prediseño y el valor experimental se reflejará en la calibración

del modelo matemático descrito previamente.

Las uniones entre columnas, losas y tabla base se materializan mediante adhesivo,

seleccionando para tal efecto cola blanca, Lanco grip bond 4 (acetato de polivinilo) en las

uniones de carga principal, dada su penetración en la fibra de balsa y su capacidad para

desarrollar resistencias adecuadas tras el curado.


**Figura 5. Cola blanca empleada para la fabricación.**

Como criterio constructivo, se limita el traslape en las uniones de madera balsa a un máximo

de 40 mm [9]. Esta restricción busca evitar excesos de adhesivo y zonas con rigidez adicional

que puedan alterar el comportamiento dinámico del modelo. Además, en las uniones

columna-losa, un traslape excesivo podría modificar la longitud libre efectiva de la columna

y afectar el cálculo de su rigidez lateral.


## Sistema de masas

Con el objetivo de materializar físicamente la hipótesis de masas concentradas en cada nivel

—fundamento del modelo discreto de dos grados de libertad introducido previamente—,

ambos edificios incorporan en cada uno de sus pisos un conjunto de masas estandarizadas,

cuya magnitud es significativamente superior a la masa propia de las losas y columnas de


<!-- Página 21 -->

balsa, de modo que la idealización lumped-mass resulte una representación fiel del sistema

real.

El sistema de masas se construye en torno a una barra roscada de 3/8 de pulgada y 22 cm

de longitud, dispuesta horizontalmente y atravesando ambas losas a través de

canalizaciones pasantes practicados en su geometría. Esta barra cumple la doble función de

servir de elemento guía para el ensamblaje y de soporte estructural para las masas,

asegurando su posicionamiento centrado y su solidaridad con la respectiva losa. Las masas

propiamente dichas consisten en discos cilíndricos calibrados de 0,5 kg de peso nominal y

8,5 cm de diámetro, cada uno con un orificio central que permite enhebrarlos sobre la barra

roscada [9].

Las masas se fijan al sistema mediante tuercas hexagonales y arandelas planas que las

comprimen contra la losa de su correspondiente nivel, asegurando un contacto firme y

suprimiendo cualquier holgura o juego que pudiera introducir disipación de energía

adicional o no linealidades en el comportamiento dinámico. La cantidad de discos colocados

en cada piso podrá ajustarse durante la fase experimental con el fin de explorar distintas

configuraciones de distribución de masa entre los niveles y, eventualmente, sintonizar las

frecuencias naturales del modelo en el rango deseado.

A continuación, se presenta la distribución de masas en el sistema:


**Tabla 3. Distribución del sistema de masas en los dos modelos.**

Componente

Edificio esbelto

Edificio chato

Masa nominal por disco

0,5 kg

0,5 kg

Diámetro de disco

8,5 cm

8,5 cm

Barra roscada (diámetro ×

longitud)

3/8" × 22 cm

3/8" × 22 cm

Número de discos en el

primer piso

1

1

Número de discos en el

segundo piso

1

1

Masa concentrada total m₁

(primer piso)

0.7Kg

0.7Kg

Masa concentrada total m₂

(segundo piso)

0.7Kg

0.7Kg

Masa total del edificio

Despreciable

Despreciable

Elementos de fijación

Tuercas + arandelas planas

Tuercas + arandelas planas

> Comentado [ACR6]: Buscar la cita

> Comentado [ACR7R6]: También agregar a marco teórico


<!-- Página 22 -->


## Repositorio para la replicación del análisis

Con el fin de compartir académicamente el desarrollo del experimento y su análisis con

futuras generaciones, se dejarán disponibles los documentos, datos experimentales y

archivos utilizados durante el proyecto en un repositorio de GitHub. Este material podrá

consultarse

en

el

siguiente

enlace:

https://github.com/adrianix360/RepositorioProyectoDeDinamicaUCR.git


# Metodología Experimental


## Prueba de vibración libre

La prueba de vibración libre constituye el ensayo experimental más sencillo y directo para

identificar las propiedades dinámicas fundamentales de cada modelo: sus frecuencias

naturales y sus razones de amortiguamiento modal. El procedimiento parte de imponer al

edificio una condición inicial controlada, conocida, fuera de su posición de equilibrio, y

registrar la respuesta libre que se desarrolla espontáneamente tras liberar el sistema, en

ausencia de toda excitación externa adicional [1], [6].

La condición inicial se materializa de dos maneras complementarias, que se ejecutarán de

forma alternativa según el modo de vibración que se desee excitar. La primera consiste en

aplicar un desplazamiento estático en el extremo superior del edificio mediante una fuerza

horizontal controlada, midiendo la deformación impuesta antes de liberar el sistema; esta

configuración excita preferentemente el primer modo de vibración, que es el de mayor

amplitud y menor frecuencia. La segunda consiste en aplicar un impulso súbito —un

pequeño golpe lateral controlado con un instrumento calibrado— en distintos niveles del

edificio, lo que permite excitar simultáneamente ambos modos del sistema de 2 GDL y

favorecer la identificación posterior del segundo modo en el espectro de frecuencias.

La respuesta libre del sistema se registra mediante un acelerómetro adherido al segundo

piso, dado que este nivel exhibe las mayores amplitudes en ambos modos del edificio. De

manera complementaria, puede instalarse un segundo acelerómetro en el primer piso para

reconstruir las formas modales experimentales y verificar el carácter del movimiento. La

adquisición de datos se realizará a una frecuencia de muestreo no inferior a 200 Hz,

suficiente para resolver las frecuencias naturales esperadas en el rango de unos pocos hertz

> Comentado [ACR8]: Antes de mandarlo recuerdenme

subir los datos a GitHub


<!-- Página 23 -->

hasta varias decenas de hertz, conforme al criterio de Nyquist4 y dejando un margen amplio

para evitar fenómenos de aliasing5 [7].

Para cada modelo se realizarán al menos cinco pruebas de vibración libre con condiciones

iniciales nominalmente idénticas, con el fin de promediar los parámetros identificados y

reducir la incertidumbre asociada a la repetibilidad del ensayo. De cada registro se

extraerán: la historia temporal de aceleración (o desplazamiento) del segundo piso, el

tiempo total de oscilación significativa, las amplitudes y los instantes de los picos sucesivos,

el periodo amortiguado aparente y la frecuencia de muestreo efectiva. Estos parámetros

constituyen los insumos para las identificaciones modales descritas previamente.


## Identificación de frecuencias naturales

La identificación experimental de las frecuencias naturales de cada modelo se aborda

mediante el análisis en el dominio de la frecuencia del registro de vibración libre adquirido

en la sección Prueba de vibración libre. La técnica empleada es la transformada rápida de

Fourier (FFT, Fast Fourier Transform), que descompone la señal temporal 𝑥(𝑡) —o, en este

caso, la aceleración registrada ẍ(𝑡)— en una superposición discreta de componentes

armónicas, cuya amplitud y fase dependen de la frecuencia [7], [4].

Dado un registro discreto 𝑥ₙ de N muestras adquiridas con un intervalo 𝛥𝑡, la FFT entrega

un vector complejo 𝑋ₖ de N coeficientes, cuya magnitud al cuadrado constituye el espectro

de potencia de la señal:

|𝑋𝑘|2 = |∑

𝑥𝑛· 𝑒−𝑖·2𝜋·𝑘·𝑛/𝑁

𝑁−1

𝑛=0

|

2 (22)

El espectro de potencia de la respuesta libre subamortiguado de un sistema de n GDL exhibe

un pico pronunciado en torno a cada una de las frecuencias naturales amortiguadas del

sistema. Para los modelos del presente trabajo, sistemas de 2 GDL, se esperan dos picos

espectrales claramente distinguibles, asociados al primer modo (frecuencia más baja,

traslación en fase de ambos pisos) y al segundo modo (frecuencia más alta, traslación en

oposición de fase). La frecuencia de cada pico se identifica directamente sobre el espectro

como la abscisa del máximo local, y a partir de ella se calcula la frecuencia natural

amortiguada 𝑓𝑑,𝑖= 𝑚𝑎𝑥|𝑥𝑘|2 del modo correspondiente.

4 El criterio de Nyquist establece que, para registrar correctamente una señal dinámica, la frecuencia de

muestreo debe ser al menos el doble de la frecuencia máxima presente en la señal. De esta forma se evita el

fenómeno de aliasing, en el cual una señal de alta frecuencia puede interpretarse erróneamente como una de

menor frecuencia.

5 El aliasing es un fenómeno que ocurre cuando una señal se registra con una frecuencia de muestreo

insuficiente. En este caso, las componentes de alta frecuencia no se representan correctamente y pueden

aparecer como señales falsas de menor frecuencia.


<!-- Página 24 -->

La frecuencia natural circular amortiguada se obtiene mediante 𝜔𝑑,𝑖= 2𝜋· 𝑓𝑑,𝑖, y la

frecuencia natural no amortiguada se recupera a partir de la relación (9) del marco teórico,

𝜔𝑛,𝑖= 𝜔𝑑,𝑖/√(1 −𝜉ᵢ2). Para razones de amortiguamiento pequeñas, propias de las

estructuras civiles, esta corrección es despreciable y se acepta 𝜔ₙ ≈𝜔𝑑 a efectos prácticos.

La resolución espectral de la FFT es 𝛥𝑓= 1/(𝑁· 𝛥𝑡), por lo que la duración total del registro

y la frecuencia de muestreo se eligen para garantizar una resolución suficiente que separe

ambos picos. Cuando se detecte una proximidad excesiva entre los modos —situación poco

probable dada la asimetría geométrica entre el edificio esbelto y el chato— se recurrirá a

registros más largos y al promedio espectral entre ensayos sucesivos para mejorar la nitidez

del espectro.


## Identificación del amortiguamiento

La razón de amortiguamiento modal de cada modo se identifica mediante el método del

decremento logarítmico introducido en la sección 8.5 del marco teórico [1], [6], aplicado al

registro de vibración libre filtrado para aislar la contribución de cada modo. El

procedimiento consta de las siguientes etapas:

En primer lugar, se filtra el registro de aceleración del segundo piso mediante un filtro

pasabanda6 centrado en torno a la frecuencia natural identificada en la sección Prueba de

vibración libre para el modo de interés, con un ancho de banda suficientemente estrecho

como para suprimir la contribución del otro modo y del ruido de medición, pero lo bastante

amplio como para no distorsionar la envolvente exponencial de la respuesta.

En segundo lugar, sobre la señal filtrada se identifican los instantes y las amplitudes de los

picos positivos sucesivos 𝑥1, 𝑥2, … , 𝑥(𝑁+1) mediante un algoritmo de detección de máximos

locales. La elección de N picos consecutivos —entre los cuales se calculará el decremento—

es un compromiso entre la mejora estadística que aporta el promedio sobre múltiples ciclos

y la pérdida de información asociada a las últimas oscilaciones, cuya amplitud se aproxima

al nivel de ruido. Para los modelos del presente trabajo se contempla un valor de N entre 5

y 10 ciclos.

En tercer lugar, el decremento logarítmico promedio se calcula aplicando la ecuación (15)

del marco teórico, particularizada al modo y al registro:

𝛿𝑖=

1

𝑁· 𝑙𝑛(

𝑥1

𝑥𝑁+1)

(23)

6 Un filtro pasabanda es un filtro que permite conservar las componentes de una señal dentro de un rango

específico de frecuencias, mientras atenúa las frecuencias que se encuentran por debajo y por encima de ese

intervalo. En análisis dinámico, se utiliza para aislar la parte de la señal asociada al comportamiento de interés

y reducir el efecto de ruido o vibraciones no deseadas.


<!-- Página 25 -->

Finalmente, la razón de amortiguamiento del modo i se despeja mediante la ecuación (14),

aplicada al decremento medido:

𝜉𝑖 =

𝛿𝑖

√4𝜋2 + 𝛿𝑖

2

(24)

Este procedimiento se repite para el primer y segundo modo de cada uno de los dos

edificios, promediando los valores obtenidos sobre las cinco repeticiones recomendadas en

la sección 10.1. El producto final de la identificación experimental es un par de razones de

amortiguamiento modal (𝜉1, 𝜉2) por edificio, que alimentarán la construcción de la matriz

de amortiguamiento [C] del modelo matemático mediante el procedimiento de Rayleigh

descrito previamente.


## Prueba de vibración forzada

La prueba de vibración forzada se realiza con el fin de observar cómo responde cada edificio

cuando la base se mueve de forma controlada mediante la mesa vibratoria. A diferencia de

la vibración libre, en este ensayo la estructura no oscila por un impacto inicial, sino por una

excitación continúa aplicada desde la base.

Para cada edificio, se aplican diferentes frecuencias de movimiento en la mesa vibratoria y

se registra la respuesta del piso superior. En cada frecuencia se espera a que la respuesta se

estabilice y luego se mide la amplitud representativa del movimiento. Con estos datos se

construye una curva de respuesta, donde se compara la frecuencia aplicada con la amplitud

obtenida en el edificio.

El punto más importante de esta prueba es identificar la frecuencia en la que el edificio

presenta su mayor amplitud de movimiento. Esta condición corresponde a la resonancia y

permite verificar, de forma experimental, las frecuencias naturales obtenidas previamente

con la prueba de vibración libre y la FFT. Además, al comparar el movimiento de la base con

el movimiento del piso superior, se puede observar el desfase entre ambas señales y analizar

cómo cambia la respuesta del edificio antes, durante y después de la resonancia.

En esta sección se presentarán, para cada edificio, las gráficas de desplazamiento de la base

y del piso superior, los acercamientos alrededor de la resonancia, una tabla con la frecuencia

aplicada y la amplitud medida, y la curva de respuesta experimental. Finalmente, se

compararán los resultados del edificio esbelto y del edificio chato para discutir cuál presenta

mayor amplificación dinámica, cuál posee mayor rigidez y cómo varía su comportamiento

ante una misma excitación.


<!-- Página 26 -->


## Prueba sísmica en mesa vibratoria

La etapa culminante de la fase experimental consiste en someter ambos modelos,

simultáneamente, a una excitación sísmica reproducida por la mesa vibratoria del

laboratorio. Esta prueba persigue dos objetivos: por un lado, evaluar la respuesta de los

edificios ante registros sísmicos realistas y observar fenómenos de amplificación dinámica

análogos a los que ocurren en estructuras reales; por otro, contrastar las historias

temporales de desplazamiento y aceleración registradas experimentalmente con las

predicciones de la simulación numérica mediante la integral de Duhamel, desarrollada

previamente [1], [8].

La selección de los registros sísmicos a utilizar se realizará atendiendo a tres criterios. En

primer lugar, se priorizarán registros representativos del entorno sísmico de Costa Rica y

Centroamérica, considerando eventos históricos de magnitud y condiciones de sitio

diversas, con el propósito de exponer los modelos a contenidos frecuenciales realistas para

el contexto regional [2], [3]. En segundo lugar, se incluirá al menos un registro cuyo

contenido espectral dominante se aproxime a la primera frecuencia natural del edificio

esbelto y otro que se acerque a la del edificio chato, con el fin de evidenciar el fenómeno

de resonancia entre ambos modelos bajo una misma solicitación. En tercer lugar, se

contemplará un registro de banda ancha.

Durante cada ensayo sísmico, los acelerómetros instalados en el primer y segundo piso de

ambos edificios —así como un acelerómetro de referencia adherido a la tabla base, que

registra la excitación efectivamente impuesta por la mesa— adquirirán simultáneamente las

historias temporales de aceleración. A partir de las señales registradas, podrán reconstruirse

asimismo los datos de velocidad y desplazamiento de cada nivel. Estas series temporales

constituirán el insumo principal del capítulo de resultados experimentales y servirán de

referencia para evaluar la fidelidad de las predicciones del modelo matemático calibrado.


# Modelo Matemático


## Ecuaciones de movimiento

El modelo matemático adoptado para ambos edificios corresponde al sistema discreto de

dos grados de libertad introducido previamente. Bajo excitación sísmica, el movimiento del

sistema se describe respecto al desplazamiento relativo de cada piso respecto a la base, lo

que conduce a la ecuación matricial fundamental [1], [5]:

[𝑀] · 𝑥̈(𝑡) + [𝐶] · 𝑥̇(𝑡) + [𝐾] · 𝑥(𝑡) = −[𝑀] · {1} · 𝑥𝑔̈ (𝑡) (25)


<!-- Página 27 -->

donde 𝑥(𝑡) = [𝑥1(𝑡)𝑥2(𝑡)]ᵀ es el vector de desplazamientos relativos del primer y segundo

piso respecto a la base, ẍ𝑔(𝑡) es la aceleración del suelo registrada por el acelerómetro de

referencia, y 1 = [11]ᵀ es el vector unitario de coeficientes de influencia que distribuye la

aceleración de la base sobre todos los grados de libertad traslacionales del sistema, en

virtud de la hipótesis de excitación rígida de la base. El segundo miembro de la ecuación

(26) representa la fuerza inercial efectiva inducida por el movimiento del suelo, en plena

consistencia con la formulación sísmica de la integral de Duhamel anteriormente [1], [8].

Para un edificio de dos pisos con masas concentradas, la matriz de masa es diagonal y la

matriz de rigidez adopta la forma tridiagonal característica del shear building.

Reproduciendo las expresiones (5) y (6) particularizadas al caso de 2 GDL:

[𝑀] = [𝑚1

0

0

𝑚2] , [𝐾] = [𝑘1 + 𝑘2

−𝑘2

−𝑘2

𝑘2 ] (26)

donde m₁ y m₂ son las masas concentradas del primer y segundo piso, medidas físicamente

como el total de discos de 0,5 kg colocados sobre la barra roscada de cada nivel. Las rigideces

de entrepiso k₁ (entre la base y el primer piso) y k₂ (entre el primer y segundo piso) se

obtienen sumando las rigideces laterales individuales de las columnas que componen cada

entrepiso. Asumiendo 𝑛𝑐𝑜𝑙𝑢𝑚𝑛𝑎 columnas idénticas en el entrepiso i, con sección b × h,

módulo de elasticidad E y altura libre ℎᵢ, la rigidez total del entrepiso es [4]:

𝑘𝑖 = ∑

12·𝐸·𝐼

ℎ𝑖

3 = 𝑛𝑐𝑜𝑙·

12·𝐸·𝐼

ℎ𝑖

3 (27)

con𝐼= 𝑏· ℎ3/12 el momento de inercia de la sección transversal respecto al eje débil o

fuerte de flexión, según la dirección de aplicación del movimiento. La matriz de

amortiguamiento [C] no se obtiene a partir de propiedades constitutivas del material, sino

que se construye a posteriori por el método de Rayleigh, expresándola como una

combinación lineal de las matrices de masa y rigidez [1], [5]:

[𝐶] = 𝛼[𝑀] + 𝛽[𝐾] (28)

donde los coeficientes α y β se eligen para reproducir las razones de amortiguamiento

modales 𝜉1y 𝜉2 identificadas experimentalmente. Esta formulación garantiza que [C] sea

ortogonal respecto a los modos del sistema no amortiguado y que el desacople modal

habitual del análisis dinámico siga siendo aplicable. El sistema completo de dos ecuaciones

diferenciales acopladas en (26) constituye el modelo matemático que se calibrará y simulará

en las secciones siguientes.


<!-- Página 28 -->


## Determinación de parámetros dinámicos

Los parámetros dinámicos del modelo matemático —masas, rigideces, frecuencias

naturales y amortiguamientos— se determinan combinando información geométrica y de

materiales del modelo físico con los resultados de los ensayos de identificación

experimental. El procedimiento se estructura como sigue.

Las masas concentradas 𝑚ᵢ se obtienen directamente como 𝑚ᵢ= 𝑛ᵢ· 𝑚𝑑𝑖𝑠𝑐𝑜, donde 𝑛ᵢ es el

número de discos efectivamente instalados en el piso i durante los ensayos y 𝑚𝑑𝑖𝑠𝑐𝑜= 0,5

kg es la masa nominal de cada disco. Esta lectura directa elimina toda incertidumbre

asociada a la estimación indirecta de la masa, dejando como única fuente de error la

tolerancia de fabricación de los discos calibrados.

Las rigideces de entrepiso kᵢ se calculan a partir de la ecuación (28), sustituyendo las

dimensiones geométricas medidas en el modelo construido (𝑛𝑐𝑜𝑙𝑢𝑚𝑛𝑎, 𝑏, ℎ, ℎᵢ) y el módulo

de elasticidad E adoptado inicialmente del rango referencial de la balsa (3–4 GPa). El

momento de inercia I se calcula como 𝐼= 𝑏· ℎ3/12 para la dirección de flexión

correspondiente al movimiento aplicado. Las frecuencias naturales no amortiguadas del

sistema de 2 GDL se obtienen como las raíces cuadradas de los autovalores del problema

generalizado [1], [5]:

𝑑𝑒𝑡([𝐾] −𝜔𝑛

2 · [𝑀]) = 0 (29)

Para el sistema de 2 GDL con [M] y [K] dados por (27), el desarrollo del determinante

conduce a una ecuación bicuadrática en ωₙ²:

𝑚1 · 𝑚2 · 𝜔𝑛

4 − [𝑚1 · 𝑘2 + 𝑚2 · (𝑘1 + 𝑘2)] · 𝜔𝑛

2 + 𝑘1 · 𝑘2 = 0

(30)

cuyas dos raíces positivas 𝜔ₙ, 12 y 𝜔ₙ, 22 (con 𝜔ₙ, 1 < 𝜔ₙ, 2) corresponden a las

frecuencias circulares naturales del primer y segundo modo del sistema, respectivamente.

Las frecuencias cíclicas analíticas se obtienen como 𝑓𝑛,𝑖= ω(𝑛,𝑖)/(2𝜋) y se comparan con

las frecuencias amortiguadas identificadas experimentalmente por FFT, recordando

que𝑓𝑑,𝑖≈𝑓𝑛,𝑖 para amortiguamientos pequeños.

Una vez obtenidas las frecuencias modales y las razones de amortiguamiento

experimentales (𝜉1, 𝜉2), los coeficientes de Rayleigh 𝛼 y 𝛽 se despejan resolviendo el

sistema:

𝜉1 =

𝛼

2·𝜔𝑛,1 +

𝛽·𝜔𝑛,1

2

(31)

𝜉2 =

𝛼

2·𝜔𝑛,2 +

𝛽·𝜔𝑛,2

2

(32)


<!-- Página 29 -->

que proporciona los valores únicos de α y β que reproducen ambos amortiguamientos

modales identificados, completando así la construcción de la matriz de amortiguamiento [C]

de la ecuación (29). Con [M], [K] y [C] determinados, el modelo matemático del edificio

queda completamente especificado y listo para ser simulado bajo cualquier excitación

sísmica mediante la integral de Duhamel discretizada del capítulo 12 [8].


## Calibración del modelo

Con los parámetros nominales obtenidos según la sección 11.2, las frecuencias naturales

analíticas raramente coincidirán de manera exacta con las identificadas experimentalmente:

la variabilidad natural del módulo de elasticidad de la balsa entre lotes y dentro de una

misma pieza, las tolerancias dimensionales de la sección de las columnas, el carácter no

perfectamente empotrado de las uniones reales y las masas estructurales no contabilizadas

en 𝑚𝑑𝑖𝑠𝑐𝑜 son fuentes legítimas de discrepancia [4], [3]. El proceso de calibración consiste

en ajustar uno o varios parámetros del modelo de manera que las frecuencias naturales

analíticas reproduzcan las frecuencias experimentales dentro de una tolerancia acordada.

El módulo de elasticidad E de la balsa se adopta como parámetro principal de calibración,

por tres razones complementarias. En primer lugar, su valor referencial reportado en la

literatura presenta una dispersión amplia (3 a 4 GPa, y aún mayor entre especímenes), lo

que justifica refinarlo experimentalmente. En segundo lugar, E interviene linealmente en

cada rigidez de entrepiso a través de la ecuación (28), y por ende interviene de manera

escalable en ambas frecuencias modales sin alterar las formas modales del sistema. En

tercer lugar, las masas y las dimensiones geométricas son medibles con menor

incertidumbre que el módulo de elasticidad y, por tanto, no procede modificarlas en

ausencia de evidencia de error de medición.

El procedimiento de calibración se aborda como un problema de mínimos cuadrados sobre

las dos frecuencias modales. Se define la función de discrepancia:

𝐽(𝐸) = 𝑤1 · (𝑓𝑛,1(𝐸) −𝑓𝑒𝑥𝑝,1)

2 + 𝑤2 · (𝑓𝑛,2(𝐸) −𝑓𝑒𝑥𝑝,2)

2

(33)

donde 𝑓ₙ(𝐸) son las frecuencias analíticas obtenidas resolviendo (31) con las rigideces (28)

recalculadas para el valor de E vigente, 𝑓𝑒𝑥𝑝,𝑖 son las frecuencias identificadas

experimentalmente y w₁, w₂ son pesos que pueden ajustarse para priorizar la concordancia

en el primer modo —usualmente el más importante para la respuesta sísmica— o para

ponderarlos por igual. El módulo calibrado E es aquel que minimiza J, y se obtiene mediante

una búsqueda unidimensional en el rango físicamente admisible para la balsa.

Tras la calibración, las frecuencias analíticas reproducirán las experimentales dentro de un

error residual asociado a las limitaciones del modelo discreto: hipótesis de empotramiento


<!-- Página 30 -->

perfecto, masa concentrada idealizada, ausencia de torsión y amortiguamiento de tipo

Rayleigh, entre otras. Cuando este error residual exceda una tolerancia razonable —del

orden del 5 % en cada frecuencia— se procederá a un análisis crítico de las hipótesis del

modelo y, eventualmente, a la introducción de correcciones complementarias, tales como

una rigidez efectiva reducida en la base para simular la flexibilidad real de las uniones

empotradas, o un incremento de las masas concentradas para reflejar la masa estructural

de las losas y elementos secundarios. Cualquier ajuste adicional se documentará

explícitamente y se justificará a la luz de las observaciones experimentales.


# Simulación Numérica


## Método de la Integral de Duhamel


## Registros sísmicos utilizados


## Resultados de la simulación


# Resultados Experimentales


## Análisis de vibración libre

En la siguiente sección se presentan y analizan los resultados obtenidos durante las pruebas

de vibración libre, la cual consistió en una serie de impactos puntuales aplicados para

comprender su respuesta al movimiento. Se busca identificar las principales propiedades

dinámicas de cada estructura, edificio chato y edificio esbelto, además analizar

específicamente sus frecuencias naturales, periodos de vibración y razones de

amortiguamiento.


## Resultados de vibración libre del edificio chato

Para comprender el comportamiento del edificio chato en la prueba de vibración libre, se

muestra la Figura 6, donde se observa la historia de desplazamiento durante la prueba. En

la Figura 7 se muestra un acercamiento de la prueba con una duración de aproximadamente

de 3 segundos.


<!-- Página 31 -->


**Figura 6. Desplazamiento del edificio chato en función del tiempo durante la prueba de**

vibración libre.

Fuente: creación propia


**Figura 7. Zona de estudio de la historia de vibración libre del edificio chato.**

Fuente: creación propia

Para lograr observar las características dinámicas del modelo chato fue necesario

determinar sus periodos de oscilación, para ello se tomaron las mediciones del

desplazamiento en función del tiempo y se seleccionaron máximos y mínimos como se

observa en la Figura 8 y Figura 9


<!-- Página 32 -->


**Figura 8. Máximos de la zona de estudio de la historia de vibración libre del edificio chato.**

Fuente: creación propia


**Figura 9. Mínimos de la zona de estudio de la historia de vibración libre del edificio chato.**

Fuente: creación propia


<!-- Página 33 -->


**Figura 10. Datos para el cálculo del segundo periodo de oscilación del edificio chato.**

Fuente: creación propia

Se puede observar en las etiquetas de Figura 8 y Figura 9 que los valores más altos de cada

ciclo decrecen conforme el tiempo avanza, lo anterior se fundamenta en la suposición de

que la estructura amortigua las vibraciones libres que recibe, por lo que la función sinusoidal

disminuye su amplitud por la acción de una exponencial envolvente que relaciona el

amortiguamiento con la frecuencia circular natural.

Para conocer el modo fundamental de vibraciones se tomaron las mediciones de una

sección acotada de la historia del desplazamiento y se incorporaron a la Tabla 4, por otro

lado, para el cálculo del segundo periodo de oscilación se tomaron los datos de la Figura 10

que muestra aceleración-tiempo.


**Tabla 4. Cálculos de periodos de oscilación del edificio chato**

Primer modo

Segundo modo

k

Tiempo (s)

Periodo (s)

k

Tiempo (s)

Periodo (s)

T=2Δt

1

20,11

-

1

54,20

-

2

20,29

0,18

2

54,22

0,04


<!-- Página 34 -->

3

20.46

0,17

3

54,24

0,04

4

20,64

0,18

4

54,27

0,06

5

20,82

0,18

5

54,30

0.06

6

21,00

0,18

6

54,33

0,06

7

21,17

0,17

7

54,36

0,06

8

21,35

0,18

8

54,39

0,06

Promedio

0,177142857

Promedio

0,05428571

Desviación estándar

0,004879500

Desviación estándar

0,009759

Como se observa en la Tabla 4 los periodos que se obtuvieron para ambos modos presentan

valores estadísticamente alineados. Para el primer modo se obtuvo un periodo promedio

de 0,1771 segundos y una desviación estándar que representa aproximadamente un 2,75%

del periodo promedio, lo que indica una baja dispersión entre mediciones.

Para el segundo modo se determinó un periodo de 0,054 segundos valor considerablemente

menor que el del primer modo. Esto confirma que el segundo modo posee una frecuencia

mayor, como es esperable en este tipo de sistema. La desviación estándar obtenida fue de

aproximadamente 0,00976 s, equivalente a cerca de un 18 % del periodo promedio. Esta

mayor dispersión puede atribuirse a que el segundo modo se observa durante un intervalo

de tiempo más corto, con oscilaciones más rápidas y mayor dificultad para identificar con

precisión los picos en la señal de aceleración.

Con los datos obtenidos, se calcula el amortiguamiento con la formula del decremento

logarítmico que se muestra en la ecuación (15), para ello se utilizaron máximos y mínimos

que se encuentran en las figuras anteriores.


**Tabla 5. Determinación del amortiguamiento del edificio chato en la prueba de vibración**

libre, para el desplazamiento del modo fundamental

k

U_max

(mm)

U_min

(mm)

δ para

U_max

δ para

U_min

ξ para

U_max

ξ para U_min

1

1,572940

-1,789060

-

-

-

-

2

1,434230

-1,471420

0,09232

0,19546

0,01469

0,03109

3

1,400670

-1,363810

0,02368

0,07595

0,00377

0,01209

4

1,232600

-1,184710

0,12782

0,14078

0,02034

0,02240

5

1,109490

-1,067430

0,10523

0,10424

0,01674

0,01659

6

1,005250

-0,958998

0,09866

0,10712

0,01570

0,01705

7

0,915608

-0,860872

0,09340

0,10794

0,01486

0,01718

8

0,878857

-0,74592

0,04097

0,14780

0,00652

0,02352

Promedio

0,01323

0,01999

Desv.

Estándar

0,00589

0,00622

> Comentado [ACR9]: Acá sería valioso agregar la formula

vista en clase el 18/06

> Comentado [NU10R9]: Pongo la formula otra vez aunque

este arriba?


<!-- Página 35 -->

Como se observa en la Tabla 5, el amortiguamiento que se obtuvo a partir de los picos

máximos presenta un valor promedio de 1,323%, mientras que los mínimos tienen un valor

correspondiente a 1,999%. Ambos valores se encuentran dentro de un mismo orden de

magnitud, se observan diferencias apreciables.

Para los picos máximos, la desviación estándar fue de aproximadamente un 44,5% del valor

promedio, en el caso de los picos mínimos el valor es equivalente a un 31,1% de promedio.

Estos porcentajes muestran que existe una dispersión considerable en los valores

individuales de amortiguamiento.

La variabilidad que se observa se asocia con la dificultad para identificar las amplitudes de

los picos con exactitud y la influencia del impacto inicial sobre las primeras oscilaciones. En

particular, el primer valor de amortiguamiento calculado con los mínimos, igual a 0,03109

es mayor que los valores posteriores y contribuye a un aumento en el promedio y la

dispersión, estas pequeñas variaciones en las amplitudes producen cambios importantes en

el decremento logarítmico, debido a que se calcula mediante cociente entre picos

consecutivos.


**Figura 11. Aceleración en función del tiempo del edificio chato.**

Fuente: creación propia

En este gráfico de aceleración contra el tiempo para el edificio chato, se observan picos

iniciales altos que se amortiguan aceleradamente. Esta rápida disipación de energía, está

> Comentado [ACR11]: @NATALIA CAMPOS UMAÑA Esto

está bien? Sí es cociente?

> Comentado [NU12R11]: Si, está bien cociente


<!-- Página 36 -->

ligada a la rigidez del sistema, cuya baja flexibilidad impide oscilaciones prolongadas. Los

cortos periodos de la señal, señalan que el sistema posee un periodo fundamental bajo,

característico de estructuras de baja altura. En consecuencia, el modelo demuestra un

óptimo desempeño dinámico al estabilizarse y alcanzar el equilibrio rápidamente tras ser

sometido a una perturbación externa.


<!-- Página 37 -->


**Figura 12. Aceleración en función del tiempo del edificio chato acotado para FFT.**

Fuente: creación propia


<!-- Página 38 -->


**Figura 13. Resultado de la FFT para los datos acotados de la historia de aceleración del**

edificio chato.

Fuente: creación propia

Para poder calcular los periodos de oscilación del edificio, se necesita encontrar 2 “picos”

que sobresalgan en amplitud con respecto al resto, para eso se analizan solo ciertas partes

de toda la historia de aceleración (figura 11). Al acotar los datos de esta historia de 11900 a

14000, se obtiene la gráfica de la figura 13. Aquí se observan dos puntos que sobresalen,

por lo que se utilizarán para calcular los periodos de oscilación del edificio.

𝑇𝑓𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙= 𝑓−1

𝑇2° 𝑚𝑜𝑑𝑜= 𝑓−1

𝑇𝑓𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙= (5.664)−1

𝑇2° 𝑚𝑜𝑑𝑜= (18.0664)−1

𝑇𝑓𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙= 0.1766𝑠

𝑇2° 𝑚𝑜𝑑𝑜= 0.0554𝑠


## Resultados de vibración libre del edificio esbelto

De igual manera que se realizó un análisis de las principales propiedades dinámicas del

edificio chato se elaborara el mismo procedimiento para el edificio esbelto. Primero para

comprender la prueba de vibración libre se muestran las historias de desplazamiento y

aceleración del modelo estas se encuentran en la Figura 14 y Figura 15.


<!-- Página 39 -->


**Figura 14. Desplazamiento del edificio esbelto en función del tiempo para la prueba de**

vibración libre

Fuente: creación propia


**Figura 15. Aceleración del edificio esbelto en función del tiempo para la prueba de**

vibración libre

Fuente: creación propia

Como se observa en la Figura 14 y Figura 15 después de cada perturbación, la estructura

presenta una respuesta oscilatoria cuya amplitud disminuye progresivamente hasta


<!-- Página 40 -->

aproximarse nuevamente a su posición de equilibrio. Este comportamiento corresponde a

un sistema subamortiguado. Por otro lado, el amortiguamiento critico representa el valor

mínimo de amortiguamiento necesario para que la estructura regrese a su posición de

equilibrio sin presentar oscilaciones.

𝑐𝑐= 2√𝑘𝑚 (33)

𝑐𝑐≈ 𝑐 (34)

En la historia de desplazamiento se observan amplitudes mayores y oscilaciones más

prolongadas lo que evidencia la menor rigidez lateral del edificio esbelto. Por otra parte, la

historia de aceleración permite distinguir con mayor claridad los instantes donde se

aplicaron los impactos. El pico aislado que aparece al final del registro podría corresponder

a un nuevo impacto o a una perturbación externa por lo que no se tomara en cuenta para

el análisis.


**Figura 16. Acercamiento al gráfico de desplazamiento del edificio esbelto en función del**

tiempo para la prueba de vibración libre

Fuente: creación propia

En la Figura 16 se presenta un acercamiento realizado a la historia de desplazamiento, con

el propósito de identificar con mayor precisión los tiempos y amplitudes de los picos

utilizados, se calculó el periodo del primer modo de vibración. Asimismo, las amplitudes se

> Comentado [ACR13]: Acá sería valioso hablar del

amortiguamiento crítico

> Comentado [NU14R13]: Así?

> Comentado [ACR15R13]: A partir de la rígidez que calcula

debajo de la tabla 6, calcula coeficiente de amortiguamiento

crítico, es importante añadir que debido a la naturaleza del

proyecto y la simplificación de los modelos, coeficiente de

amortiguamiento y coeficiente de amortiguamiento crítico

son muy similares, formula34

> Comentado [ACR16]: Acá es valioso calcular la rigidez

según omega cuadrado, se despeja omega cuadrado = raíz de

k sobre m, m es 0.7kg

> Comentado [NU17R16]: Puedo calcular la rigidez debajo

de la tabla 6 donde ya tengo el valor del periodo

> Comentado [ACR18R16]: Sí, me gusta, es importante

hacerle énfasis porque ese dato se necesita para el resto del

análisis, se usa en el método matricial por ejemplo


<!-- Página 41 -->

utilizarán posteriormente para determinar la razón de amortiguamiento del modo

fundamental con el método de decremento logarítmico.


**Tabla 6. Cálculos de periodos de oscilación del modo fundamental del edificio esbelto.**

Primer modo

k

Tiempo (s)

Periodo (s)

1

2,46

-

2

3,16

0,70

3

3,88

0,72

4

4,58

0,70

5

5,31

0,73

6

6,01

0,70

7

6,73

0,72

8

7,45

0,72

Promedio

0,71285714

Desviación estándar

0,01253566

En la Tabla 6 se observan los periodos calculados para el modo fundamental del edificio

esbelto, estos se encuentran entre 0,70s y 0,73s lo que indica una variación reducida entre

mediciones, el periodo promedio es de 0,7129 segundos.

La desviación estándar es de 0,0125 segundos, representa aproximadamente un 1,76% del

periodo promedio. Este valor indica que existe una baja dispersión y una alta uniformidad

en los periodos es decir se muestra una respuesta oscilatoria estable.

A partir del periodo promedio obtenido, se calculó la frecuencia natural angular del primer

modo de vibración mediante la siguiente expresión.

𝜔𝑛= 2𝜋/𝑇 (35)

Se obtiene una frecuencia natural de 8,81 rad/s con la que se calcula la rigidez tomando la

masa como 0,7 kg y evaluando en la formula (2) despejada para la rigidez.

𝑘= 𝑚𝜔𝑛

2 (36)

La rigidez equivalente del sistema tiene un valor de 54,38 N/m para el primer modo de

vibración. A partir de esta rigidez se determinó el coeficiente de amortiguamiento crítico

evaluando en la ecuación (33), se obtiene un valor de 12,34 N.

El coeficiente de amortiguamiento critico representa el valor limite. Sin embargo, debido a

la naturaleza experimental del proyecto y la simplificación del edificio la respuesta crítica y

la respuesta subamortiguada con una razón cercana a la unidad pueden presentar

comportamientos similares.


<!-- Página 42 -->

A partir de las amplitudes correspondientes a los picos consecutivos del primer modo de

vibración, se calculó el decremento logarítmico del sistema. Se obtuvo un decremento

logarítmico de 0,08667 y una razón de amortiguamiento experimental de 0,01379,

equivalente aproximadamente al 1,38 %.

Al comparar ambos valores muestra que el coeficiente de amortiguamiento experimental

corresponde únicamente al 1,38 % del amortiguamiento crítico. Por lo tanto, la respuesta

del modelo no puede considerarse similar a la de un sistema críticamente amortiguado. El

edificio esbelto presenta un comportamiento subamortiguado, por la presencia de varias

oscilaciones decrecientes antes de alcanzar el equilibrio.

Para el segundo modo de vibración del edificio se tomaron datos de aceleración en función

del tiempo como se muestran en las Figura 17 por otro lado, el valor del periodo y la

recopilación de datos se resume en la Tabla 7.


**Figura 17. Gráfico de historia de vibración libre de la aceleración del edificio esbelto, para**

determinar el periodo del segundo modo.

Fuente: creación propia


**Tabla 7. Determinación del periodo de oscilación del segundo modo del edificio esbelto en**

la prueba de vibración libre con su historia de aceleración.

Segundo modo

k

Tiempo (s)

Periodo (s)

1

98,47

-


<!-- Página 43 -->

2

98,72

0,25

3

98,96

0,24

4

99,21

0,25

5

99,46

0,25

6

99,71

0,25

7

99,95

0,24

8

100,20

0,25

Promedio

0,247142857

Desviación estándar

0,004879500

Acerca de los datos obtenidos en la Tabla 7 los periodos obtenidos para el segundo modo

de vibración se encuentran entre 0,24 y 0,25 segundos que muestra una variación reducida

entre mediciones.

El periodo promedio que se obtuvo fue de 0,2471 segundos con una desviación estándar de

0,00488 segundos que es aproximadamente un 1,97% del periodo promedio es decir

presenta una baja dispersión y una uniformidad adecuada.

Si comparamos con el resultado del modo fundamental que es igual 0,713 s se muestra que

el segundo modo presenta un periodo menor y por lo tanto una mayor frecuencia, lo cual

es coherente con lo que se espera de un sistema con dos grados de libertad.

Para encontrar el amortiguamiento del edificio esbelto se utilizaron los datos de las gráficas

de desplazamiento en función de tiempo y cálculos basados en la fórmula de decremento

logarítmico, dichos datos se encuentran resumidos en la Tabla 8


**Tabla 8. Determinación del amortiguamiento del edificio esbelto en la prueba de vibración**

libre, para el desplazamiento del modo fundamental

k

U_max

(mm)

U_min

(mm)

δ para

U_max

δ para

U_min

ξ para

U_max

ξ para

U_min

1

10,247487 -9,774218

-

-

-

-

2

9,449894

-9,070283

0,08103

0,07474

0,0129

0,0119

3

8,625582

-8,271505

0,09127

0,09219

0,01452

0,01467

4

7,992231

-7,487227

0,07626

0,09962

0,01214

0,01585

5

7,290759

-6,828069

0,09186

0,09216

0,01462

0,01467

6

6,576336

-6,159973

0,10313

0,10297

0,01641

0,01639

7

6,074945

-5,544862

0,0793

0,1052

0,01262

0,01674

8

5,574558

-5,093264

0,08596

0,08495

0,01368

0,01352

Promedio 0,01384143

0,01482


<!-- Página 44 -->

Desv.

Estándar 0,00146988 0,0017065

La desviación estándar indica que existe una dispersión relativamente baja y uniforme con

valores de aproximadamente 10,62% en promedio para el máximo y 11,51% del promedio

para los mínimos.

Los resultados obtenidos de la Tabla 8 tiene como resultado el valor del amortiguamiento.

Para los máximos se obtuvo un valor de 0,0138 equivalente a 1,384%, mientras que para los

mínimos se obtuvo un valor promedio de 0,01482 correspondiente al 1,482%. Estos

resultados indican que el edificio esbelto posee un amortiguamiento bajo por lo que las

oscilaciones disminuyen gradualmente.


**Figura 18. Aceleración del tiempo del edificio esbelto acotado para FFT.**

Fuente: Creación propia

> Comentado [ACR19]: @NATALIA CAMPOS UMAÑA Vas

muy bien, ya ahí tiene casi todos los datos necesarios para

montar la ec. Fundamental de vibración libre. Falta algún

apartado donde para cada edificio encuentre las rigideces de

cada “losa” además de plantear explícitamente una eq que

modele el movimiento de cada edificio. Puede usar la

formula

> Comentado [ACR20R19]: La formula 7

> Comentado [NU21R19]: @DANIEL JOSUE QUIROS

AMPIEE

> Comentado [DA22R19]: Ya mañana lo subo, esq estoy

trabajandolo en una copia de word porque lo voy

modificando y para no cagar el documento original


<!-- Página 45 -->


**Figura 19. Resultado de la FFT para los datos acotados de la historia de aceleración del**

edificio esbelto.

Fuente: Creación propia

Como se hizo con el edificio chato, también se necesitan 2 “picos” para los cuales su

amplitud sea mayor en comparación al resto en la gráfica de la Transformada Rápida de

Fourier. En este caso, seleccionamos los datos de 0 a 8000 (figura 18). Aquí también se

observan dos puntos que sobresalen (figura 19), por lo que se utilizarán para calcular los

periodos de oscilación del edificio.

𝑇𝑓𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙= 𝑓−1

𝑇2° 𝑚𝑜𝑑𝑜= 𝑓−1

𝑇𝑓𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙= (1.416)−1

𝑇2° 𝑚𝑜𝑑𝑜= (4.05273)−1

𝑇𝑓𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙= 0.706𝑠

𝑇2° 𝑚𝑜𝑑𝑜= 0.2467𝑠


## Comparación de resultados de edificios en vibración libre

En esta sección, se realizará una comparativa del comportamiento de ambos edificios ante

la prueba de vibración libre. Esta comparación se hará mediante una inspección visual. A

continuación, en la figura 20, se muestra la superposición de las historias de desplazamiento

de ambos edificios.


<!-- Página 46 -->


**Figura 19. Desplazamiento del edificio chato y esbelto en función del tiempo.**

Fuente: Creación propia

Al comparar ambos edificios, se nota claramente cómo la altura cambia por completo su

comportamiento. El edificio chato, al ser más bajo, es mucho más rígido. Esto hace que sus

periodos de oscilación sean más cortos. Físicamente esta rigidez ayuda a que el movimiento

se frene casi de inmediato, disipando la energía del impacto de forma rápida y eficiente. Por

el contrario, el edificio alto es mucho más flexible por sus dimensiones, lo que hace que sus

oscilaciones sean más lentas y duren más tiempo antes de que la estructura pueda volver a

quedarse completamente quieta. Para observar mejor este comportamiento, se hizo un

acercamiento (figura 20).


<!-- Página 47 -->


**Figura 20. Acercamiento a la gráfica de desplazamiento del edificio chato y esbelto en**

función del tiempo.

Fuente: Creación propia

Como se puede observar, las amplitudes del desplazamiento son distintas para cada edificio.

Para el edificio esbelto se pueden apreciar desplazamientos cercanos a los 10 mm, mientras

que en el chato son mucho menores, rondando los 2 mm.


**Figura 21. Aceleración del edificio chato y esbelto en función del tiempo.**

Fuente: Creación propia


<!-- Página 48 -->

En la figura 21, se puede observar otra comparación importante, que es la superposición de

ondas de aceleración medidas para ambos edificios en vibración libre. En este caso se

observa que el comportamiento es inverso al que se observa en la figura 19. El edificio

esbelto tiene aceleraciones pico menores a 0.2g. Para el edificio chato en cambio, las

aceleraciones pico rondan los 0.6g.

Al ser el edificio chato más rígido y con periodo fundamental más corto, la estructura se

acelera con mayor rapidez para completar su ciclo de oscilación, por lo cual, según la teoría

y los datos obtenidos, se puede concluir que la aceleración de cada edificio es proporcional

a la frecuencia angular natural al cuadrado (𝜔𝑛

2)

A continuación, para comparar los periodos de oscilación de ambos edificios, se creó una

tabla comparativa (tabla 9). Este cuadro contiene los datos recopilados anteriormente en el

análisis de vibración libre para cada edificio.


**Tabla 9. Comparativa de los periodos de oscilación de ambos edificios para a prueba de**

vibración libre

Edificio

Método utilizado

Periodo de oscilación

Modo fundamental (s)

Segundo modo (s)

Esbelto

Nube de puntos

0.7128

0.2471

FFT

0.706

0.2467

Chato

Nube de puntos

0,1771

0,0543

FFT

0.1766

0.0554

Observando los datos de la tabla 9, ambos edificios tienen periodos de oscilación muy

distintos, tanto en el modo fundamental como en el segundo modo. Por ejemplo, para el

modo fundamental, el periodo de oscilación del edificio chato, representa en promedio un

24.96% del periodo de oscilación del edificio esbelto.


## Análisis de vibración forzada

La prueba de vibración forzada se llevó a cabo mediante la aplicación de movimientos

sinusoidales cuya frecuencia se fue incrementando progresivamente. Para ello se indujeron

una serie de oscilaciones sinusoidales por medio de una mesa vibratoria. En los siguientes

incisos se analiza la respuesta dinámica de ambos edificios en vibración forzada.


## Resultados de vibración forzada del edificio chato

Para comprender el comportamiento del edificio chato a la prueba de vibración forzada se

muestra la Figura 22 donde muestra la superposición de la historia de la aceleración y

desplazamiento y la Figura 23 que muestra la superposición de la historia únicamente del


<!-- Página 49 -->

desplazamiento. Para este edificio los valores a analizar son a partir de los 450 segundos

debido a que en los primeros segundos se estaba trabajado únicamente con el edificio

esbelto.


**Figura 22. Superposición de la historia de desplazamiento y aceleración del piso superior**

del edificio chato.

Fuente: creación propia


<!-- Página 50 -->


**Figura 23. Superposición de la historia de desplazamiento de la base y del piso superior del**

edificio bajo

Fuente: creación propia


**Figura 24. Acercamiento al desplazamiento y aceleración del edificio chato en función del**

tiempo.


<!-- Página 51 -->

Fuente: creación propia

Como se observa en la Figura 22, a partir de aproximadamente 600 s se observa un

crecimiento progresivo de ambas respuestas, hasta alcanzar sus valores máximos. Este

aumento considerable es compatible con un fenómeno de amplificación dinámica

(fenómeno de resonancia) producido cuando la frecuencia aplicada por la mesa vibratoria

se aproxima a una de las frecuencias naturales de la estructura.

Después de alcanzar la máxima amplificación, las amplitudes comienzan a disminuir, lo que

sugiere que la frecuencia de excitación se aleja de la condición de resonancia. Por tanto, la

historia completa permite identificar tres zonas, una de respuesta de baja amplitud antes

de la resonancia, otra de amplificación significativa cercana a la resonancia y por último una

reducción de la respuesta después de la resonancia.

En la Figura 18 se presenta un acercamiento al intervalo comprendido aproximadamente

entre 168 s y 188 s. En esta zona, las oscilaciones se mantienen alrededor de la posición de

equilibrio.


**Figura 25. Acercamiento de desplazamiento del edificio bajo y la base respecto al tiempo**

(antes de resonancia).

Fuente: creación propia


<!-- Página 52 -->


**Figura 26. Acercamiento de desplazamiento del edificio bajo y la base respecto al tiempo**

(en resonancia).

Fuente: creación propia

En la Figura 25, correspondiente a una condición previa a la resonancia, tanto la base como

el piso superior presentan una respuesta aproximadamente sinusoidal y estable. La

amplitud del movimiento de la base se mantiene cercana a 0,4 mm, mientras que el piso

superior alcanza aproximadamente 1 mm. Esto indica que, incluso antes de alcanzar la

resonancia, el edificio amplifica el movimiento impuesto por la mesa vibratoria, aunque no

se observa aumento en la amplitud.

En la Figura 26, la frecuencia aplicada se encuentra próxima a la frecuencia natural del

edificio chato. La amplitud del piso superior aumenta hasta valores cercanos a 9 mm,

mientras que el desplazamiento de la base continúa siendo pequeño. Por tanto, la gran

diferencia entre ambas amplitudes evidencia una amplificación dinámica considerable y

confirma la presencia del fenómeno de resonancia.

La comparación entre ambas figuras permite observar que el incremento de la respuesta no

se debe a un aumento importante del desplazamiento impuesto por la mesa vibratoria, sino

a la cercanía entre la frecuencia de excitación y la frecuencia natural del edificio.


<!-- Página 53 -->


**Figura 27. Ejemplo del método utilizado para obtener el tiempo de retraso.**

Fuente: creación propia

Con la Figura 27 se ilustra el método para la obtención del tiempo de retraso de la respuesta

de desplazamiento del edificio (rojo) respecto al desplazamiento de la base (azul), el cual se

utilizó para calcular el ángulo de fase experimental.


**Tabla 9. Resumen de datos del ángulo experimental calculado del edificio chato.**

Frecuencia

aplicada (Hz)

Tiempo de

retraso (s)

ωp experimental

(rad/s)

φ de fase

experimental

(rad)

φ de fase

experimental (°)

5,4

0,0099

33,9292

0,3359

19,24

5,6

0,0099

35,1858

0,3491

20

5,8

0,0099

36,4425

0,3621

20,75

6

0,0101

37,6991

0,3808

21,82

6,4

0,0099

40,2124

0,3989

22,86

6,6

0,0101

41,469

0,4189

24

6,8

0,01

42,7257

0,426

24,41

7

0,0101

43,9823

0,4425

25,35

7,2

0,0099

45,2389

0,4488

25,71

7,4

0,01

46,4956

0,4654

26,67

7,6

0,0099

47,7522

0,4739

27,15

7,8

0,0099

49,0088

0,4871

27,91


<!-- Página 54 -->

8

0,02

50,2655

1,0045

57,55

8,2

0,02

51,5221

1,03

59,02

8,4

0,0298

52,7788

1,5708

90

8,6

0,0298

54,0354

1,6111

92,31

8,8

0,0299

55,292

1,6535

94,74

9

0,0303

56,5487

1,7136

98,18

9,2

0,0406

57,8053

2,3488

134,58

9,4

0,0405

59,0619

2,3936

137,14

9,6

0,0521

60,3186

3,1416

180

En la Tabla 9 se presentan los valores experimentales del ángulo de fase entre el

desplazamiento de la base y la respuesta del piso superior del edificio chato para las

diferentes frecuencias aplicadas

A partir de 8,0 Hz se observa un aumento importante en el tiempo de retraso, que pasa de

aproximadamente 0,01 s a 0,02 s. Esto produce un incremento del ángulo de fase hasta

57,55°. Posteriormente, para una frecuencia de 8,4 Hz, el ángulo de fase es cercano a 90° y

finalmente, a 9,6 Hz se calcula un ángulo cercano a 180°, lo que indica que el piso superior

y la base presentan movimientos prácticamente opuestos en determinados instantes del

ciclo. Esta evolución del ángulo, desde valores reducidos hasta aproximarse a 180°,

concuerda cualitativamente con la respuesta de un sistema amortiguado al incrementarse

la frecuencia de excitación.


**Figura 28. Ejemplo de la variación del ángulo respecto a la frecuencia del edificio bajo.**

Fuente: creación propia


<!-- Página 55 -->

a) Análisis de amplitud estacionaria

En la Tabla 10 se presentan los datos de amplitud estacionaria para cada frecuencia

analizada del edificio bajo. Los datos incluyen la frecuencia aplicada, frecuencia

experimental, amplitud, promedio de las amplitudes y la desviación estándar.


**Tabla 10. Resumen de datos de amplitud estacionaria medida del edificio bajo**

Frecuencia

aplicada (Hz)

Frecuencia

experimental

(Hz)

Amplitud

positiva

(mm)

Amplitud

negativa, valor

absoluto (mm)

Promedio

Desviación

estándar

5,4

3,5923

0,8396

0,936

0,8878

0,0682

5,6

3,7879

0,881

1,0075

0,9442

0,0895

5,8

3,8942

0,9028

1,0336

0,9682

0,0924

6

3,9928

0,9086

1,0736

0,9911

0,1167

6,4

4,0928

0,9896

1,1309

1,0602

0,0999

6,6

4,2235

1,1397

1,197

1,1683

0,0405

6,8

4,2885

1,2223

1,2263

1,2243

0,0029

7

4,586

1,4913

1,5798

1,5356

0,0626

7,2

4,7945

1,8212

1,9427

1,8819

0,0859

7,4

4,9932

2,551

2,4898

2,5204

0,0433

7,6

5,0883

3,0301

3,0581

3,0441

0,0198

7,8

5,1882

3,8622

3,9396

3,9009

0,0548

8

5,3362

6,0614

5,9878

6,0246

0,052

8,2

5,4953

7,8301

7,7956

7,8129

0,0244

8,4

5,5936

6,0442

5,9165

5,9803

0,0903

8,6

5,7336

4,2226

4,1707

4,1967

0,0367

8,8

5,8824

3,1097

3,1025

3,1061

0,0051

9

6,0914

2,4086

2,3586

2,3836

0,0353

9,2

6,3857

1,7126

1,7609

1,7367

0,0341

9,4

6,7816

1,2928

1,257

1,2749

0,0253

9,6

7,4913

0,9492

0,8853

0,9172

0,0452

b) Curva de transmisibilidad

La curva de transmisibilidad de desplazamiento para los datos experimentales del edificio

bajo se encuentra en la Figura


<!-- Página 56 -->


**Figura 29. Curva de transmisibilidad de desplazamiento experimental para el edificio bajo**

Fuente: creación propia

c) Método de ancho de banda


**Figura 30. Datos y gráfica del método de ancho de banda para el edificio bajo**

Fuente: creación propia


<!-- Página 57 -->

La Figura 30 muestra los valores utilizados para el método de ancho de banda, que

consiste en dividir la amplificación máxima de la curva de FAD entre la raíz cuadrada

de dos, con esto se obtiene una recta horizontal a una altura “y”.

𝐴𝑚𝑝𝑙𝑖𝑡𝑢𝑑  𝐹𝐴𝐷 𝑚á𝑥  =  20

𝑅𝑒𝑐𝑡𝑎 𝑦  =

20

√2 = 14,142 (37)

La recta horizontal interseca a la curva en dos puntos que son tomados como

frecuencia 1 y 2 en la siguiente ecuación:

𝜉=

𝑓2−𝑓1

2𝑓𝑛 (38)

Sustituyendo los datos de las frecuencias y tomando la fn = 1 se obtiene:

𝜉=

1,0241−0,9740

2

= 0,0250

ξ = 2,50%

d) Amortiguamiento mediante prueba de resonancia

El amortiguamiento del sistema se obtiene utilizando la formula (11) con condición

de resonancia r = 1 se reduce a la ecuación (12)

𝜉=

1

2 ⋅20 = 0,025

e) Función teórica de la curva de transmisibilidad

En la Figura 31 se presenta la comparación entre la curva teórica del factor de

amplificación dinámica y los valores obtenidos experimentalmente para el edificio

chato. La curva teórica se determinó mediante la ecuación (11), utilizando la razón

de amortiguamiento calculada previamente a partir de la prueba de resonancia, cuyo

valor fue de aproximadamente a un 2,50 %.


<!-- Página 58 -->


**Figura 31. Comparación entre las curvas teórica y experimental del factor de amplificación**

dinámica del edificio chato.

Fuente: creación propia

Como se observa en la Figura 31, tanto la curva teórica como los puntos experimentales

presentan un incremento considerable del factor de amplificación cuando la razón de

frecuencias se aproxima a la unidad. La máxima amplificación experimental es cercana a 20,

lo que concuerda con el comportamiento esperado para un sistema con bajo

amortiguamiento.

f) Función del ángulo de fase experimental y teórico

En la Figura 32 se presenta la comparación entre la curva teórica del ángulo de fase

y los valores experimentales para el edificio chato. Se observa que para razones de

frecuencia menores a 1 el desface es pequeño lo que indica que la respuesta del piso

superior ocurre aproximadamente en fase con el movimiento de la base.


<!-- Página 59 -->


**Figura 32. Comparativa de la variación del ángulo de fase teórico y experimental según las**

frecuencias inducidas en la base para el edificio bajo

Fuente: creación propia

g) Comparación de frecuencias naturales


**Tabla 11. Resumen comparativo de período y frecuencia naturales obtenidos mediante tres**

diferentes métodos para el edificio bajo

Método utilizado

Periodo natural (s)

Frecuencia natural (Hz)

Lectura directa de la curva de

vibración libre

0,1771

5,645

Transformada rápida de Fourier

0,1766

5,664

Curva de transmisibilidad

0,182

5,495

Los resultados obtenidos mediante los tres métodos presentan valores cercanos entre sí. La

lectura directa de la curva de vibración libre produjo una frecuencia natural de

aproximadamente 5,645 Hz, mientras que mediante la transformada rápida de Fourier se

obtuvo un valor de 5,664 Hz. La diferencia entre estos dos resultados es reducida, lo que

evidencia consistencia entre el análisis realizado en el dominio del tiempo y el análisis en el

dominio de la frecuencia.


<!-- Página 60 -->

Por otra parte, mediante la curva de transmisibilidad se obtuvo una frecuencia aproximada

de 5,495 Hz, ligeramente menor que las determinadas mediante vibración libre. Esta

diferencia puede estar asociada con el amortiguamiento del sistema, la resolución utilizada

para el barrido de frecuencias o la medición de las amplitudes.

h) Comparación de los amortiguamientos


**Tabla 12. Resumen comparativo del amortiguamiento obtenido mediante tres diferentes**

métodos para el edificio bajo

Método utilizado

Amortiguamiento

Amortiguamiento (%)

Decremento logarítmico

0,01661

1,661

Método de ancho de banda

0,025

2,5

Prueba de resonancia

0,02503

2,503

Los valores obtenidos mediante el método de ancho de banda y la prueba de resonancia

son prácticamente iguales, con razones de amortiguamiento cercanas a 0,025. Esta

semejanza es coherente, debido a que ambos procedimientos se basan en la respuesta del

edificio durante la prueba de vibración forzada

El amortiguamiento obtenido mediante decremento logarítmico es menor, con un valor

aproximado de 0,0166. Esta diferencia puede relacionarse con que el decremento

logarítmico se determina a partir de una prueba de vibración libre. Además, la identificación

de los picos, el ruido experimental y la selección de los puntos de la curva pueden influir en

los resultados.

A pesar de las diferencias, los encuentran en un mismo orden de magnitud. Por lo tanto, los

tres métodos permiten clasificar al edificio chato como un sistema subamortiguado, con una

razón de amortiguamiento aproximada entre 1,7 % y 2,5 %.


## Resultados de vibración forzada del edificio esbelto

Con el propósito de caracterizar la respuesta dinámica del edificio esbelto ante

excitaciones armónicas, se realizó una prueba de vibración forzada utilizando la mesa

vibratoria del laboratorio. Durante el ensayo se mantuvo una amplitud de excitación en la

base de aproximadamente 0,5 mm, mientras que la frecuencia fue incrementada

progresivamente para identificar las condiciones de resonancia y determinar los parámetros

dinámicos del sistema.

La respuesta obtenida permitió identificar claramente dos frecuencias de resonancia

asociadas a los modos predominantes de vibración del edificio. La primera resonancia se

presentó alrededor de 1,4 Hz, alcanzando una amplitud máxima aproximada de 15 mm,

mientras que la segunda resonancia se registró cerca de 4,0 Hz con una amplitud máxima

de aproximadamente 4 mm. Estos resultados evidencian la presencia de múltiples modos


<!-- Página 61 -->

de vibración y confirman el comportamiento dinámico esperado para una estructura de dos

grados de libertad.


**Figura 33. Superposición de la historia de desplazamiento y aceleración del piso superior**

del edificio esbelto.

Fuente: creación propia

En la Figura 33 se observa la historia completa de desplazamiento y aceleración del edificio

esbelto durante la prueba de vibración forzada. La señal muestra un incremento importante

de la respuesta en la zona de resonancia principal y, posteriormente, una segunda

amplificación de menor magnitud asociada al segundo modo. Este comportamiento permite

distinguir claramente las regiones donde la frecuencia aplicada por la mesa se aproxima a

las frecuencias naturales del modelo.


<!-- Página 62 -->


**Figura 34. Superposición de la historia de desplazamiento de la base y del piso superior del**

edificio esbelto.

Fuente: creación propia

La Figura 34 permite comparar directamente el movimiento impuesto por la base con

la respuesta del piso superior. Se observa que la amplitud de la base permanece reducida

durante toda la prueba, mientras que el piso superior presenta amplificaciones importantes

cuando se alcanza la resonancia. Por lo tanto, el incremento de desplazamiento no se debe

a un aumento en la amplitud de la mesa vibratoria, sino a la cercanía entre la frecuencia

aplicada y las frecuencias naturales del edificio.

a) Comportamiento antes de la resonancia


**Figura 35. Respuesta del edificio esbelto antes de la resonancia.**


<!-- Página 63 -->

Fuente: creación propia

En la Figura 35 se muestra una zona previa a la resonancia. En esta etapa se observa

que la amplitud de respuesta permanece relativamente reducida y cercana a la amplitud

impuesta por la mesa vibratoria. La frecuencia de excitación aún se encuentra alejada de la

frecuencia natural del sistema, por lo que la transferencia de energía entre la base y la

estructura es limitada. Como consecuencia, el desplazamiento del piso superior presenta

una amplificación moderada y un desfase reducido respecto al movimiento de la base.

b) Comportamiento durante la resonancia


**Figura 36. Respuesta del edificio esbelto durante la resonancia.**

Fuente: creación propia

La Figura 36 presenta la respuesta registrada cuando la frecuencia de excitación

coincide con la frecuencia natural predominante del sistema. Se aprecia un incremento

significativo en la amplitud de vibración, alcanzando desplazamientos cercanos a 15 mm en

el piso superior. Considerando que la amplitud de excitación aplicada en la base fue de

únicamente 0,5 mm, se obtiene una amplificación dinámica cercana a treinta veces el

desplazamiento impuesto.

Este comportamiento constituye una evidencia clara del fenómeno de resonancia,

donde la frecuencia de excitación coincide con la frecuencia natural del sistema y se produce

una transferencia máxima de energía hacia la estructura. Además, la frecuencia de

resonancia experimental obtenida durante esta prueba corresponde aproximadamente a

1,4 Hz, valor que coincide con la frecuencia natural determinada previamente mediante la

prueba de vibración libre. Esta concordancia confirma la consistencia de los resultados

experimentales y valida los procedimientos empleados para la caracterización dinámica del

modelo.


<!-- Página 64 -->

c) Comportamiento después de la resonancia


**Figura 37. Respuesta del edificio esbelto después de la resonancia.**

Fuente: creación propia

Al continuar incrementando la frecuencia de excitación se observa una disminución

progresiva de la amplitud de vibración, como se aprecia en la Figura 37. Esto ocurre debido

a que la frecuencia aplicada se aleja de la frecuencia natural del sistema, reduciendo la

transferencia de energía entre la base y la estructura. Como resultado, los desplazamientos

retornan gradualmente a valores similares a los observados antes de la resonancia.

d) Análisis de amplitud estacionaria


**Figura 38. Curva experimental de amplitud estacionaria del edificio esbelto.**


<!-- Página 65 -->

Fuente: creación propia

La Figura 38 presenta la amplitud estacionaria obtenida para distintas frecuencias

evaluadas durante el ensayo. La curva evidencia un incremento progresivo de la amplitud

conforme la frecuencia de excitación se aproxima a la frecuencia natural fundamental. Para

frecuencias inferiores a 1,1 Hz las amplitudes permanecen cercanas a 1 mm; sin embargo, a

partir de 1,2 Hz se observa un crecimiento acelerado que culmina con una amplitud máxima

de aproximadamente 15 mm a 1,4 Hz. Posteriormente la respuesta disminuye rápidamente

conforme la frecuencia continúa aumentando.

Asimismo, se identificó una segunda resonancia alrededor de 4,0 Hz, donde se registró

una amplitud máxima cercana a 4 mm. Aunque esta amplificación es considerablemente

menor que la observada en el primer modo, confirma la existencia de un segundo modo de

vibración que participa en la respuesta dinámica del sistema.


**Tabla 13. Resumen de amplitudes máximas y transmisibilidad estimada para el edificio**

esbelto.

Frecuencia aplicada (Hz)

Amplitud máxima (mm)

FAD = A/A_base

0,7

1,0

2,0

0,8

0,9

1,8

0,9

0,8

1,6

1,0

1,0

2,0

1,1

1,3

2,6

1,2

2,0

4,0

1,25

2,7

5,4

1,3

3,8

7,6

1,35

8,0

16,0

1,4

15,0

30,0

1,45

7,0

14,0

1,5

3,7

7,4

1,6

1,5

3,0

1,7

1,2

2,4

2,0

0,5

1,0

3,0

0,3

0,6

3,3

0,3

0,6

3,6

0,4

0,8

3,8

0,9

1,8

3,9

1,4

2,8

4,0

4,0

8,0

4,1

1,8

3,6

4,2

0,6

1,2

4,3

0,5

1,0


<!-- Página 66 -->

En la Tabla 13 se resumen las amplitudes máximas registradas para el edificio esbelto.

Se utilizó la amplitud de base de 0,5 mm para estimar el factor de amplificación dinámica

de cada punto. El máximo valor se obtiene a 1,4 Hz, donde el FAD alcanza aproximadamente

30. Para la segunda resonancia, a 4,0 Hz, el FAD alcanza un valor aproximado de 8,

confirmando que el segundo modo tiene una participación menor en términos de

desplazamiento global.

e) Curva de transmisibilidad


**Figura 39. Curva de transmisibilidad de desplazamiento en función de la frecuencia.**

Fuente: creación propia

La relación entre la amplitud de respuesta y la amplitud de excitación se representa

mediante la curva de transmisibilidad mostrada en la Figura 39. Esta curva presenta un pico

pronunciado alrededor de la frecuencia natural fundamental del sistema. El factor de

amplificación dinámica máximo obtenido experimentalmente es cercano a 30, lo que indica

una respuesta altamente sensible cuando la frecuencia de excitación coincide con la

frecuencia natural del edificio.

La forma de la curva es coherente con la respuesta esperada de un sistema

subamortiguado. Antes de la resonancia, el factor de amplificación crece gradualmente; en

la resonancia alcanza su valor máximo; y después de la resonancia disminuye conforme la

frecuencia aplicada se aleja de la frecuencia natural.

f) Determinación del amortiguamiento mediante el método de ancho de banda


<!-- Página 67 -->


**Figura 40. Aplicación del método de ancho de banda sobre la curva de transmisibilidad.**

Fuente: creación propia

La Figura 40 muestra la aplicación del método de ancho de banda para estimar la razón

de amortiguamiento del sistema. El procedimiento consiste en identificar las frecuencias

correspondientes a los puntos donde la amplitud alcanza un valor igual a la amplitud

máxima dividida entre la raíz cuadrada de dos. A partir de estas frecuencias se calcula la

razón de amortiguamiento experimental mediante la expresión:

ξ = (f₂ − f₁) / (2 fₙ)

Mediante este procedimiento se obtuvo una razón de amortiguamiento aproximada de:

ξ = 0,021 = 2,10 %

Este resultado confirma que el edificio esbelto se comporta como un sistema

ligeramente amortiguado, condición típica en modelos estructurales construidos con

madera balsa y con uniones adhesivas.

g) Amortiguamiento mediante prueba de resonancia

De forma complementaria, el amortiguamiento también se estimó utilizando la

amplitud máxima obtenida en resonancia. En esta prueba se registró una amplitud de base

cercana a 0,5 mm y una amplitud máxima de respuesta aproximada de 15 mm para la

primera resonancia. Con estos valores se empleó la relación aproximada:

ξ = A_base / (2 A_res)

ξ = 0,5 / (2 · 15) = 0,0167 = 1,67 %


<!-- Página 68 -->

El valor obtenido mediante resonancia es ligeramente menor que el calculado mediante

el método de ancho de banda. Esta diferencia es esperable, ya que ambos métodos

dependen de la lectura experimental de amplitudes y de la forma en que se identifica la

condición exacta de resonancia.

h) Comparación entre el FAD experimental y teórico


**Figura 41. Comparación entre el FAD experimental y el FAD teórico.**

Fuente: creación propia

La Figura 41 muestra la comparación entre la curva experimental del factor de

amplificación dinámica y la curva teórica obtenida a partir del amortiguamiento calculado.

Se observa una buena concordancia entre ambas curvas, especialmente en las cercanías de

la resonancia. La posición del pico de amplificación y la tendencia general de la respuesta

presentan una correspondencia satisfactoria, lo que indica que el modelo teórico representa

adecuadamente el comportamiento dinámico del edificio.

Las diferencias observadas pueden atribuirse a incertidumbres experimentales,

variaciones en las propiedades reales de la madera balsa, pequeñas imperfecciones en las

uniones y simplificaciones inherentes al modelo matemático empleado. Aun así, la cercanía

entre la curva teórica y los datos experimentales confirma que la respuesta del edificio

puede aproximarse adecuadamente mediante la teoría de vibraciones forzadas para

sistemas subamortiguados.

i) Análisis del ángulo de fase


<!-- Página 69 -->


**Figura 42. Ejemplo del método utilizado para obtener el tiempo de retraso entre la base y**

el piso superior.

Fuente: creación propia

Para determinar el ángulo de fase experimental se utilizó el tiempo de retraso entre el

desplazamiento de la base y el desplazamiento del piso superior. En la Figura 42 se muestra

un ejemplo del procedimiento empleado para medir dicho retraso. Con el valor de tiempo

obtenido y la frecuencia angular de excitación se calculó el desfase correspondiente.


**Figura 43. Variación del ángulo de fase respecto a la frecuencia del edificio esbelto.**

Fuente: creación propia

La Figura 43 muestra la variación general del ángulo de fase conforme cambia la

frecuencia aplicada. Para frecuencias bajas, el edificio se mueve casi en fase con la base. Al


<!-- Página 70 -->

aproximarse a la resonancia, el ángulo aumenta rápidamente, y posteriormente tiende a

valores cercanos a 180 grados.


**Figura 44. Comparación entre el ángulo de fase teórico y experimental.**

Fuente: creación propia

En la Figura 44 se presenta la comparación entre los valores experimentales y teóricos

del ángulo de fase. Para frecuencias bajas, el movimiento del edificio permanece

prácticamente en fase con la excitación aplicada. Conforme la frecuencia se aproxima a la

resonancia, el desfase aumenta progresivamente hasta alcanzar valores cercanos a 90

grados, comportamiento característico de sistemas sometidos a vibración forzada.


**Figura 45. Curva de ángulo de fase experimental y teórico.**

Fuente: creación propia


<!-- Página 71 -->

La misma tendencia se observa en la Figura 45, donde se representa nuevamente la

evolución del ángulo de fase a partir de los resultados experimentales y teóricos. La similitud

entre ambas curvas demuestra que la teoría de vibraciones forzadas describe

adecuadamente el comportamiento del sistema, reproduciendo de forma satisfactoria la

evolución del desfase a lo largo del rango de frecuencias analizado.

j) Comparación de frecuencias naturales


**Tabla 14. Comparación de frecuencias naturales obtenidas mediante distintos métodos**

para el edificio esbelto.

Método utilizado

Periodo natural (s)

Frecuencia natural (Hz)

Lectura directa de vibración

libre

0,713

1,40

Transformada rápida de

Fourier

0,706

1,42

Curva de transmisibilidad

0,714

1,40

Como se observa en la Tabla 14, los tres métodos utilizados producen valores muy

cercanos para la frecuencia natural fundamental del edificio esbelto. La lectura directa de la

prueba de vibración libre proporciona una frecuencia aproximada de 1,40 Hz, la FFT entrega

un valor cercano a 1,42 Hz, y la curva de transmisibilidad identifica la resonancia principal

alrededor de 1,40 Hz. Esta concordancia valida los resultados obtenidos y confirma que el

pico observado en vibración forzada corresponde al modo fundamental del sistema.

k) Comparación de los métodos de amortiguamiento


**Tabla 15. Comparación de razones de amortiguamiento obtenidas para el edificio esbelto.**

Método utilizado

Amortiguamiento

Amortiguamiento (%)

Decremento logarítmico

0,0143

1,43 %

Método de ancho de

banda

0,0210

2,10 %

Prueba de resonancia

0,0167

1,67 %

En la Tabla 15 se comparan los valores de amortiguamiento obtenidos mediante los

distintos procedimientos. El método de decremento logarítmico, calculado a partir de la

prueba de vibración libre, produjo una razón de amortiguamiento cercana a 1,43 %. Por otro

lado, el método de ancho de banda arrojó un valor de 2,10 %, mientras que el método de

resonancia produjo un valor aproximado de 1,67 %.

Los tres resultados se encuentran dentro de un mismo orden de magnitud, por lo que

se puede afirmar que el edificio esbelto presenta un comportamiento claramente


<!-- Página 72 -->

subamortiguado. Las diferencias entre métodos pueden atribuirse a la sensibilidad de cada

procedimiento frente a pequeñas variaciones en las amplitudes medidas, al ruido

experimental y a la dificultad de identificar con exactitud el punto de resonancia.

l) Síntesis del comportamiento observado

En términos generales, los resultados de vibración forzada confirman las conclusiones

obtenidas durante las pruebas de vibración libre. El edificio esbelto presenta una frecuencia

natural baja, desplazamientos máximos elevados y una alta susceptibilidad a fenómenos de

resonancia. La máxima amplificación se produjo a 1,4 Hz, frecuencia que coincide con el

modo fundamental previamente identificado. Además, la presencia de una segunda

resonancia alrededor de 4,0 Hz confirma la participación del segundo modo de vibración.

La elevada amplificación observada en la resonancia principal se relaciona

directamente con la menor rigidez lateral del edificio esbelto y con su mayor altura. Por

tanto, este modelo representa una estructura flexible, con periodos largos y

desplazamientos laterales significativos bajo excitaciones cercanas a su frecuencia natural.

Estos resultados son coherentes con el comportamiento esperado para sistemas

estructurales esbeltos sometidos a cargas dinámicas armónicas.


<!-- Página 73 -->


# Comparación Y Análisis De Resultados


## Comparación de frecuencias naturales

En la Tabla 16 se presenta un resumen comparativo de los periodos y frecuencias naturales

obtenidos mediante tres métodos diferentes para el edificio esbelto. Los métodos

considerados corresponden a la lectura directa de la curva de vibración libre, la

Transformada Rápida de Fourier y la curva de transmisibilidad obtenida durante la prueba

de vibración forzada.


**Tabla 16. Resumen comparativo de periodo y frecuencia natural obtenidos mediante tres**

métodos diferentes para el edificio esbelto.

Método utilizado

Periodo natural (s) Frecuencia

natural

(Hz)

Lectura directa de la curva de vibración libre 0,7128

1,403

Transformada Rápida de Fourier

0,7060

1,416

Curva de transmisibilidad

0,7143

1,400

Los resultados obtenidos mediante los tres métodos presentan valores muy cercanos entre

sí. La lectura directa de la curva de vibración libre produjo un periodo natural de

aproximadamente 0,7128 s, equivalente a una frecuencia natural de 1,403 Hz. Por otra

parte, mediante la Transformada Rápida de Fourier se obtuvo un periodo de 0,7060 s,

correspondiente a una frecuencia de 1,416 Hz.

La curva de transmisibilidad, obtenida a partir de la prueba de vibración forzada, permitió

identificar la resonancia principal del edificio esbelto alrededor de 1,4 Hz, lo que

corresponde a un periodo natural aproximado de 0,7143 s. Este valor coincide de forma

satisfactoria con los resultados obtenidos mediante vibración libre y FFT.


<!-- Página 74 -->

La cercanía entre los tres valores confirma la consistencia de los procedimientos

experimentales utilizados para identificar la frecuencia natural fundamental del edificio

esbelto. Además, permite validar que la máxima amplificación observada durante la prueba

de vibración forzada corresponde efectivamente al primer modo de vibración del sistema.

Las pequeñas diferencias entre los métodos pueden atribuirse a la resolución del barrido de

frecuencias, a la precisión con la que se identificaron los picos de desplazamiento y a la

presencia de ruido experimental en las mediciones. Sin embargo, estas variaciones son

reducidas y no modifican la interpretación general del comportamiento dinámico del

edificio.


## Comparación de los amortiguamientos

En la Tabla 17 se presenta un resumen comparativo de los valores de amortiguamiento

obtenidos mediante tres métodos diferentes para el edificio esbelto: decremento

logarítmico, método de ancho de banda y prueba de resonancia.


**Tabla 17. Resumen comparativo del amortiguamiento obtenido mediante tres métodos**

diferentes para el edificio esbelto.

Método utilizado

Amortiguamiento

Amortiguamiento (%)

Decremento logarítmico

0,01433

1,433

Método de ancho de banda

0,02100

2,100

Prueba de resonancia

0,01670

1,670

Como se observa en la Tabla 17, los valores de amortiguamiento obtenidos mediante los

tres métodos se encuentran dentro de un mismo orden de magnitud. El decremento

logarítmico produjo un amortiguamiento aproximado de 0,01433, equivalente a 1,433 %.

Este valor proviene de la prueba de vibración libre, por lo que representa la disipación de

energía del edificio después de una perturbación inicial, sin excitación externa continua.


<!-- Página 75 -->

Por medio del método de ancho de banda se obtuvo un amortiguamiento de

aproximadamente 0,02100, equivalente a 2,10 %. Este valor es ligeramente mayor que el

obtenido por decremento logarítmico, lo cual puede deberse a que el método se basa

directamente en la forma de la curva de transmisibilidad alrededor de la resonancia. Por

esta razón, es sensible a la amplitud máxima registrada y a las frecuencias seleccionadas a

ambos lados del pico de resonancia.

Finalmente, mediante la prueba de resonancia se obtuvo un amortiguamiento aproximado

de 0,01670, correspondiente a 1,67 %. Este resultado se encuentra entre los valores

obtenidos por decremento logarítmico y por ancho de banda, lo que indica una buena

coherencia entre los métodos experimentales aplicados.

Las diferencias entre los valores calculados pueden asociarse con la sensibilidad propia de

cada procedimiento, la precisión de las mediciones de amplitud, la resolución del barrido

de frecuencias y las pequeñas variaciones constructivas del modelo físico. Además, al

tratarse de un edificio esbelto, los desplazamientos durante la resonancia fueron

considerablemente mayores, por lo que pequeñas variaciones en la lectura de amplitudes

pueden generar cambios apreciables en el cálculo del amortiguamiento.

A pesar de estas diferencias, los tres métodos permiten clasificar al edificio esbelto como

un sistema subamortiguado. Esto concuerda con las observaciones experimentales

realizadas tanto en vibración libre como en vibración forzada, donde la estructura presentó

oscilaciones prolongadas y una amplificación significativa al aproximarse a su frecuencia

natural.

En términos generales, la comparación de resultados confirma que el edificio esbelto posee

una frecuencia natural fundamental cercana a 1,4 Hz y un amortiguamiento bajo,

comprendido aproximadamente entre 1,4 % y 2,1 %. Estos resultados son coherentes con

su baja rigidez lateral, su mayor altura y su mayor susceptibilidad al fenómeno de

resonancia.


# Conclusiones Y Recomendaciones


# Referencias Bibliográficas


<!-- Página 76 -->

Las referencias se listan a continuación en orden de primera aparición en el texto, conforme

al estándar de citación numérica IEEE.

- [1] A. K. Chopra, Dynamics of Structures: Theory and Applications to Earthquake

Engineering, 5.ª ed. Hoboken, NJ, EE. UU.: Pearson, 2020.

- [2] American Society of Civil Engineers, Minimum Design Loads and Associated Criteria for

Buildings and Other Structures (ASCE 7-22). Reston, VA, EE. UU.: ASCE, 2022.

- [3] N. M. Newmark y E. Rosenblueth, Fundamentals of Earthquake Engineering. Englewood

Cliffs, NJ, EE. UU.: Prentice-Hall, 1971.

- [4] S. S. Rao, Mechanical Vibrations, 6.ª ed. Hoboken, NJ, EE. UU.: Pearson, 2018.

- [5] R. W. Clough y J. Penzien, Dynamics of Structures, 3.ª ed. Berkeley, CA, EE. UU.: Computers

& Structures, 2003.

- [6] R. R. Craig y A. J. Kurdila, Fundamentals of Structural Dynamics, 2.ª ed. Hoboken, NJ, EE.

UU.: Wiley, 2006.

- [7] D. J. Inman, Engineering Vibration, 4.ª ed. Upper Saddle River, NJ, EE. UU.: Pearson, 2014.

- [8] M. Paz y Y. H. Kim, Structural Dynamics: Theory and Computation, 6.ª ed. New York, NY,

EE. UU.: Springer, 2019.

- [9] Y.-C. Liu, “Proyecto,” IC-0502 Mecánica II, I Ciclo Lectivo de 2026, Escuela de Ingeniería

Civil, Universidad de Costa Rica, San José, Costa Rica, 2026.

- [10] D. E. Kretschmann, “Mechanical properties of wood,” in Wood Handbook—Wood as an

Engineering Material, R. J. Ross, Ed. Madison, WI, EE. UU.: USDA Forest Service, Forest

Products Laboratory, 2010, ch. 5.


# Apéndices


---

## Nota para uso como contexto en Claude

Este Markdown proviene de una extracción automática del PDF. Algunas ecuaciones, tablas y símbolos pueden requerir revisión manual contra el PDF original antes de una entrega final. Para análisis técnico, usar este archivo como contexto base y verificar valores numéricos críticos en las tablas y figuras originales.
