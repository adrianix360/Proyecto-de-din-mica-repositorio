# Proyecto de vibraciones mecánicas

**Universidad de Costa Rica**  
Facultad de Ingeniería  
Escuela de Ingeniería Civil  
IC-0502: Dinámica

**Presentan:** Adrián Gutiérrez Oviedo (C13550); Alejandro Porras Navas (C26029); Daniel Artavia Aguilar (C20836); Fabiola Raquel Fallas Monge (C22848); Pablo Andrés Rodríguez Mora (C16666); Susana Jiménez Valverde (C24116).

**Profesor:** Ing. Yi Cheng Liu Kuan

**Lugar y fecha:** Ciudad Universitaria Rodrigo Facio, Costa Rica. Julio, 2024.

> Nota de conversión: Markdown optimizado para Claude. Se eliminaron índices, saltos de página y números de página para reducir tokens. Las figuras no se incrustaron como imágenes; se conservan sus títulos/captions y fuentes. Las tablas se conservaron como texto extraído con el espaciado original.

---

# 1. Introducción
## 1.1. Importancia

   Costa Rica es un país sísmicamente activo, es por esta razón que la aplicación de la ingeniería
sismo-resistente tiene un gran aporte en el desarrollo de cualquier obra civil dentro del territorio
nacional. Los cálculos estructurales y el estudio de los comportamientos de las edificaciones ante
acciones sísmicas son parte de los aportes que tiene esta área en la ingeniería civil. Además, la
aplicación de conocimientos de la dinámica estructural permite evaluar y predecir el
comportamiento de las estructuras durante un evento sísmico. Dicho lo anterior, se demuestra
que el análisis de las vibraciones sísmicas les da a los ingenieros civiles una herramienta para
prever daños generados por un sismo en una estructura, logrando de esta manera que los
ingenieros puedan diseñar y construir obras sismo-resistentes.
   De la misma manera, este proyecto busca analizar las propiedades y comportamientos
dinámicos de dos edificios distintos. Dando como resultado, el uso de software (MATLAB)
especializado en el análisis de datos; este software es una herramienta que facilita el
entendimiento de distintos conceptos de la dinámica estructural, como, por ejemplo: vibración
libre, vibración forzada, rigidez, amortiguamiento, registros sísmicos, entre otros.
   En fin, la realización de este proyecto permite recopilar y comprender todos los conceptos y
cálculos que se encuentran en el estudio de vibraciones mecánicas, logrando así, dar a los
estudiantes involucrados un acercamiento a la teoría de la ingeniería sismo-resistente.

## 1.2. Objetivos

### 1.2.1. Objetivo general

- Construir, experimentar, caracterizar y comparar las propiedades dinámicas de dos
       edificios que comparten la misma base, ambos de 2 grados de libertad, con sus columnas
       empotradas en la base, y analizar comportamientos dinámicos de ambos ante
       movimientos introducidos en la base mediante el uso de una mesa vibratoria.

### 1.2.2. Objetivos específicos

- Diseñar y construir según las especificaciones las estructuras de 2 edificios de 2 plantas,
       donde a cada uno de ellos se les añadirán una masa total que puede variar de 2 a 3 kg
       ubicadas en las 2 plantas dependiendo de la capacidad del edificio construido.
- Determinar experimentalmente las frecuencias naturales de vibración y amortiguamiento
       de las estructuras mediante pruebas de vibración libre.


- Determinar experimentalmente la frecuencia natural de vibración y amortiguamiento de
        las estructuras mediante pruebas de vibración forzada con la ayuda de la mesa vibratoria.
- Simular el comportamiento dinámico y predecir la historia de desplazamiento en el tiempo
        de la planta alta de las estructuras ante diferentes registros sísmicos, con las
        características dinámicas experimentales identificadas de las estructuras y mediante el
        uso de los métodos numéricos.
- Realizar prueba sísmica de las estructuras ante diferentes eventos sísmicos.
- Comparar y discutir los resultados de simulación analítica y mediciones experimentales
        de la respuesta de las estructuras ante sismos simulados por la mesa vibratoria, y
        comparar los resultados entre los dos edificios.


# 2. Metodología
## 2.1. Diseño y construcción

### 2.1.1. Datos

        Este proyecto se basó en la construcción de dos edificios, uno esbelto y otro chato.
Ambos edificios se empotraron en una misma base la cual fue proporcionada por el docente del
curso. La tabla de montaje era una tabla rectangular de 45,72 cm x 40 cm aproximadamente,
con un espesor de 1,25 cm (1/2 pulgada). La tabla poseía 4 orificios de 0,64 cm (1/4 pulgada)
para el anclaje sobre la mesa vibratoria. En la Figura 1 se pueden observar las dimensiones de la
base y la dirección del movimiento.


**Figura 1. Dimensiones de la tabla y sus respectivos orificios para su anclaje a la mesa vibratoria**
*Fuente: Proyecto Mecánica II con mesa vibratoria (2023)*


       Para la construcción de las dos torres se ocuparon los siguientes materiales: pinchos,
madera balsa, lija para madera, segueta, goma blanca y cinta métrica o regla. Primeramente, se
precisaron las dimensiones en planta de los dos edificios por construir; para tomar una decisión
se basó en las posibles medidas que se encuentran en la Figura 2.


**Figura 2. Dimensiones máximas y mínimas en planta de los edificios**
*Fuente: Proyecto Mecánica II con mesa vibratoria (2023)*


       Al final se trabajó para el edificio chato y el edificio esbelto las mismas dimensiones en
planta; siendo estas: 14 cm de largo y 15 cm de ancho. Además, como se pudo observar en la
Figura 2 el espaciamiento mínimo entre los edificios era de 9 cm de largo, pero para este proyecto
se construyó con un distanciamiento de 7 cm esto debido a que, si se seguían las instrucciones,
los edificios iban a quedar a menos de 1 cm de distancia con el borde y dicha situación no era
recomendable. Ahora se puede observar en la Figura 3 las medidas antes mencionadas e
inclusive se logra visualizar que los edificios quedan con un espacio entre 4 cm a 5 cm respecto
al borde.


**Figura 3. Dimensiones en planta utilizadas para ambos edificios**
*Fuente: (Elaboración propia)*


       Seguidamente,     se   trabajaron    las   medidas    de    elevación para    cada   edificio
respectivamente. Al igual que en la parte de dimensiones de planta, se tenían medidas máximas
y mínimas para cada edificio (información dada por el docente del curso). A continuación, en la
Figura 4 se observan dichas dimensiones.


**Figura 4. Dimensiones en elevación para cada edificio.**
*Fuente: Proyecto Mecánica II con mesa vibratoria (2023)*


       En el edificio esbelto se construyó con las siguientes características: 90 cm de alto, 8
columnas de 45 cm de largo, 8 vigas de 15.6 cm de largo y 8 empotramientos de 3 cm de largo.


Finalmente, para el edificio chato se construyó en base a las siguientes características: 30 cm de
alto, 8 columnas de 15 cm de largo, 8 vigas de 15.6 cm de largo y 8 empotramientos de 3 cm de
largo.

### 2.1.2. Fase constructiva

         A continuación, se podrá observar en la Figura 5 una representación gráfica del proceso
de construcción de los edificios.


**Figura 5. Diagrama de flujo de la metodología del proceso constructivo**
*Fuente: (Elaboración propia)*


         La información encontrada en la Figura 5 es un resumen del proceso que se llevó a cabo
para la construcción del edificio esbelto y el edificio chato. La ejecución de la revisión de
instrucciones y la elección de diseño de cada edificio fue de suma importancia, primeramente,
esto permitió que todos los miembros del grupo pudieran entender el propósito de este proyecto,
las fases constructivas y además se dio la posibilidad de la discusión de distintas ideas para el
diseño de cada edificio. Completando las fases anteriormente descritas, se logra el cálculo y la
compra de los materiales necesarios para la elaboración de ambos edificios dando como
resultado una reducción significativa en el posible desperdicio de material.
         Posteriormente del análisis, comprensión y decisión sobre el diseño de ambos edificios,
se procedió a la construcción de cada estructura. Para ambos edificios se decidió que la mejor
manera de armarlos era distribuir entre los miembros del grupo distintas tareas como, por
ejemplo: la elaboración de las vigas, columnas y empotramientos. Seguidamente, se realizaría la
unión entre vigas y columnas. En esta parte de la construcción se decidió no unir todavía las
columnas a la tabla base, esto debido a que, si se trabajaba de una vez sobre la base, se corría


el riesgo de no lograr uniones perfectas y que así de alguna manera el edificio quedara con cierta
inclinación (facilitando luego en las pruebas de laboratorio un fallo prematuro). Luego de tener
listo el marco de cada edificio, se colocaron los arriostres. Para el edificio esbelto el
arriostramiento fue colocado en forma de “x”; con el fin de dar suficiente rigidez al edificio en el
sentido transversal y evitar a toda costa movimientos indeseados en dicho sentido, fue necesario
para ambas plantas colocar dos veces este sistema de arriostres. Del mismo modo, para el
edificio chato, se colocaron sistemas de arriostramiento, solo que en esta situación se tomó la
decisión de que el arriostre fuera solo una diagonal, para que de tal manera se evitara un exceso
de rigidez en la estructura.
        Finalmente, todas las columnas, vigas y arriostres estaban perfectamente unidos; dada
esa razón se procedió con la unión de cada edificio a la tabla de montaje (realización del
empotramiento). Cada edificio contaba en la primera planta con cuatro columnas, las cuales
serían las responsables de transmitir todo el peso del edificio a la base. Para la simulación del
empotramiento se elaboraron bloques de madera. De igual manera, los empotramientos iban a
estar en dirección del movimiento para un mejor comportamiento en las pruebas de laboratorio;
dando como resultado, que dos caras de cada columna estarían en contacto con un bloque de
empotramiento. Este diseño de empotramiento fue el mismo para cada edificio, solamente con
una pequeña diferencia en el edificio esbelto; la cual resulta ser la adhesión de un bloque más
(por encima de los bloques anteriores) con el fin de formar un empotramiento tipo “L”.


**Figura 6. Resultado final**
*Fuente: (Elaboración propia)*


### 2.1.3. Dificultades

       Primeramente, se empezaron a tomar las medidas de la tabla base para así marcar las
zonas donde se iban a colocar las columnas y sus respectivos empotramientos. Es en este
momento que el equipo de trabajo se enfrenta a un primer problema, un error en las medidas del
proyecto; y es que en el documento donde se encuentran las instrucciones, se especifica que los
edificios deben se estar separados por una distancia mínima de 9 cm (ver Figura 1), lo cual
provocaba que los edificios estuvieran al borde de la tabla de montaje y a una distancia
aproximada de 0.5 cm de los agujeros de ensamblaje; lo cual podría provocar futuros
inconvenientes en el ensamblaje de las torres a la mesa vibratoria.
       Finalmente, otra dificultad que se afrontó durante el proceso constructivo fue con la
madera balsa. Hubieron dos situaciones en específico con este material; la primera circunstancia
fue que, para poder elaborar las vigas y las columnas, se tenía que cortar varios centímetros de
más respecto a la medida necesaria, esto debido a que si se cortaba con la medida exacta podía
suceder que el material se fracturaba justamente en la zona de corte y esto impediría una correcta
unión entre los elementos; de la misma manera, si sucedía dicha situación, pero se tenía un
margen, la solución era lijar el material hasta que quedara con la medida correcta y en un buen
estado para realizar las futuras conexiones. De igual modo, la otra problemática con dicho
material es que en los momentos en los cuales se aplicaba un poco de fuerza (para sujetar el
material mientras se cortaba) este se hundía, dando la impresión de que el material estaba
podrido o húmedo.


# 3. Caracterización dinámica del edificio
   En la sección siguiente, se hará una recopilación numérica y gráfica de las principales
características dinámicas de los edificios ensayados. A través de distintos métodos, se buscará
definir la respuesta de dichas estructuras ante distintas interacciones dinámicas. La información
obtenida, será fundamental para análisis posteriores.

## 3.1. Prueba de vibración libre

      La prueba de vibración libre de los edificios consistió en una serie de impactos aplicados
para comprender su respuesta al movimiento. Previo al ensayo, se instrumentalizaron las
estructuras con la finalidad de obtener datos que midieran ambos niveles de los modelos de dos
grados de libertad. En las subsecciones siguientes, se estudiará la respuesta obtenida para cada
edificio (alto y bajo), así como una comparativa de las mediciones obtenidas.


### 3.1.1. Resultados de vibración libre del edificio alto

       Para comprender el comportamiento general del edificio alto en la prueba de vibración
libre, se adjuntan la Figura 7 y Figura 8. En las anteriores, es posible observar la historia de
desplazamiento y aceleración del edificio esbelto.


**Figura 7. Desplazamiento del edificio alto en función del tiempo para la prueba de vibración libre**
*Fuente: (Elaboración propia)*


**Figura 8. Aceleración del edificio alto en función del tiempo para la prueba de vibración libre**
*Fuente: (Elaboración propia)*


        Como se puede observar en ambas figuras, se realizó una prueba de vibración libre de
alrededor de 230 segundos. Como parte fundamental de la caracterización dinámica que se debe
realizar, es necesario conocer los periodos de oscilación del modelo. Con la finalidad de calcular
dichos periodos, es necesario tomar datos de las gráficas de desplazamiento en función del
tiempo (para el modo fundamental) y aceleración en función de tiempo (para el segundo modo
de oscilación).
        Para obtener los periodos de oscilación del edificio, se tomarán dos mediciones por modo.
En el caso del periodo de oscilación del modo fundamental del sistema, se debe de extraer la
información de una sección acotada de la historia de desplazamiento. Las historias de
desplazamiento seleccionadas para las series de medición son las asociadas al sensor que medía
el movimiento en la parte alta de la torre. El criterio que sustenta la selección de dicho sensor se
basa en que el nivel superior posee el mayor movimiento ante una vibración libre.
        Las series de medición que se tomaron de muestra se encuentran ilustradas en la Figura
9 y Figura 10.


**Figura 9. Acercamiento al gráfico de desplazamiento del edificio alto en función del tiempo para la prueba**
                                de vibración libre; primera serie de datos
*Fuente: (Elaboración propia)*


**Figura 10. Acercamiento al gráfico de desplazamiento del edificio alto en función del tiempo para la**
                              prueba de vibración libre; segunda serie de datos
*Fuente: (Elaboración propia)*
         Como se puede observar en las dos figuras adjuntas, las etiquetas de los valores más
altos de cada ciclo de oscilación decrecen al pasar el tiempo. Lo anterior se sustenta en el
supuesto de que las estructuras ensayadas amortiguan las vibraciones libres que reciben. Por lo
anterior, la función sinusoidal que modela el desplazamiento de la estructura decrece por la
acción de una exponencial envolvente, que se relaciona al amortiguamiento y a la frecuencia
circular natural del sistema.
         Para medir con mayor exactitud el periodo de oscilación del edificio alto, se recopilaron
los datos de desplazamiento en el Cuadro 1.

**Cuadro 1. Determinación del periodo de oscilación del modo fundamental del edificio alto en la prueba de**
vibración libre con su historia de desplazamiento

                Primera serie                                         Segunda Serie
  Tiempo al pico de                                      Tiempo al pico de
                             Periodo (s)                                          Periodo (s)
  desplazamiento (s)                                     desplazamiento (s)
        6,830                  0,550                          136,470               0,540
        7,380                  0,550                          137,010               0,570
        7,930                  0,550                          137,580               0,540
        8,480                  0,560                          138,120               0,540
        9,040                  0,550                          138,660               0,580
        9,590                  0,560                          139,240               0,530
       10,150                  0,540                          139,770               0,550
       10,690                  0,540                          140,320               0,560
       11,230                  0,570                          140,880               0,550


                Primera serie                                          Segunda Serie
  Tiempo al pico de                                       Tiempo al pico de
                             Periodo (s)                                           Periodo (s)
  desplazamiento (s)                                      desplazamiento (s)
       11,800                  0,540                           141,430               0,550
       12,340                                                  141,980

      Promedio                        0,551                                                   0,551
 Desviación Estándar                  0,010                                                   0,015


        Como es posible observar en las mediciones obtenidas en el Cuadro 1, el periodo de
oscilación obtenido del modo fundamental para la primera y segunda serie de datos es idéntico
(en sus primeros 3 dígitos significativos). Es notable que la medición del periodo difiere respecto
a su desviación estándar. Mientras que en la primera serie la desviación estándar representa un
1,805% del promedio, para la segunda serie, esta representa un 2,766%.
        El incremento en la varianza de la segunda serie se puede deber a diversos factores
asociados a la forma en la que se aplicó la fuerza en el momento de la medición. A pesar de la
discrepancia, se puede observar que hay una alta uniformidad en los datos del periodo. Por lo
tanto, se puede afirmar que el periodo del modo fundamental del edificio esbelto es igual a 0,551
segundos.
        Para obtener el periodo del segundo modo de vibración del edificio, se tomaron datos de
la aceleración en función del tiempo del edificio. Sobre el comportamiento de la Figura 8, se
tomaron las mediciones de tiempo asociadas a los “picos” de aceleración en dos series distintas.
La información anterior se encuentra resumida en el Cuadro 2.


**Figura 11. Gráfico de historia de vibración libre de la aceleración del edificio alto, para determinar el**
                                       periodo del modo fundamental.
*Fuente: (Elaboración propia)*


**Figura 12. Gráfico de historia de vibración libre de la aceleración del edificio alto, para determinar el**
                                          periodo de la segunda serie.

*Fuente: (Elaboración propia)*


**Cuadro 2. Determinación del periodo de oscilación del segundo modo del edificio alto en la prueba de**
vibración libre con su historia de aceleración

                   Primera serie                                          Segunda serie
     Tiempo al pico de                                       Tiempo al pico de
                                Periodo (s)                                           Periodo (s)
      aceleración (s)                                         aceleración (s)
         81,270                   0,200                          96,500                 0,240
         81,470                   0,240                          96,740                 0,200
         81,710                   0,190                          96,940                 0,200
         81,900                   0,200                          97,140                 0,200
         82,100                   0,230                          97,340                 0,220
         82,330                   0,200                          97,560                 0,220
         82,530                   0,210                          97,780                 0,200
         82,740                   0,220                          97,980                 0,210
         82,960                   0,200                          98,190                 0,220
         83,160                   0,220                          98,410                 0,200
         83,380                   0,200                          98,610                 0,220
         83,580                   0,210                          98,830                 0,200
         83,790                   0,210                          99,030                 0,210
         84,000                                                  99,240

      Promedio                          0,210                                                   0,211
 Desviación Estándar                    0,014                                                   0,013


          Acerca de los datos recopilados en el Cuadro 2, se puede afirmar que hay uniformidad en
los resultados obtenidos en ambas series. En el caso de la primera serie, la desviación estándar
representa un 6,734% del promedio general, mientras que, en la segunda serie, el porcentaje


corresponde a 5,958%. Dado que ambas medidas de dispersión son bajas, se puede afirmar que
la medida del periodo para el segundo modo de vibración para el edificio alto ronda entre 0,211
y 0,210 segundos.
        Otra de las propiedades fundamentales que se deben conocer acerca de la estructura es
su amortiguamiento. Para estudiarlo, es necesario utilizar la fórmula del decremento logarítmico,
que se muestra en la ecuación [ 1 ].

                                          𝑢𝑖
                                𝛿 = ln        = 𝑗2𝜋𝜉                                       [1]
                                         𝑢𝑖+𝑗

        Con los datos obtenidos de la prueba de vibración libre, se formuló una recopilación de
datos y cálculos para encontrar el amortiguamiento de la estructura. Para dicha determinación,
se utilizaron los picos máximos y mínimos que se encuentran en la historia de desplazamiento de
la Figura 7. Dichos datos se encuentran almacenados en el Cuadro 3.

**Cuadro 3. Determinación del amortiguamiento del edificio alto en la prueba de vibración libre, para el**
desplazamiento del modo fundamental

 Número        Y = Umáx         Y = Umín        δ Umín        δ Umin           ξ             ξ
   (k)           (mm)            (mm)            j=1           j=1           (Umax)        (Umin)
    1          12,1010         -12,4550        0,0873        0,0632         0,0139        0,0101
    2          11,0900         -11,6920        0,0948        0,1052         0,0151        0,0167
    3          10,0860         -10,5240        0,0546        0,0616         0,0087        0,0098
    4           9,5510          -9,8961        0,1033        0,0856         0,0164        0,0136
    5           8,6130          -9,0840        0,0687        0,1108         0,0109        0,0176
    6           8,0420          -8,1310        0,0711        0,0500         0,0113        0,0080
    7           7,4900          -7,7342        0,1000        0,0985         0,0159        0,0157
    8           6,7770          -7,0088        0,0695        0,0783         0,0111        0,0125
    9           6,3214          -6,4809        0,0745        0,0638         0,0119        0,0102
   10           5,8676          -6,0803
                                                           Promedio         0,0128        0,0127
                                                           Desviación
                                                                            0,0025        0,0032
                                                            Estándar

        Como se puede observar, los promedios obtenidos para el amortiguamiento del edificio
alto son muy similares sin importar el pico que se tomó para la formulación. Para el Umáx se tiene
un amortiguamiento estimado del 1,28%, mientras que para el Umín se tiene un amortiguamiento
estimado del 1,27%. Acerca de la desviación estándar, se puede notar que hay una uniformidad
aceptable en los datos. En el caso del Umáx , la desviación estándar representa un 19,47% del
promedio obtenido, mientras que para el Umín, esta representa un 25,61% del promedio.


       En general, se tiene que las mediciones por el método del decremento logarítmico son
uniformes en su distribución y arrojan un resultado muy similar entre sí. Por lo tanto, se puede
afirmar que el amortiguamiento del edificio esbelto ronda entre el 1,27% y el 1,28%.
       Con la finalidad de comprender de otra forma el fenómeno físico de las vibraciones
mecánicas en el edificio esbelto, se buscarán las frecuencias modales de la estructura. Lo
anterior, se hará aplicando la transformada rápida de Fourier. El resultado de dicha
transformación a una historia de vibración es una “acumulación” de la señal en las frecuencias
de mayor amplitud. Dicha acumulación es de utilidad para analizar el periodo de oscilación de
una estructura.
       En la Figura 13 se muestra la historia de aceleración seleccionada para el análisis del
periodo de oscilación.


**Figura 13. Aceleración del edificio alto en función del tiempo para la prueba de vibración libre, acotado**
                             para la aplicación de la transformada de Fourier
*Fuente: (Elaboración propia)*
> Nota: El gráfico está acotado desde el registro 300 hasta el registro 2348.


       Como se puede observar, en la Figura 13 se recopila una historia de aceleración para un
solo modo de oscilación. Dado que la transformada rápida de Fourier, va a indicar de forma gráfica
la frecuencia de oscilación del sistema, es necesario conocer la relación entre la frecuencia y el
periodo. Esta relación es descrita por la ecuación [ 2 ]. En la Figura 14 se encuentra el gráfico
producido por la transformada rápida de Fourier, siendo que esta se aplicó al intervalo que va del
registro 300 al 2348.


                                       𝑇 = 𝑓 −1                                                 [2]


**Figura 14. Espectro de Fourier en escala logarítmica para la historia de aceleración del edificio alto en la**
                                        prueba de vibración libre.
*Fuente: (Elaboración propia)*


       Como se puede observar, en la Figura 8. Sobre la historia de aceleración de vibración
libre del edificio alto se observa fácilmente en donde se ubica el periodo fundamental, sin
embargo, se identifican otras señales candidatas a ser el registro del segundo modo, se le aplicó
transformada de Fourier a cada una de las señales y se obtuvo:


**Figura 15. Aceleración del edificio alto en función del tiempo para la prueba de vibración libre, acotado**
                            para la aplicación de la transformada de Fourier

*Fuente: (Elaboración propia)*


**Figura 16. Espectro de Fourier en escala logarítmica de uno de los candidatos al segundo modo para la**
                historia de aceleración del edificio alto en la prueba de vibración libre.

*Fuente: (Elaboración propia)*


**Figura 17. Aceleración del edificio alto en función del tiempo para la prueba de vibración libre, acotado**
                            para la aplicación de la transformada de Fourier

*Fuente: (Elaboración propia)*


**Figura 18. Espectro de Fourier en escala logarítmica de uno de los candidatos al segundo modo para la**
                 historia de aceleración del edificio alto en la prueba de vibración libre.

*Fuente: (Elaboración propia)*


        A partir de la Figura 16 y Figura 18, no se puede obtener información clara sobre si esos
picos son del valor de frecuencia para el segundo modo, debido a esto se omiten estos datos y
solamente se utilizan los pertenecientes a la Figura 14 para determinar la frecuencia mediante
transformada de Fourier del edificio alto, ya que si brindan información clara en los picos de la
transformada.
        Así como se puede observar en la Figura 14, hay 2 picos en el espectro de Fourier que
superan ampliamente a las demás partes del registro. Estos datos máximos corresponden a las
frecuencias del 1° (fundamental) y 2° modo de vibración. Como se enunció anteriormente, es
necesario distinguir el periodo de oscilación, por lo que al aplicar la ecuación [ 2 ], se obtiene:

                𝑇𝐹𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙 = 𝑓 −1                                   𝑇2° 𝑀𝑜𝑑𝑜 = 𝑓 −1

        𝑇𝐹𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙 = (1,85547 𝐻𝑧)−1                          𝑇2° 𝑀𝑜𝑑𝑜 = (4,78516 𝐻𝑧)−1

             𝑇𝐹𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙 = 0,539 𝑠                                  𝑇2° 𝑀𝑜𝑑𝑜 = 0,209 𝑠

### 3.1.2. Resultados de vibración libre del edificio bajo

      Así como se realizó un análisis de las principales propiedades dinámicas del edificio alto, se
reproducirá el mismo para el edificio bajo. Cabe destacar que el edificio bajo también puede ser
llamado “chato”, así como este es antónimo al término “esbelto”, utilizado para el análisis de la
subsección anterior.


       Primeramente, para comprender la prueba de vibración libre a la que fue sometida el edificio
bajo, se muestran las historias de desplazamiento y aceleración para el modelo. Dichas historias
para la vibración libre se encuentran en la Figura 19 y Figura 20 respectivamente.


**Figura 19. Desplazamiento del edificio bajo en función del tiempo para la prueba de vibración libre**
*Fuente: (Elaboración propia)*


**Figura 20. Aceleración del edificio bajo en función del tiempo para la prueba de vibración libre**
*Fuente: (Elaboración propia)*

         Acerca de las figuras anteriores, se puede notar que, en comparación al edificio alto, los
impactos recibidos por el edificio bajo son mucho más “explosivos” en lo que respecta a la
aceleración y el desplazamiento. Al igual que con la subsección anterior, se buscarán encontrar


los periodos de oscilación del edificio. Para este fin de aplicarán diversos métodos, el primero de
estos se enfoca en tomar los datos directamente del comportamiento gráfico del sistema.

        Para conocer el periodo del modo fundamental de vibraciones, se tomaron mediciones
del desplazamiento en función del tiempo del edificio. En la Figura 21 se muestra una sección de
la historia de vibración libre, que fue utilizada para encontrar el periodo del 1° modo de vibración.


**Figura 21. Acercamiento al gráfico de desplazamiento del edificio bajo en función del tiempo para la**
                            prueba de vibración libre; primera serie de datos
*Fuente: (Elaboración propia)*

      Los datos recopilados en la Figura 21, fueron de utilidad para elaborar el Cuadro 4, donde
se estima el periodo fundamental de oscilación del edificio chato.

**Cuadro 4. Determinación del periodo de oscilación del modo fundamental del edificio bajo en la prueba**
de vibración libre con su historia de desplazamiento

                Primera serie                                       Segunda serie
  Tiempo al pico de                                    Tiempo al pico de
                             Periodo (s)                                        Periodo (s)
  desplazamiento (s)                                   desplazamiento (s)
       39,710                  0,110                        40,720                0,110
       39,820                  0,120                        40,830                0,120
       39,940                  0,110                        40,950                0,110
       40,050                  0,120                        41,060                0,110
       40,170                  0,100                        41,170                0,110
       40,270                  0,120                        41,280                0,110
       40,390                  0,110                        41,390                0,110
       40,500                  0,110                        41,500                0,110
       40,610                                               41,610


                Primera serie                                       Segunda serie
  Tiempo al pico de                                    Tiempo al pico de
                             Periodo (s)                                        Periodo (s)
  desplazamiento (s)                                   desplazamiento (s)

      Promedio                      0,113                                                0,111
 Desviación Estándar                0,007                                                0,004


        Los resultados que se muestran en el Cuadro 4, son muestra de una medición consistente
del periodo fundamental del edificio chato. La relación porcentual de la desviación estándar de la
primera serie, respecto al promedio de la misma, es de 6,285%, mientras que esta relación para
la segunda serie es de 3,178%. Conociendo la baja dispersión de los datos respecto a la media,
se puede afirmar que el periodo del modo fundamental de vibración para el edificio bajo se
encuentra entre 0,111 y 0,113 segundos.
        Sobre este mismo edificio, se puede conocer el periodo de su segundo modo de vibración,
si se utiliza la historia de aceleración en función del tiempo del sistema. Los datos para estimar
dicho periodo se obtuvieron de dos series cercanas. Las series mencionadas, se pueden observar
en la Figura 22.


**Figura 22. Acercamiento al gráfico de aceleración del edificio bajo en función del tiempo para la prueba**
                          de vibración libre; primera y segunda serie de datos
*Fuente: (Elaboración propia)*

        Los datos recopilados en la Figura 22, fueron de utilidad para elaborar el Cuadro 5,
donde se estima el periodo del segundo modo de vibración del edificio chato.


**Cuadro 5. Determinación del periodo de oscilación del segundo modo del edificio bajo en la prueba de**
vibración libre con su historia de aceleración

                 Primera serie                                    Segunda serie
   Tiempo al pico de                                 Tiempo al pico de
                              Periodo (s)                                     Periodo (s)
    aceleración (s)                                   aceleración (s)
       120,880                  0,020                    121,520                0,020
       120,900                  0,020                    121,540                0,020
       120,920                  0,020                    121,560                0,020
       120,940                  0,050                    121,580                0,030
       120,990                  0,050                    121,610                0,020
       121,040                  0,040                    121,630                0,020
       121,080                  0,040                    121,650                0,020
       121,120                  0,050                    121,670                0,020
       121,170                  0,040                    121,690                0,020
       121,210                  0,050                    121,710                0,050
       121,260                  0,040                    121,760                0,050
       121,300                  0,040                    121,810                0,040
       121,340                  0,050                    121,850                0,040
       121,390                                           121,890

      Promedio                    0,039                                             0,028
 Desviación Estándar              0,012                                             0,012


       Se puede observar que los resultados del Cuadro 5, acerca de las mediciones del periodo
son muy distintas. La primera serie de datos tiene una dispersión muy alta, si se basa esta
medición en la desviación estándar. Dicha dispersión, contrastada con el promedio, representa
un 30,271% del valor esperado, mientras que el mismo contraste para la segunda serie es de un
42,662%. Esta característica de dispersión alta también se puede observar en los resultados
entre series. Mientras que la primera arroja un periodo promedio de 0,039 segundos, la segunda
arroja uno de 0,028 segundos.
       Estas diferencias importantes que fueron obtenidas experimentalmente se deben a que el
edificio bajo era muchísimo más rígido que el alto. Por lo anterior, con una prueba de vibración
libre fue mucho más difícil encontrar su segundo modo de vibración. Así como se puede observar
en la Figura 22, la respuesta de edificio es descoordinada y no sigue ninguna tendencia fija.
Inclusive si se toma el periodo más lago y de menor dispersión, este representa solo treinta y
nueve milésimas de segundo.
       Con la finalidad de comprender otras características dinámicas de la estructura y explicar
las distorsiones del segundo modo de vibración; Se encontró el amortiguamiento del edificio bajo.
Para calcularlo, se utilizaron datos de la gráfica de desplazamiento en función del tiempo (como


la historia de la Figura 19). El cálculo, se basó en la fórmula del decremento logarítmico, presente
en la ecuación [ 1 ]. Dichos datos, fueron recopilados en el Cuadro 6

**Cuadro 6. Determinación del amortiguamiento del edificio bajo en la prueba de vibración libre, para el**
desplazamiento del modo fundamental

 Número        Y = Umáx         Y = Umín        δ Umín        δ Umin           ξ             ξ
   (k)          (mm)             (mm)            j=1           j=1           (Umax)        (Umin)
    1          0,9636           -0,6977        0,4599        0,0286         0,0732        0,0046
    2          0,6084           -0,6780        0,1269        0,2120         0,0202        0,0337
    3          0,5359           -0,5485        0,2029        0,0012         0,0323        0,0002
    4          0,4375           -0,5478        0,0253        0,0284         0,0040        0,0045
    5          0,4265           -0,5325        0,0214        0,0565         0,0034        0,0090
    6          0,4175           -0,5032        0,0786        0,0437         0,0125        0,0070
    7          0,3859           -0,4817        0,1848        0,1153         0,0294        0,0183
    8          0,3208           -0,4293        0,1185        0,0743         0,0189        0,0118
    9          0,2850           -0,3985        0,0178        0,0271         0,0028        0,0043
   10          0,2800           -0,3879
                                                           Promedio         0,0219        0,0104
                                                           Desviación
                                                            Estándar        0,0209        0,0096

        Acerca de los resultados obtenidos del Cuadro 6, se puede observar una discrepancia
significativa entre las mediciones. El decremento logarítmico se aplicó a los picos mínimos y
máximos de las series de datos. En el caso de los máximos, se obtuvo un amortiguamiento de
2,19%, con una desviación estándar de 0,0209. Dicha desviación representa un 95,493% del
promedio. En el caso de los mínimos, se obtuvo un amortiguamiento del 1,04%, con una
desviación estándar de 0,0096. La desviación de esta serie representa un 92,701% del promedio.
        La amplia dispersión de las mediciones en la historia de desplazamiento se puede deber
a la alta rigidez de la estructura. Siendo que es una prueba de vibración libre, las velocidades
iniciales que fueron impresas al modelo, no conseguían hacerlo oscilar lo suficiente como para
obtener una medición fina dada la tasa de muestreo de los instrumentos.
        Como análisis final de la vibración libre en el edificio chato, se aplicará el método de la
transformada rápida de Fourier (TRF), con la finalidad de encontrar las frecuencias modales de la
estructura. La TRF se aplicará a una serie de datos selecta de la historia de vibración libre del
edificio chato. En la Figura 23, se encuentra una muestra de los datos utilizados para la aplicación
de la TRF.


**Figura 23. Aceleración del edificio bajo en función del tiempo para la prueba de vibración libre, acotado**
                             para la aplicación de la transformada de Fourier
*Fuente: (Elaboración propia)*
> Nota: El gráfico está acotado desde el registro 11900 hasta el registro 14000.


        En la Figura 24, se encuentra el resultado gráfico de aplicar la TRF a la serie de datos que
se encuentra en la Figura 23.


**Figura 24. Espectro de Fourier en escala logarítmica para la historia de aceleración del edificio bajo en la**
                                         prueba de vibración libre
*Fuente: (Elaboración propia)*


        En la Figura 24, se observa que hay 2 “picos” que superan en amplitud a las demás
frecuencias del espectro. Sin embargo, así como se ha ilustrado en partes anteriores de esta
sección, hay áreas problemáticas en el análisis del edificio bajo por su alta rigidez. A pesar de que
hay 2 señales dominantes, la demás parte del espectro de Fourier no es necesariamente muy
inferior a las mediciones de las crestas. Aun siendo así, se pueden calcular los periodos del edificio
utilizando la ecuación [ 2 ].
        Para los periodos de oscilación del edificio bajo se tiene que:

                𝑇𝐹𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙 = 𝑓 −1                                     𝑇2° 𝑀𝑜𝑑𝑜 = 𝑓 −1

         𝑇𝐹𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙 = (8,98438 𝐻𝑧)−1                           𝑇2° 𝑀𝑜𝑑𝑜 = (22,2656 𝐻𝑧)−1

              𝑇𝐹𝑢𝑛𝑑𝑎𝑚𝑒𝑛𝑡𝑎𝑙 = 0,111 𝑠                                  𝑇2° 𝑀𝑜𝑑𝑜 = 0,045 𝑠


### 3.1.3. Comparación de edificios en vibración libre

      En la sección presente, se hará una comparación del comportamiento de ambos edificios
ante la prueba de vibración libre. Para realizar la comparación se hará una inspección visual. En
la Figura 25 se muestra la superposición de las historias de desplazamiento de ambas torres.


**Figura 25. Superposición de las historias de desplazamiento para la prueba de vibración libre en el edificio**
                                                alto y bajo
*Fuente: (Elaboración propia)*

        Acerca de lo mostrado en la Figura 25, es notorio que hay una diferencia marcada en las
amplitudes máximas del desplazamiento para el edificio alto y bajo. Lo anterior se debe a que la
rigidez del edificio alto es mucho menor a la del edificio bajo. Por lo tanto, la amplitud máxima del
movimiento (en el segundo nivel), es mayor. Lo anterior se puede evidenciar en los periodos de


oscilación de los modelos, como se muestra en el Cuadro 7. Para observar de mejor manera
estas diferencias, se hizo un acercamiento al gráfico anterior. Dicho acercamiento se encuentra
en la Figura 26.


**Figura 26. Acercamiento a la superposición de las historias de desplazamiento para la prueba de**
                                 vibración libre en el edificio alto y bajo
*Fuente: (Elaboración propia)*

       Acerca de la Figura 26, se puede notar que las amplitudes del desplazamiento son
distintas. En el caso del edificio alto se tienen desplazamientos cercanos a los 13 mm. El edificio
bajo tiene una amplitud de onda menor a 5 mm. Otra comparación relevante es la superposición
de las ondas de aceleración, medidas para ambos edificios en la prueba de vibración libre. Dicha
comparativa gráfica se encuentra en la Figura 27.


**Figura 27. Superposición de las historias de aceleración para la prueba de vibración libre**
*Fuente: (Elaboración propia)*


          En el caso de las historias de aceleración, el comportamiento es inverso al observado en
la Figura 25. En este caso, se puede observar que el edificio alto llega a unas aceleraciones pico
que rondan 0,2g. Para el edificio bajo se tiene que las aceleraciones pico que alcanza son de
0,5g, aproximadamente. El comportamiento es el esperado según la teoría. Dado que el edificio
bajo tiene una mayor rigidez y un periodo fundamental más corto, la estructura se acelera más
rápido para completar su ciclo de oscilación, por lo tanto, siguiendo con la teoría y los resultados
obtenidos, se puede concluir que la aceleración de cada edificio es proporcional a la frecuencia
angular natural al cuadrado (wn).
          Para comparar los periodos de oscilación de los edificios, se formuló un cuadro
comparativo. Dicho cuadro (el Cuadro 7) recopila la información obtenida en las subsecciones
anteriores del apartado de vibración libre. En el caso de los periodos obtenidos con los datos
experimentales, se tomó el promedio de las dos series medidas.
**Cuadro 7. Comparativa de los periodos de oscilación de ambos edificios para la prueba de vibración libre**

                                                                  Periodo de oscilación
           Edificio             Método utilizado         Modo fundamental
                                                                              Segundo modo (s)
                                                                (s)
                                Nube de puntos1               0,551                  0,211
             Alto             Transformada rápida
                                                                0,539                    0,209
                                   de Fourier
                                Nube de puntos                  0,112                    0,034
             Bajo             Transformada rápida
                                                                0,111                    0,045
                                   de Fourier


          Como se puede observar en el Cuadro 7, el periodo de ambos modos de oscilación de
las estructuras es muy distinto. Por ejemplo, el periodo del modo fundamental de oscilación del
modelo esbelto es 385,586% más largo que el mismo de la torre chata (tomando el valor
calculado con la TRF).

## 3.2. Prueba de vibración forzada

        La prueba de vibración forzada de los edificios consistió en la aplicación de una serie de
movimientos sinusoidales dentro de un rango de frecuencias. Dicha fuerza excitadora, provenía
del movimiento de la base de la mesa vibratoria. En las subsecciones siguientes, se estudiará la
respuesta obtenida para cada edificio (alto y bajo), así como una comparativa de las mediciones
obtenidas.


    Tomando los datos experimentales. Ver Cuadro 1


### 3.2.1. Resultados de vibración forzada del edificio alto

       Para comprender el comportamiento general del edificio alto en la prueba de vibración
forzada, se adjunta la Figura 28. En la cual, se muestra la superposición de la historia de
aceleración y desplazamiento del piso superior del edificio alto.


**Figura 28. Superposición de la historia de desplazamiento y aceleración del piso superior del edificio**
                                                 esbelto
*Fuente: (Elaboración propia)*


       Como se puede observar de la Figura 28, ambas historias (aceleración y desplazamiento)
presentan un comportamiento similar, debido a la fuerza excitadora aplicada en la base del
edificio. A pesar de esto, sus amplitudes son diferentes, sin embargo, no pueden ser comparadas
debido a que son unidades diferentes, lo que si se aprecia, es que a lo largo de la gráfica, ambos
van aumentando y disminuyendo de la misma manera, solo que el desplazamiento tiene cada vez
una amplitud menor, cuando se llega al segundo modo.

                              Aceleración y desplazamiento siempre están fuera de fase!


**Figura 29. Superposición de la historia de desplazamiento de la base y del piso superior del edificio**
                                                   esbelto
*Fuente: (Elaboración propia)*


         Como se observa en la Figura 29, el desplazamiento de la base refleja directamente el
movimiento impuesto por la mesa vibratoria, actuando como entrada de excitación para el
sistema. En contraste, el desplazamiento del piso superior incorpora la respuesta dinámica del
edificio a esta excitación. De manera que, el piso superior muestra una mayor amplitud de
desplazamiento debido a la amplificación de la respuesta a lo largo de la altura del edificio.

         A continuación, en las Figura 30, Figura 31 y Figura 32, se muestran las historias
superpuestas de desplazamiento del piso superior y la base durante la vibración forzada. Estos
gráficos describen el comportamiento antes, durante y después de que el edificio entre en
resonancia.


**Figura 30. Superposición de la historia de desplazamiento de la base y del piso superior del edificio alto**
                                         (antes de resonancia)
*Fuente: (Elaboración propia)*


**Figura 31. Superposición de la historia de desplazamiento de la base y del piso superior del edificio alto**
                                        (durante de resonancia)
*Fuente: (Elaboración propia)*


**Figura 32. Superposición de la historia de desplazamiento de la base y del piso superior del edificio alto**
                                         (después de resonancia)
*Fuente: (Elaboración propia)*


        Como se observa en las Figura 30, Figura 31 y Figura 32 antes de la resonancia, el
desplazamiento del piso superior es mayor que el de la base, y ambos tienen períodos similares.
Durante la resonancia, el desplazamiento del piso superior aumenta significativamente,
alcanzando aproximadamente diez veces la amplitud observada antes de la resonancia, lo que
también acorta su período. En contraste, en la base, la amplitud del desplazamiento disminuye y
el período aumenta. Después de la resonancia, se observa un desfase entre las ondas de
desplazamiento, con un aumento en el desplazamiento de la base y una disminución en el piso
superior.


        En la siguiente Figura 33 se muestra el método utilizado para la obtención del tiempo de
retraso.


**Figura 33. Ejemplo del método usado para obtener el tiempo de retraso**
*Fuente: (Elaboración propia)*


        En el Cuadro 8 se resumen algunos datos del ángulo experimental calculado según las
frecuencias de vibración de la base para el edificio alto.
**Cuadro 8. Resumen datos del ángulo experimental calculado del edificio alto**

                            Frecuencia
 Frecuencia aplicada                           Tiempo de       ωp experimental       φ de fase
                           experimental
        (Hz)                                   retraso (s)         (rad/s)        experimental (°)
                               (Hz)
          1,0                 1,0000              0,03               6,2832             10,8000
          1,2                 1,2346              0,02               7,7572              8,8891
          1,4                 1,4084              0,02               8,8492             10,1405
          1,5                 1,5385              0,02               9,6667             11,0772
          1,6                 1,6129              0,02              10,1341             11,6129
          1,7                 1,7241              0,02              10,8328             12,4135
          1,8                 1,8182              0,19              11,4241             124,3649
          1,9                 1,8868              0,25              11,8551             169,8120
          2,0                 2,0000              0,22              12,5664             158,4000
          2,1                 2,0833              0,22              13,0898             164,9974
          2,2                 2,1740              0,22              13,6596             172,1808
          2,5                 2,3490              0,20              14,7592             169,1280
          3,0                 2,9412              0,16              18,4801             169,4131
          4,0                 4,0000              0,12              25,1327             172,8000
          4,5                 4,5454              0,12              28,5596             196,3613
          4,6                 4,6511              0,12              29,2237             200,9275


                            Frecuencia
 Frecuencia aplicada                             Tiempo de        ωp experimental          φ de fase
                           experimental
        (Hz)                                     retraso (s)          (rad/s)           experimental (°)
                               (Hz)
          4,7                 4,7619                0,13              29,9199              222,8569
          4,8                 4,8892                0,18              30,7197              316,8202
          4,9                 4,9505                0,01              31,1049              342.1782
          5,0                 5,0000                0,01              31,4159              342.0000
          5,1                 5,1282                0,01              32,2214              341.5385
          5,2                 5,2632                0,01              33,0697              341.0525

       Como se puede observar en el Cuadro 8, a medida que la frecuencia aplicada de vibración
aumenta, la frecuencia experimental del edificio alto se aproxima gradualmente a la frecuencia
aplicada. El tiempo de retraso se mantiene relativamente constante en ciertas secciones, antes,
durante y luego de la resonancia, mientras que la velocidad angular experimental (ωp) muestra un
incremento progresivo con la frecuencia aplicada. Además, hay una variación en el ángulo de
fase experimental (φ), mostrando una tendencia a aumentar mientras más se acerca a la
frecuencia de resonancia, la cual tiene un valor de 1,8 Hz. Luego de alcanzarla, el valor del ángulo
se acerca a los 180°, sin embargo, como se aprecia en la Figura 34, hay valores posteriores que
lo superan debido a que se está entrando al segundo modo de resonancia.


**Figura 34. Ejemplo de la variación del ángulo respecto a la frecuencia del edificio alto.**

*Fuente: (Elaboración propia)*


#### a) Análisis de amplitud estacionaria

        En la Figura 35 se observa el ejemplo del método utilizado para la obtención de la amplitud
estacionaria.


**Figura 35. Ejemplo del método usado para obtener la amplitud estacionaria**
*Fuente: (Elaboración propia)*
        En el Cuadro 9 se presentan los datos obtenidos de amplitud estacionaria para cada
frecuencia analizada del edificio alto. Estos datos incluyen la frecuencia aplicada, la frecuencia
experimental, la amplitud medida, el promedio de las amplitudes y la desviación estándar
correspondiente.
**Cuadro 9. Resumen datos de amplitud estacionaria medida del edificio alto**


                                Frecuencia
            Frecuencia
                               experimental           Amplitud (mm)              Promedio
           aplicada (Hz)
                                   (Hz)
                 1,0              1,0000         0,40993         0,39524          0,40258
                 1,2              1,2346         0,53805         0,54882          0,54343
                 1,4              1,4084         0,70786         0,71443          0,71114
                 1,5              1,5385         0,96257         0,95427          0,95842
                 1,6              1,6129         1,46450         1,45037          1,45744
                 1,7              1,7241         2,06083         2,06001          2,06042
                 1,8              1,8182         12,40580       12,41710         12,41145
                 1,9              1,8868         3,85765         3,85400          3,85583
                 2,0              2,0000         1,75031         1,75423          1,75227
                 2,1              2,0833         1,22940         1,24108          1,23524
                 2,2              2,1740         0,89207         0,90876          0,90042


                               Frecuencia
            Frecuencia
                              experimental            Amplitud (mm)               Promedio
           aplicada (Hz)
                                  (Hz)
                2,5              2,3490          0,53441          0,54927          0,54184
                3,0              2,9412          0,36250          0,37865          0,37057
                4,0              4,0000          0,39169          0,38749          0,38959
                4,5              4,5454          0,47750          0,47030          0,47390
                4,6              4,6511          0,79194          0,79532          0,79363
                4,7              4,7619          1,83111          1,83530          1,83321
                4,8              4,8892          1,90616          1,91227          1,90922
                4,9              4,9505          0,86681          0,86900          0,86791
                5,0              5,0000          0,47422          0,47595          0,47508
                5,1              5,1282          0,36816          0,37190          0,37003
                5,2              5,2632          0,31700          0,30478          0,31089

        Se observa que la amplitud medida varía considerablemente con la frecuencia aplicada,
siendo las amplitudes más altas registradas en frecuencias de 1,8 Hz (12,41145 mm) y 4,7 Hz
(1,83321 mm).

#### b) Curva de transmisibilidad

        En la Figura 36, se presenta la curva de transmisibilidad de desplazamiento para los datos
experimentales del edificio alto.


**Figura 36. Curva de transmisibilidad de desplazamiento experimental para el edificio alto**
*Fuente: (Elaboración propia)*


#### c) Método de ancho de banda

       En la Figura 37 se ilustra la gráfica del método de ancho de banda, junto a los valores de
importancia para usar este procedimiento.


**Figura 37. Datos y gráfica del método de ancho de banda para el edificio alto**
*Fuente: (Elaboración propia)*


       El método de ancho de banda consiste en encontrar la amplitud máxima de la curva de
FAD para dividir dicho valor entre raíz de dos y de este modo obtener una recta constante a una
altura “y”. Los puntos de intersección entre esta recta y la curva de FAD representa los valores
de interés, de manera matemática se sigue que:

                                  𝐴𝑚𝑝𝑙𝑖𝑡𝑢𝑑 𝐹𝐴𝐷 𝑚á𝑥 = 41.3715

                                                            41.3715
                                 𝑅𝑒𝑐𝑡𝑎 𝑑𝑒 𝑖𝑛𝑡𝑒𝑟é𝑠 = 𝑦 =
                                                               √2

                                            𝑦 = 29.2541

       El amortiguamiento por el método de ancho de banda está dado por la ecuación [ 3 ]:

                                         𝑓2 − 𝑓1                                             [3]
                                    𝜉=
                                           2𝑓𝑛


         Se toman los valores mostrados en la Figura 37, las razones de frecuencias se
transforman en frecuencias reales y sustituyendo se obtiene:

                                             1.8439 − 1.7819
                                        𝜉=
                                                2(1,8149)

                                        𝜉 = 0.0171 = 1.71%


#### d) Amortiguamiento mediante prueba de resonancia

         El amortiguamiento del sistema utilizando los datos de resonancia se encuentra por medio
de la ecuación [ 4 ].

                                        √1 + (2𝜉)2                                       [4]
                                𝐹𝐴𝐷 =
                                           2𝜉

                                                  √1 + (2𝜉)2
                                      41.3715 =
                                                     2𝜉

                                        𝜉 = 0.0121 = 1.21%


#### e) Función teórica de la curva de transmisibilidad

         En las Figura 38, Figura 39 y Figura 40, se presentan la curva de transmisibilidad teóricas
y experimental del edificio alto. Debido a que se obtuvieron similares valores de amortiguamiento
para los 3 casos, las gráficas siguen un comportamiento similar en todos estos, donde los puntos
rojos representan los datos experimentales y la curva azul el teórico. A pesar de que se formuló
en relación con el primer modo de resonancia, se puede apreciar como los datos experimentales
siguen la tendencia de aumentar al acercarse al segundo modo, solo que con una magnitud
menor.


**Figura 38. Curva de transmisibilidad experimental y teórica por decremento logarítmico para el edificio alto**

*Fuente: (Elaboración propia)*


**Figura 39. Curva de transmisibilidad experimental y teórica por ancho de banda para el edificio alto**
*Fuente: (Elaboración propia)*


**Figura 40. Curva de transmisibilidad experimental y teórica por resonancia para el edificio alto**
*Fuente: (Elaboración propia)*

#### f)     Función del ángulo de fase experimental y teórico

           En la Figura 41 se observa la comparativa de la variación del ángulo de fase teórico y
experimental según las frecuencias inducidas en la base. Se puede observar que los primeros
ángulos experimentales si siguen la tendencia de la curva teórica y como se explicó
anteriormente, los últimos datos son los relacionados al segundo modo, por ende, habría que
analizarlos por aparte, empezando desde los 0 grados.


**Figura 41. Comparativa de la variación del ángulo de fase teórico y experimental según las frecuencias**
                                    inducidas en la base para el edificio alto
*Fuente: (Elaboración propia)*


#### g) Comparación de frecuencias naturales

       En el Cuadro 10 se presenta un resumen comparativo de los períodos y frecuencias
naturales obtenidos mediante tres diferentes métodos para el edificio alto.

**Cuadro 10. Resumen comparativo de período y frecuencia naturales obtenidos mediante tres diferentes**
métodos para el edificio alto

               Método                       Período natural (s)         Frecuencia natural (Hz)
    Lectura directa de la curva de
                                                  0,551                         1,81488
            vibración libre
   Transformada rápida de Fourier                 0,539                         1,85547
      Curva de transmisibilidad                   0,550                         1,81820

       Del cuadro anterior, la lectura directa de la curva de vibración libre muestra un período
natural de 0,551 segundos y una frecuencia natural de 1,81488 Hz. La transformada rápida de
Fourier (FFT) ofrece un período ligeramente menor de 0,539 segundos y una frecuencia de
1,85547 Hz. La curva de transmisibilidad, por su parte, indica un período de 0,550 segundos y
una frecuencia de 1,81820 Hz. Las diferencias entre los métodos son relativamente pequeñas, lo
que sugiere que todos ellos son consistentes y válidos para la estimación de las propiedades
dinámicas del edificio alto. Sin embargo, las ligeras variaciones pueden ser atribuibles a las
diferencias en las aproximaciones y técnicas analíticas empleadas por cada método.

#### h) Comparación de los amortiguamientos

       En el Cuadro 11 se presenta un resumen comparativo del amortiguamiento obtenido
mediante tres diferentes métodos para el edificio alto.

**Cuadro 11. Resumen comparativo del amortiguamiento obtenido mediante tres diferentes métodos para el**
edificio alto

                     Método                                          Amortiguamiento
               Decremento logarítmico                                   0,0128
                  Ancho de banda                                        0,0171
                    Resonancia                                          0,0121

       Como se observa, los resultados muestran que el decremento logarítmico proporciona un
amortiguamiento de 0,0128, el cual es el valor más alto entre los métodos analizados. En
contraste, el método de ancho de banda reporta el valor más alto de amortiguamiento con
0,0171. Finalmente, el método de resonancia muestra el valor menor de 0,0121. Estas diferencias
en los resultados se deben a cómo cada método aborda y calcula el amortiguamiento del edificio.


### 3.2.2. Resultados de vibración forzada del edificio bajo


**Figura 42. Superposición de la historia de desplazamiento y aceleración del piso superior del edificio bajo**
*Fuente: (Elaboración propia)*
         De la misma manera que el edificio esbelto, como se puede observar de la Figura 42,
ambas historias (aceleración y desplazamiento) también presentan un comportamiento similar,
debido a lo mencionado anteriormente sobre la fuerza excitadora aplicada en la base. Igualmente,
la amplitud del desplazamiento sigue siendo mayor a la de la aceleración. Es de suma importancia
recalcar que, para este edificio, los valores que se toman a analizar son los que ocurren a partir
de los 450 segundos aproximadamente, es decir, el tramo final de la prueba, debido a que el
experimento se realizó de una manera continua y en los primeros segundos, se trabajaba con el
edificio alto.


**Figura 43. Superposición de la historia de desplazamiento de la base y del piso superior del edificio bajo**
*Fuente: (Elaboración propia)*


        Como se observa en la Figura 43, de mismo modo que el edificio alto, el desplazamiento
de la base refleja directamente el movimiento impuesto por la mesa vibratoria. Este sigue
funcionando como entrada de excitación para el sistema y el desplazamiento del piso superior
incorpora la respuesta dinámica del edificio bajo a esta excitación. El piso superior también
presenta una mayor amplitud de desplazamiento gracias a la amplificación de la respuesta a lo
largo de la altura del edificio, sin embargo, como esta es menor a la del edificio alto, la amplitud
de desplazamiento es de menor magnitud.

        Seguidamente, en la Figura 44, Figura 45 y Figura 46, se muestran las historias
superpuestas de desplazamiento del piso superior del edificio bajo y la base durante la vibración
forzada. Estos gráficos describen el comportamiento antes, durante y después de que el edificio
entre en resonancia.


**Figura 44. Superposición de la historia de desplazamiento de la base y del piso superior del edificio bajo**
                                          (antes de resonancia)
*Fuente: (Elaboración propia)*


**Figura 45. Superposición de la historia de desplazamiento de la base y del piso superior del edificio bajo**
                                        (durante de resonancia)
*Fuente: (Elaboración propia)*


**Figura 46. Superposición de la historia de desplazamiento de la base y del piso superior del edificio bajo**
                                        (después de resonancia)
*Fuente: (Elaboración propia)*


        En el Cuadro 12 se resumen algunos datos del ángulo experimental calculado según las
frecuencias de vibración de la base para el edificio bajo.

**Cuadro 12. Resumen datos del ángulo experimental calculado del edificio bajo**


   Frecuencia           Frecuencia            Tiempo de       ωp experimental         φ de fase
  aplicada (Hz)      experimental (Hz)        retraso (s)         (rad/s)          experimental (°)

       5,4                5,3457                    0,01          33,5880             19,2445
       5,6                5,5556                    0,01          34,9069             20,0002
       5,8                5,7637                    0,01          36,2144             20,7493
       6,0                6,0606                    0,01          38,0799             21,8182
       6,4                6,3492                    0,01          39,8932             22,8571
       6,6                6,6667                    0,01          41,8881             24,0001
       6,8                6,7797                    0,01          42,5981             24,4069
       7,0                7,0426                    0,01          44,2500             25,3534
       7,2                7,1428                    0,01          44,8795             25,7141
       7,4                7,4074                    0,01          46,5421             26,6666
       7,6                7,5417                    0,01          47,3859             27,1501
       7,8                7,7519                    0,01          48,7066             27,9068
       8,0                7,9936                    0,02          50,2253             57,5539
       8,2                8,1967                    0,02          51,5014             59,0162
       8,4                8,3333                    0,03          52,3597             89,9996
       8,6                8,5470                    0,03          53,7024             92,3076
       8,8                8,7719                    0,03          55,1155             94,7365
       9,0                9,0909                    0,03          57,1198             98,1817
       9,2                9,3457                    0,04          58,7208             134,5781
       9,4                9,5238                    0,04          59,8398             137,1427
       9,6                10,0000                   0,05          62,8319             180,0000

        Se vuelve a presentar el caso de que a medida que la frecuencia aplicada de vibración
aumenta, la frecuencia experimental del edificio bajo se aproxima a esta, justo como ocurrió con
el edificio alto, A diferencia del caso del edificio alto, para el edificio bajo solo se logró un modo
de resonancia, el cual se alcanzó a una frecuencia de 8,4 Hz, mucho mayor que la del edificio
alto, debido a su tamaño y rigidez en sus apoyos y uniones. No se presentó el problema de
sobrepasar los 180° y como se puede apreciar en la Figura 47, el ángulo de fase experimental (φ)
va aumentando progresivamente con la frecuencia aplicada y luego de la resonancia, se obtiene
el resultado esperado de que haya un desfase de 180° entre las ondas sinusoidales generadas
por la base y el piso superior del edificio bajo.


**Figura 47. Ejemplo de la variación del ángulo respecto a la frecuencia del edificio alto.**
*Fuente: (Elaboración propia)*


#### a) Análisis de amplitud estacionaria

        Del mismo modo que con el edificio esbelto, en el Cuadro 13 se presentan los datos
obtenidos de amplitud estacionaria para cada frecuencia analizada del edificio bajo. Estos datos
incluyen la frecuencia aplicada, la frecuencia experimental, la amplitud medida, el promedio de
las amplitudes y la desviación estándar correspondiente.


**Cuadro 13. Resumen datos de amplitud estacionaria medida del edificio bajo**

                              Frecuencia
           Frecuencia
                             experimental               Amplitud (mm)                 Promedio
          aplicada (Hz)
                                 (Hz)
               5,4              5,3457            0,59130            0,59440          0,59285
               5,6              5,5556            0,64519            0,64027          0,64273
               5,8              5,7637            0,70859            0,72161          0,71510
               6,0              6,0606            0,74824            0,74998          0,74911
               6,4              6,3492            0,89370            0,88986          0,89178
               6,6              6,6667            0,91805            0,91111          0,91458
               6,8              6,7797            0,96848            0,96328          0,96588
               7,0              7,0426            1,07126            1,07390          1,07258
               7,2              7,1428            1,18370            1,18397          1,18384
               7,4              7,4074            1,30271            1,30472          1,30372


                             Frecuencia
           Frecuencia
                            experimental              Amplitud (mm)               Promedio
          aplicada (Hz)
                                (Hz)
               7,6              7,5417          1,39238             1,39667        1,39453
               7,8              7,7519          1,67105             1,66895        1,67000
               8,0              7,9936          2,01923             2,02543        2,02233
               8,2              8,1967          2,03145             2,04786        2,03966
               8,4              8,3333          2,10927             2,15121        2,13024
               8,6              8,5470          2,07267             2,07559        2,07413
               8,8              8,7719          1,90578             1,90700        1,90639
               9,0              9,0909          1,60520             1,61223        1,60872
               9,2              9,3457          1,40494             1,40977        1,40736
               9,4              9,5238          1,41762             1,41944        1,41853
               9,6             10,0000          1,42719             1,42920        1,42820


#### b) Curva de transmisibilidad

       En la Figura 48, se presenta la curva de transmisibilidad de desplazamiento para los datos
experimentales del edificio bajo.


**Figura 48. Curva de transmisibilidad de desplazamiento experimental para el edificio bajo**
*Fuente: (Elaboración propia)*


#### c) Método de ancho de banda

       En la Figura 49 se muestra la forma del método de ancho de banda, junto a los valores de
importancia para usar este procedimiento.


**Figura 49. Datos y gráfica del método de ancho de banda para el edificio bajo**
*Fuente: (Elaboración propia)*


       El método de ancho de banda consiste en encontrar la amplitud máxima de la curva de
FAD para dividir dicho valor entre raíz de dos y de este modo obtener una recta constante a una
altura “y”. Los puntos de intersección entre esta recta y la curva de FAD representa los valores
de interés, de manera matemática se sigue que:

                                  𝐴𝑚𝑝𝑙𝑖𝑡𝑢𝑑 𝐹𝐴𝐷 𝑚á𝑥 = 7.1008

                                                            7.1008
                                 𝑅𝑒𝑐𝑡𝑎 𝑑𝑒 𝑖𝑛𝑡𝑒𝑟é𝑠 = 𝑦 =
                                                              √2

                                            𝑦 = 5.0210

       El amortiguamiento por el método de ancho de banda está dado por la ecuación [ 3 ]. Se
toman los valores de razones de frecuencia mostrados en la Figura 49, estos se transforman en
frecuencias reales y sustituyendo se obtiene:

                                           10.2911 − 8.5125
                                      𝜉=
                                               2(8.9286)

                                       𝜉 = 0.0996 = 9.96%


#### d) Amortiguamiento mediante prueba de resonancia

        El amortiguamiento del sistema utilizando los datos de resonancia se encuentra por medio
de la ecuación [ 4 ].

                                                     √1 + (2𝜉)2
                                          7.1008 =
                                                        2𝜉

                                          𝜉 = 0.0711 = 7.11%

#### e) Función teórica de la curva de transmisibilidad

        En la Figura 50, Figura 51 y Figura 52, se presentan la curva de transmisibilidad teórica y
experimental del edificio bajo. A diferencia del edificio alto, existe una notable diferencia entre el
amortiguamiento obtenido por la resonancia, y los obtenidos por el decremento logarítmico.
Debido a que la resonancia si toma en cuenta, indirectamente, factores como la rigidez u otros
efectos adicionales del comportamiento dinámico del edificio, se obtiene un resultado más
acercado al teórico, mostrando así cual es el valor del amortiguamiento más acertado para este
edificio.


**Figura 50. Curva de transmisibilidad experimental y teórica por decremento logarítmico para el edificio bajo**

*Fuente: (Elaboración propia)*


**Figura 51. Curva de transmisibilidad experimental y teórica por ancho de banda para el edificio bajo**
*Fuente: (Elaboración propia)*


**Figura 52. Curva de transmisibilidad experimental y teórica por resonancia para el edificio bajo**
*Fuente: (Elaboración propia)*


#### f)   Función del ángulo de fase experimental y teórico

          En la Figura 53 se observa la comparativa de la variación del ángulo de fase teórico y
experimental según las frecuencias inducidas en la base. En este caso que solo se llega al primer
modo, a diferencia del edificio alto, no hay valores que estén muy alejados de la curva teórica y
siguen la línea de tendencia de esta, en la cual va aumentando el valor del ángulo de fase en
relación con la razón de frecuencias.


**Figura 53. Comparativa de la variación del ángulo de fase teórico y experimental según las frecuencias**
                               inducidas en la base para el edificio bajo
*Fuente: (Elaboración propia)*


#### g) Comparación de frecuencias naturales

       En el Cuadro 14 se presenta un resumen comparativo de los períodos y frecuencias
naturales obtenidos mediante tres diferentes métodos para el edificio bajo.

**Cuadro 14. Resumen comparativo de período y frecuencia naturales obtenidos mediante tres diferentes**
métodos para el edificio bajo

               Método                         Período natural (s)           Frecuencia natural (Hz)
    Lectura directa de la curva de
                                                    0,112                          8,92857
            vibración libre
   Transformada rápida de Fourier                   0,111                          8,98438
      Curva de transmisibilidad                     0,112                          8,94491

       La lectura directa de la curva de vibración libre muestra un período natural de 0,112
segundos y una frecuencia natural de 8,92857 Hz. La transformada rápida de Fourier (FFT) ofrece
un período ligeramente menor de 0,111 segundos y una frecuencia de 8,98438 Hz. La curva de
transmisibilidad, por su parte, indica un período de 0,112 segundos y una frecuencia de 8,94491
Hz. Aunque las diferencias entre los métodos son mínimas, la curva de transmisibilidad muestra
una frecuencia ligeramente más alta, lo que puede deberse a su capacidad para capturar con
mayor precisión las resonancias específicas del sistema.


#### h) Comparación de los amortiguamientos

        En el Cuadro 15 presenta un resumen comparativo del amortiguamiento obtenido
mediante tres diferentes métodos para el edificio bajo.

**Cuadro 15. Resumen comparativo del amortiguamiento obtenido mediante tres diferentes métodos para el**
edificio bajo

                      Método                                           Amortiguamiento
                Decremento logarítmico                                    0,0162
                   Ancho de banda                                         0,0996
                     Resonancia                                           0,0711

        Como se observa, los resultados muestran una notable variabilidad entre los métodos
utilizados. El decremento logarítmico proporciona un amortiguamiento de 0,0162, mientras que
el método de resonancia reporta un valor mayor de 0,0711. Sin embargo, el método de ancho de
banda destaca con un valor significativamente más alto de 0,0996. Esta diferencia significativa
sugiere que el método de resonancia podría estar capturando efectos adicionales o no lineales
en el comportamiento dinámico del edificio bajo. Asimismo, podría indicar una mayor sensibilidad
del método a ciertas características estructurales.

### 3.2.3. Comparación de edificios en vibración forzada

        En el Cuadro 16 se presenta un resumen comparativo de los períodos y amortiguamientos
obtenidos en vibración forzada para ambos edificios.

**Cuadro 16. Comparativa de periodos y amortiguamientos obtenidos para cada edificio en vibración forzada**

       Vibración forzada                     Edificio alto                     Edificio bajo
          Período (s)                          0,539                              0,111
       Amortiguamiento                         0,0121                            0,0711

        Según se puede observar en el cuadro comparativo de vibración forzada, los periodos
calculados para el edificio alto son mayores a los del edificio bajo. Esta diferencia significativa en
los períodos puede ser atribuida a las características estructurales de cada edificio. El edificio
alto, siendo más esbelto, presenta un período más largo debido a su mayor flexibilidad y masa.
En contraste, el edificio bajo, siendo más compacto, tiene un período más corto debido a su menor
flexibilidad y masa.

        En cuanto al amortiguamiento, el edificio alto muestra un valor de 0,0121, lo cual es
significativamente menor que el 0,0711 del edificio bajo. Esto sugiere que el edificio bajo es más
eficiente en disipar la energía de las vibraciones, posiblemente debido a su mayor rigidez y
características de diseño que permiten un mayor amortiguamiento.


# 4. Formulación y calibración del modelo
        Para formular el modelo dinámico de un edificio es necesario conocer ciertas magnitudes
asociadas a su respuesta al movimiento. Por tanto, se deben de conocer su matriz de masa
(ecuación [ 5 ]) y su matriz de rigidez (ecuación [ 6 ]).

                                            𝑚1    0
                                     𝑚= [            ]                                        [5]
                                            0     𝑚2

                                       𝑘 + 𝑘2      −𝑘2
                                   𝑘= [ 1              ]                                      [6]
                                         −𝑘2       𝑘2

        Además, es importante conocer el planteamiento de la ecuación de movimiento del
sistema estudiado. Se conoce que la ecuación de movimiento para un sistema de masas
concentradas de dos grados de libertad, es la expresión descrita en la ecuación [ 7 ].

                          𝑚1   0 𝑢̈ 1    𝑘 + 𝑘2     −𝑘2 𝑢1     0
                      [          ][ ] + [ 1            ][ ] = [ ]                             [7]
                          0    𝑚2 𝑢̈ 2     −𝑘2      𝑘 2 𝑢2     0

        En las subsecciones siguientes, se hará la formulación y calibración del modelo dinámico
de los edificios, utilizando las ecuaciones descritas anteriormente.

## 4.1. Cálculo de las constantes de rigidez experimentales

        Para obtener valores de rigidez experimental de las torres, se utilizó la ecuación [ 8 ].

             𝑚1 ∙ 𝑚2 ∙ 𝜔𝑛4 − (𝑚1 ∙ 𝑘2 + 𝑚2 ∙ (𝑘1 + 𝑘2 )) ∙ 𝜔𝑛2 + 𝑘1 ∙ 𝑘2 = 0                  [8]


        El cálculo, se basó en formular un sistema de ecuaciones donde se conocían con
exactitud las masas y las frecuencias. Por lo tanto, es necesario conocer la información necesaria
para el cálculo. En el Cuadro 7 se recopilan los datos acerca de los periodos experimentales
calculados con la nube de puntos y la TRF. En el Cuadro 17, se muestran las masas concentradas
por nivel de cada edificio.
**Cuadro 17. Masas concentradas en cada edificio, distribuidas por nivel**

                                                           Masas por edificio (kg)
              Nivel
                                                  Alto                                Bajo
                1                                0,6354                              1,1579
                2                                0,6354                              0,6354

        Teniendo los datos necesarios para hacer el cálculo, es necesario recordar que la
ecuación [ 8 ] utiliza frecuencias circulares, por lo que están en unidades de radián entre segundo.
En la ecuación [ 9 ] se muestra como calcular la frecuencia circular a partir del periodo.


                                                    2𝜋
                                             𝜔𝑛 =                                             [9]
                                                    𝑇𝑛


            Dado el planteamiento inicial para poder calcular las constantes de rigidez
experimentales, se procede primero con el edificio bajo. Basándose en la ecuación [ 9 ] y la
información recopilada en el Cuadro 7, se elaboró el Cuadro 18.

**Cuadro 18. Frecuencias angulares modales de ambos edificios**

                                     Método de                   Frecuencia angular (rad/s)
             Edificio
                                      obtención           Modo fundamental       Segundo modo
                                   Nube de puntos             11,403                  29,778
                 Alto            Transformada rápida
                                                                11,657                 30,063
                                      de Fourier
                                   Nube de puntos               56,100                 184,800
                 Bajo            Transformada rápida
                                      de Fourier                56,605                 139,626

            Dado que se conocen dos pares de frecuencias por cada edificio, se realizó el siguiente
planteamiento. Basándose en la ecuación [ 8 ], se elaboró el planteamiento de los sistemas de
ecuaciones no lineales (abreviado como SENL), que se encuentra en el Cuadro 19.

**Cuadro 19. Planteamiento de sistemas de ecuaciones no lineales para ambos edificios**

                 Planteamiento del SENL para el edificio bajo, con ωn de la nube de puntos


             1,1579 ∙ 0,6354 ∙ 56,14 − (1,1579 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 56,12 + 𝑘1 ∙ 𝑘2 = 0
          {
            1,1579 ∙ 0,6354 ∙ 184,84 − (1,1579 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 184,82 + 𝑘1 ∙ 𝑘2 = 0

     Planteamiento del SENL para el edificio bajo, con ωn de la transformada rápida de Fourier


          1,1579 ∙ 0,6354 ∙ 56,6054 − (1,1579 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 56,6052 + 𝑘1 ∙ 𝑘2 = 0
     {
         1,1579 ∙ 0,6354 ∙ 139,6264 − (1,1579 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 139,6262 + 𝑘1 ∙ 𝑘2 = 0

                  Planteamiento del SENL para el edificio alto, con ωn de la nube de puntos


                0,63542 ∙ 11,4034 − (0,6354 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 11,4032 + 𝑘1 ∙ 𝑘2 = 0
            {
                0,63542 ∙ 29,7784 − (0,6354 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 29,7782 + 𝑘1 ∙ 𝑘2 = 0

     Planteamiento del SENL para el edificio alto, con ωn de la transformada rápida de Fourier

                0,63542 ∙ 11,6574 − (0,6354 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 11,6572 + 𝑘1 ∙ 𝑘2 = 0
            {
                0,63542 ∙ 30,0634 − (0,6354 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 30,0632 + 𝑘1 ∙ 𝑘2 = 0


        Para resolver dichos sistemas, se buscó dejar una variable en función de la otra para así
poder ingresar la relación a la segunda ecuación. Al resolver dichos sistemas, se encontraron dos
pares de soluciones (k1 y k2) por cada planteamiento. Los pares de soluciones se encuentran
clasificados por el método por el que fue obtenida la frecuencia angular. La información
mencionada se encuentra en el Cuadro 20.

**Cuadro 20. Resultados de la resolución de los sistemas de ecuaciones no lineales planteados a partir de**
las frecuencias angulares modales de los edificios
                                                 Numero de         Constante de rigidez (N/m)
      Edificio             Método
                                              solución al SENL        k1                 k2
                                                      1            216,988           214,530
                       Nube de puntos
                                                      2            429,060           108,494
        Alto            Transformada                  1            234,024           207,873
                          rápida de
                                                     2             415,745              117,012
                           Fourier
                                                     1            6001,710            13175,646
                       Nube de puntos
                                                     2            37185,900           2126,522
        Bajo            Transformada                 1            6584,328            6979,898
                          rápida de
                                                     2            19699,478             2332,95
                           Fourier

        A su vez, se probó la exactitud de los resultados, reingresando los valores a los sistemas
almacenados en el Cuadro 19. La solución más exacta al sistema es aquella que aproxime las
igualdades más cerca del cero. Por lo tanto, para considerar el efecto de todas las posibles
soluciones, se hizo una suma de los residuos de cada modo de vibración en valor absoluto. En el
Cuadro 21 se compara la información mencionada anteriormente.

**Cuadro 21. Comparación de los resultados de la resolución de los sistemas de ecuaciones no lineales**
planteados a partir de las frecuencias angulares modales de los edificios

                                                                     Residuos
   Edificio         Método           Resultado
                                                     Modo fundamental Segundo modo    Suma
                                          1              -0,0103          -0,0881    0,0984
                 Nube de puntos
                                          2              -0,0103          -0,0881    0,0984
    Alto
                                          1              -0,1060        5287,0599  5287,1659
                    Fourier
                                          2              -0,1367        5287,5172  5287,6539
                                          1              -4,3586        1757,3809  1761,7395
                 Nube de puntos
                                          2              97,1373        594,0821    691,2194
    Bajo
                                          1              -3,3735         -67,0188   70,3923
                    Fourier
                                          2             -26,2662          0,3162    26,5825

        En el cuadro anterior, se resaltaron en verde las respectivas soluciones (del edificio alto y
bajo), con el error más pequeño. En resumen, se concluye que para el edifico alto, la solución


más exacta es el segundo par de constantes extraídas de las frecuencias de la nube de puntos.
En el caso del edificio bajo, el par de soluciones más exacto fue es del segundo cálculo en base
a las frecuencias angulares obtenidas del espectro de Fourier. A modo de resumen, se muestra
el Cuadro 22 con todos los resultados.

**Cuadro 22. Cuadro resumen de las constantes de rigidez obtenidas experimentalmente**

                                                      Constante de rigidez (N/m)
             Edificio
                                                  k1                              k2
               Alto                            429,060                         108,494
               Bajo                           19699,478                        2332,950


## 4.2. Formulación y calibración del modelo dinámico del edificio bajo

        Primeramente, se expresará la matriz de masas, así como en la ecuación [ 5 ]. Para el
edificio bajo, se utilizaron dos masas distintas. En el nivel inferior, se utilizó una masa de 1,1579
kg, mientras que el segundo nivel fue cargado con una masa de 0,6354 kg. Se supone la
estructura como un modelo de masas concentradas y se deprecia la participación de la masa de
la estructura. Lo anterior, se asume dado que las masas concentradas de los pesos son muy
superiores al aporte de las vigas y columnas. La matriz de masa del edifico bajo es:

                                                      1,1579    0
                               𝑚𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑏𝑎𝑗𝑜 (𝑘𝑔) = [             ]
                                                         0   0,6354

        En el caso de la matriz de rigidez, se utilizaron los datos previamente estudiados que se
encuentran en el Cuadro 22. Por tanto, así como se muestra en la ecuación [ 6 ], la matriz de
rigidez para el edificio bajo es:

                                             19699,478 + 2332,950 −2332,950
                  𝑘𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑏𝑎𝑗𝑜 (𝑁/𝑚) = [                                 ]
                                                  −2332,950       2332,950

                                           𝑁      22032,428 −2332,950
                           𝑘𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑏𝑎𝑗𝑜 ( ) = [                     ]
                                           𝑚     −2332,950 2332,950

        Habiendo obtenido las matrices anteriores, se procede con el análisis de valores y
vectores propios de las matrices de masa y rigidez. Dicho análisis de hace utilizando la ecuación
[ 10 ]. El procedimiento arroja por resultado un vector λ que contiene el cuadrado de las
frecuencias naturales modales del sistema.

                          𝑘 + 𝑘2    −𝑘2         𝑚    0      𝑎1     0
                        {[ 1            ] − 𝜆𝑛 [ 1      ]} [𝑎 ] = [ ]                       [ 10 ]
                            −𝑘2     𝑘2          0    𝑚2      2     0


Para el edificio bajo se tiene que:

                                                                     𝑎1     0
                              {𝑘𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑏𝑎𝑗𝑜 − 𝜆𝑛 𝑚𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑏𝑎𝑗𝑜 } [𝑎 ] = [ ]
                                                                      2     0

                       22032,428 −2332,950          1,1579    0       𝑎1     0
                    {[                     ] − 𝜆𝑛 [               ]} [𝑎 ] = [ ]
                      −2332,950 2332,950               0   0,6354      2     0

                                      𝑟𝑎𝑑 2   𝜔2        3,204 × 103
                                  𝜆𝑛 (   ) = [ 12 ] = [             ]
                                       𝑠      𝜔2        1,950 × 104

           Habiendo obtenido los valores de la frecuencia circular natural del edificio bajo, se deben
de comparar con los obtenidos a partir de la prueba de vibración libre. En el Cuadro 23 se recopila
la comparación de las frecuencias obtenidas, comparando el método de valores propios, la
transformada rápida de Fourier y la nube de puntos (datos medidos).

**Cuadro 23. Comparación de la frecuencia angular de oscilación obtenida para el edifico bajo en vibración**
libre
                                                      Frecuencia angular (rad/s)
           Método utilizado
                                            Modo fundamental               Segundo modo
        Nube de puntos                          56,100                        184,800
    Transformada rápida de
                                                  56,605                          139,626
            Fourier
   Vectores y valores propios                     56,605                          139,626

           Con las frecuencias angulares obtenidas, es posible replantear la matriz de rigidez del
edificio utilizando la ecuación [ 8 ]. Los términos ωn tienen unidades de radianes entre segundos.
Se plantea el siguiente sistema considerando ambas frecuencias:

         0,6354 ∙ 1,1579 ∙ 56,6054 − (0,6354 ∙ 𝑘2 + 1,1579 ∙ (𝑘1 + 𝑘2 )) ∙ 56,6052 + 𝑘1 ∙ 𝑘2 = 0
    {
        0,6354 ∙ 1,1579 ∙ 139,6264 − (0,6354 ∙ 𝑘2 + 1,1579 ∙ (𝑘1 + 𝑘2 )) ∙ 139,6262 + 𝑘1 ∙ 𝑘2 = 0

           Las frecuencias encontradas a partir del análisis de vectores y valores propios son
idénticas a aquellas calculadas a partir de los datos experimentales. Específicamente, si se
observa el Cuadro 23, los valores de frecuencia angular de oscilación, para ambos modos, son
iguales a los calculados con la TRF. A su vez, se puede observar que el planteamiento del sistema
de dos ecuaciones no lineales anterior, ya se había considerado en la primera subsección de este
apartado.
           Concretamente, ya que en el apartado: “Planteamiento del SENL para el edificio bajo, con
ωn de la transformada rápida de Fourier” del Cuadro 19, se había resulto el sistema que surgió
de las frecuencias encontradas con los valores propios, se omite el replanteo de las constantes


de rigidez. Conociendo lo anterior, el modelo ya se encuentra calibrado. Por tanto, siguiendo la
formulación propuesta en la ecuación [ 7 ], la ecuación de movimiento calibrada para el edificio
bajo es:

                    0,6354    0     𝑢̈      22032,428 −2332,950 𝑢1     0
                   [             ] [ 1] + [                    ][ ] = [ ]
                       0   1,1579 𝑢̈ 2      −2332,950 2332,950 𝑢2      0

        Dicha ecuación, satisface una frecuencia circular para el modo fundamental con un valor
de 56,605 (rad/s), así como una para el segundo modo, con valor de 139,626 (rad/s). En la Figura
54, se muestra una representación visual de las formas modales del edificio bajo.


**Figura 54. Formas modales del edificio bajo**
*Fuente: (Elaboración propia)*


## 4.3. Formulación y calibración del modelo dinámico del edificio alto

        Al igual que con la subsección anterior, se expresa la matriz de masas del edificio alto,
acorde a la ecuación [ 5 ]. Para el edificio alto, se utilizaron dos pesos con la misma masa, 0,6354
kg. Así como con el edificio bajo, se supone la estructura como un modelo de masas
concentradas y se deprecia la participación de la masa de la estructura. La matriz de masa del
edifico alto es:

                                                    0,6354    0
                             𝑚𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑎𝑙𝑡𝑜 (𝑘𝑔) = [              ]
                                                       0   0,6354

        En el caso de la matriz de rigidez, se utilizarán los valores de las constantes de rigidez,
obtenidas en la primera subsección de este apartado. La información de forma más condensada


se encuentra en el Cuadro 22. Por tanto, así como se muestra en la ecuación [ 6 ], la matriz de
rigidez para el edificio alto es:

                                               429,060 + 108,494 −108,494
                       𝑘𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑎𝑙𝑡𝑜 (𝑁/𝑚) = [                           ]
                                                   −108,494      108,494

                                                     537,554 −108,494
                            𝑘𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑎𝑙𝑡𝑜 (𝑁/𝑚) = [                  ]
                                                    −108,494 108,494

        Habiendo obtenido la matriz de rigidez, se procede con el análisis de valores y vectores
propios de las matrices de masa y rigidez. Dicho análisis de hace utilizando la ecuación [ 10 ]. El
procedimiento arroja por resultado un vector λ que contiene el cuadrado de las frecuencias
naturales modales del sistema. Para el edificio alto se tiene que:

                                                                    𝑎1     0
                             {𝑘𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑎𝑙𝑡𝑜 − 𝜆𝑛 𝑚𝐸𝑑𝑖𝑓𝑖𝑐𝑖𝑜 𝑎𝑙𝑡𝑜 } [𝑎 ] = [ ]
                                                                     2     0

                        537,554 −108,494        0,6354    0      𝑎1    0
                     {[                 ] − 𝜆𝑛 [             ]} [ ] = [ ]
                       −108,494 108,494            0   0,6354 𝑎2       0

                                        𝑟𝑎𝑑 2   𝜔2        130,028
                                    𝜆𝑛 (   ) = [ 12 ] = [         ]
                                         𝑠      𝜔2        886,730

        Con los nuevos valores para las frecuencias de oscilación del edificio alto, es pertinente
compararlos con aquellos obtenidos en la prueba de vibración libre. En el Cuadro 24 se recopila
la comparación de las frecuencias obtenidas, comparando el método de valores propios, la
transformada rápida de Fourier y la nube de puntos (datos medidos).

**Cuadro 24. Comparación de la frecuencia angular de oscilación obtenida para el edifico alto en vibración**
libre
                                                    Frecuencia angular (rad/s)
        Método utilizado
                                          Modo fundamental               Segundo modo
        Nube de puntos                        11,403                         29,778
    Transformada rápida de
                                                 11,657                           30,063
            Fourier
   Vectores y valores propios                    11,403                           29,778

        Con las frecuencias circulares naturales obtenidas, es posible replantear la matriz de
rigidez del edificio utilizando la ecuación [ 8 ]. Se tiene el siguiente planteamiento con las
frecuencias obtenidas:
             0,63542 ∙ 11,4034 − (0,6354 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 11,4032 + 𝑘1 ∙ 𝑘2 = 0
         {
             0,63542 ∙ 29,7784 − (0,6354 ∙ 𝑘2 + 0,6354 ∙ (𝑘1 + 𝑘2 )) ∙ 29,7782 + 𝑘1 ∙ 𝑘2 = 0


        En el caso del edificio alto, el análisis de vectores y valores propios arrojó valores idénticos
a una de las instancias experimentales. Así como se puede observar en el Cuadro 24, se
obtuvieron las mismas frecuencias angulares que las que arrojó la nube de puntos. El replanteo
que se debería de hacer se puede omitir, ya que en el apartado “Planteamiento del SENL para el
edificio alto, con ωn de la nube de puntos” del Cuadro 19 ya se probaron los valores encontrados.
        Según lo comentado anteriormente, se puede contemplar que el resultado es invariante
al considerar las frecuencias obtenidas de los valores propios de la ecuación [ 10 ]. Por tanto,
siguiendo la formulación propuesta en la ecuación [ 7 ], la ecuación de movimiento calibrada para
el edificio alto es:

                           0,6354    0     𝑢̈      537,554 −108,494 𝑢1     0
                       [                ] [ 1] + [                 ][ ] = [ ]
                              0   0,6354 𝑢̈ 2     −108,494 108,494 𝑢2      0

        Dicha ecuación, satisface una frecuencia circular para el modo fundamental con un valor
de 11,403 (rad/s), así como una para el segundo modo, con valor de 29,778 (rad/s). En la Figura
55, se muestra una representación visual de las formas modales del edificio alto.


**Figura 55. Formas modales del edificio alto**
*Fuente: (Elaboración propia)*


# 5. Simulación numérica de la respuesta del edificio ante solicitaciones
     sísmicas aplicadas
        En esta sección, se presenta un análisis detallado de la respuesta de dos tipos de edificios
(alto y bajo) ante el sismo de Samara. La simulación numérica se realizó utilizando un modelo que
permite evaluar la respuesta dinámica de los edificios bajo condiciones sísmicas específicas. A
continuación, se muestran los resultados obtenidos.


## 5.1. Resultados sismo Samara en el edificio alto

        En esta subsección, se detallan los resultados de la simulación para un edificio alto. Las
gráficas presentadas permiten observar cómo el edificio responde a la solicitación sísmica
aplicada.


**Figura 56. Historia de aceleración en la mesa vibratoria**

*Fuente: (Elaboración propia)*

        En la Figura 56, se muestra la historia de aceleración registrada en la mesa vibratoria
durante la simulación del sismo de Samara. Esta información es crucial para entender la base de
las solicitaciones aplicadas al edificio.


**Figura 57. Historia de la aceleración del piso superior del edificio alto**

*Fuente: (Elaboración propia)*

        La Figura 57 presenta la historia de la aceleración en el piso superior del edificio alto. Aquí
se puede observar cómo se transmite la aceleración desde la base hasta el punto más alto del


edificio, permitiendo analizar el comportamiento dinámico en términos de amplificación de la
aceleración.


**Figura 58. Historia de desplazamiento relativo del piso superior respecto a la base para el edificio alto**

*Fuente: (Elaboración propia)*

        En la Figura 58, se ilustra el desplazamiento relativo del piso superior con respecto a la
base del edificio alto. Esta gráfica es fundamental para evaluar la deformación total del edificio
bajo el sismo, lo que es clave para el diseño estructural y la seguridad sísmica.


**Figura 59. Respuestas del primer y segundo modo ante impulso unitario para el edificio alto**

*Fuente: (Elaboración propia)*


       La Figura 59 muestra las respuestas del primer y segundo modo del edificio alto ante un
impulso unitario. Estos modos son esenciales para comprender las frecuencias naturales del
edificio y cómo cada modo contribuye a la respuesta total.


**Figura 60. Respuestas del primer y segundo modo ante el sismo para el edificio alto**

*Fuente: (Elaboración propia)*
       La Figura 60 presenta las respuestas del primer y segundo modo del edificio alto
específicamente ante el sismo de Samara. Esta información es vital para ver cómo las frecuencias
naturales del edificio interactúan con el contenido de frecuencias del sismo.


**Figura 61. Desplazamiento del primer y segundo modo ante el sismo para el edificio alto**
                               experimental
*Fuente: (Elaboración propia)*


        En la Figura 61, se ilustra el desplazamiento asociado con el primer y segundo modo del
edificio alto durante el sismo. Este análisis permite identificar cuál de los modos es dominante en
la respuesta del edificio.


**Figura 62. Comparación del desplazamiento total y el contribuido por el primer piso para el edificio alto**

*Fuente: (Elaboración propia)*

        Finalmente, la Figura 62 compara el desplazamiento total del edificio con el desplazamiento
contribuido únicamente por el primer piso. Esta comparación ayuda a entender la distribución de
deformaciones a lo largo de la altura del edificio.

## 5.2. Resultados sismo Samara en el edificio bajo

        En esta subsección, se presentan los resultados obtenidos para un edificio bajo las
mismas condiciones de sismo. Las gráficas permiten comparar y contrastar las respuestas de
edificios de diferentes alturas.


**Figura 63. Historia de la aceleración del piso superior del edificio bajo**

*Fuente: (Elaboración propia)*

       La Figura 63 muestra la historia de la aceleración en el piso superior del edificio bajo. Esta
gráfica es clave para observar cómo se comporta un edificio más bajo en términos de transmisión
y amplificación de aceleraciones.


**Figura 64. Historia de desplazamiento relativo del piso superior respecto a la base para el edificio bajo**

*Fuente: (Elaboración propia)*

       En la Figura 64, se presenta el desplazamiento relativo del piso superior respecto a la base
del edificio bajo. Este análisis es crucial para evaluar la deformación del edificio y su seguridad
estructural durante el sismo.


**Figura 65. Respuestas del primer y segundo modo ante impulso unitario para el edificio bajo**

*Fuente: (Elaboración propia)*
       La Figura 65 ilustra las respuestas del primer y segundo modo del edificio bajo ante un
impulso unitario. Este análisis permite comprender las frecuencias naturales y la contribución de
cada modo a la respuesta global del edificio.


**Figura 66. Respuestas del primer y segundo modo ante el sismo para el edificio bajo**

*Fuente: (Elaboración propia)*
       En la Figura 66, se muestran las respuestas del primer y segundo modo del edificio bajo
específicamente ante el sismo de Samara. Esta información es fundamental para entender cómo
los modos naturales del edificio interactúan con las frecuencias del sismo.


**Figura 67. Desplazamiento del primer y segundo modo ante el sismo para el edificio bajo**

*Fuente: (Elaboración propia)*


        La Figura 67 presenta el desplazamiento asociado con el primer y segundo modo del
edificio bajo durante el sismo. Este análisis ayuda a identificar el modo dominante en la respuesta
del edificio bajo.


**Figura 68. Comparación del desplazamiento total y el contribuido por el primer piso para el edificio bajo**

*Fuente: (Elaboración propia)*
        Finalmente, la Figura 68 compara el desplazamiento total del edificio bajo con el
desplazamiento contribuido únicamente por el primer piso. Esta comparación es esencial para
entender la distribución de deformaciones y la respuesta global del edificio bajo en comparación
con el edificio alto.


## 5.3. Estudio y análisis de las historias

        En esta sección se presentan los resultados del estudio y análisis de las historias sísmicas
simuladas, utilizando el edificio alto y el edificio bajo en el contexto del sismo de Samara.

**Cuadro 25. Comparación del edificio alto ante el sismo de Samara**

 Aceleración
                              Desplazamiento                  Aceleración
 máxima de        Tiempo                           Tiempo                     Tiempo     ¿Colapso
                              máximo relativo                 piso superior
  la mesa            (s)                              (s)                        (s)      o daño?
                                  (mm)                            (m/s2)
   (m/s2)
                                                                                          No hubo
     7,49378         18,27        61,362           21,37           8,67217     17,10     colapso ni
                                                                                           daños

        Como se observa en el Cuadro 25 simulación del sismo de Samara para el edificio alto
mostró una aceleración máxima de la mesa de 7,49378 m/s², alcanzada en los primeros 18,27
segundos del evento sísmico. El desplazamiento máximo relativo del edificio alto fue de 61,362
mm, registrado a los 21,37 segundos. La aceleración máxima en el piso superior fue de 8,67217
m/s², detectada a los 17,10 segundos.

        A pesar de estas cifras de aceleración y desplazamiento, el edificio alto no sufrió colapso
ni daños estructurales. Esto sugiere que el diseño estructural del edificio alto fue efectivo para
absorber y disipar la energía sísmica generada por el sismo de Samara. Además, la respuesta del
edificio alto indica que las frecuencias sísmicas predominantes pudieron haber estado en sintonía
con la capacidad de amortiguación de la estructura, permitiendo una mayor estabilidad durante
el evento sísmico.

**Cuadro 26. Comparación del edificio bajo ante el sismo de Samara**

 Aceleración
                              Desplazamiento                  Aceleración
 máxima de        Tiempo                           Tiempo                     Tiempo     ¿Colapso
                              máximo relativo                 piso superior
  la mesa            (s)                              (s)                        (s)      o daño?
                                  (mm)                            (m/s2)
   (m/s2)
                                                                                          No hubo
     7,49378         18,27        3,69245          18,07           18,7236     20,23     colapso ni
                                                                                           daños

        De manera similar, según los datos mostrados en el Cuadro 26, la simulación del sismo
de Samara para el edificio bajo presentó una aceleración máxima de la mesa de 7,49378 m/s²,
alcanzada en el mismo tiempo de 18,27 segundos que el edificio alto. Sin embargo, el
desplazamiento máximo relativo del edificio bajo fue ligeramente mayor, con 3,69245 mm
registrado a los 18,07 segundos. La aceleración máxima en el piso superior del edificio bajo fue
significativamente mayor, con 18,7236 m/s², registrada a los 20,23 segundos.


        A pesar de estas elevadas cifras de aceleración y desplazamiento, el edificio bajo tampoco
sufrió colapso ni daños estructurales. Esto indica que, al igual que el edificio alto, el edificio bajo
posee una estructura capaz de absorber y disipar eficientemente la energía sísmica. La mayor
aceleración en el piso superior del edificio bajo podría estar relacionada con su menor altura y
mayor rigidez, permitiendo una mejor adaptación a las frecuencias del sismo.

## 5.4. Comparación con la respuesta experimental
  Para ambos compararon historia de desplazamiento experimental absoluta
  (historia azul) con la roja que no sé qué es... aquí se enredaron con las historias
        En la siguiente sección se presentan las comparaciones entre los resultados obtenidos de
los modelos numéricos y los datos experimentales para los desplazamientos relativos de los
edificios alto y bajo, así como se muestran las figuras correspondientes.

        En la Figura 69 se muestra la superposición la curva de desplazamiento relativo del piso
superior del edificio alto. La curva azul corresponde a la predicción teórica obtenida mediante la
integración numérica de Duhamel, mientras que la curva roja muestra la historia experimental del
desplazamiento relativo.


**Figura 69. Superposición del desplazamiento relativo del edificio alto y la historia experimental del**
                                           desplazamiento

*Fuente: (Elaboración propia)*

        Se puede observar que ambas curvas (teórica y experimental) si bien no son iguales,
presentan un comportamiento similar en términos de la amplitud. De modo que los patrones de
desplazamiento general presentan similitud a lo largo del tiempo.


         La similitud entre los resultados teóricos y experimentales indica que la teoría basada en
la integración de Duhamel es relativamente precisa para predecir el comportamiento del edificio
ante las condiciones del sismo. Por lo tanto, el modelo teórico proporciona una representación
confiable para visualizar el comportamiento promedio del desplazamiento relativo a lo largo del
sismo.

         En la Figura 70 muestra la superposición de las curvas de desplazamiento relativo e
historia experimental del edificio bajo.


**Figura 70. Superposición del desplazamiento relativo del edificio bajo y la historia experimental del**
                                            desplazamiento

*Fuente: (Elaboración propia)*

         A diferencia del edificio alto, se pueden observar diferencias significativas entre las curvas
teórica y experimental. La diferencia más notoria es que la curva teórica muestra un
desplazamiento menor en comparación con la curva experimental. Las divergencias sugieren que
el modelo teórico no representa adecuadamente el comportamiento dinámico del edificio bajo
ante el sismo. Es posible que factores como la alta rigidez del edificio debido al método
constructivo y sus dimensiones (era muy bajo) no estén adecuadamente consideradas en el
modelo teórico o modificaran significativamente el historial experimental.


# 6. Conclusiones
       La caracterización dinámica de ambos edificios y sus debidas simulaciones realizadas en
el software Matlab fueron herramientas muy importantes para poder llegar a distintas
conclusiones. Primeramente, en el estudio de vibración libre se demostró que el edificio chato
presenta mayor rigidez, menor desplazamiento, un periodo fundamental menor y frecuencias
naturales más altas en comparación al edificio esbelto.

       Seguidamente, el análisis realizado en vibración forzada muestra que el edificio chato es
más eficiente a la hora de disipar energía y por ende el edificio esbelto se comporta como una
estructura mucho más flexible presentando de esa manera periodos más largos; debido a este
estudio se concluyó que el edificio chato presenta un mayor coeficiente de amortiguamiento.

       Finalmente, el estudio realizado en historias sísmicas, comprueban que ambos edificios,
alto y bajo, demostraron una excelente capacidad de resistencia ante los sismos principalmente
con el sismo de Samara; donde ambos edificios no presentaron colapso ni daños significativos.
Destacando la eficacia de sus diseños estructurales en la absorción y disipación de la energía
sísmica, con el fin de garantizar la estabilidad y seguridad de las estructuras durante el evento
sísmico.

