# Vibraciones Mecánicas - Lección 1: Introducción

**Archivo fuente:** `CHOPRA-Tema 1 Introducción (1).pdf`  
**Tipo de documento:** diapositivas de clase.  
**Curso indicado en el documento:** IC-0502, Vibraciones Mecánicas.  
**Fecha indicada en portada:** 8 de junio de 2026.  
**Uso recomendado:** contexto para explicar sistemas de un grado de libertad, formulación de ecuaciones de movimiento, fuerza externa, excitación sísmica, amortiguamiento, rigidez y métodos básicos de solución.

## Cita IEEE sugerida

[1] Universidad de Costa Rica, “Vibraciones Mecánicas: Lección 1, Introducción,” material de clase IC-0502, I Semestre 2026, 8 jun. 2026.

> Nota: el PDF no muestra autor personal en la portada. Por eso se usa la institución como autor corporativo.

---

## 1. Objetivo general de la lección

La lección introduce la forma en que se idealizan estructuras sencillas para analizarlas dinámicamente. El enfoque principal es el **sistema de un grado de libertad (UGL)**, que representa muchos problemas estructurales básicos mediante una masa concentrada, una rigidez lateral y un mecanismo de amortiguamiento.

El documento desarrolla:

- idealización de estructuras reales como sistemas UGL;
- definición de grados de libertad;
- relación fuerza-desplazamiento;
- fuerza de amortiguamiento;
- ecuación de movimiento por fuerza externa;
- ecuación de movimiento por excitación sísmica;
- combinación de respuestas estáticas y dinámicas;
- métodos de solución de la ecuación diferencial.

---

## 2. Estructuras sencillas como sistemas UGL

Una estructura sencilla puede representarse como un sistema con:

- una masa concentrada $m$;
- una estructura de rigidez $k$ sin masa;
- movimiento lateral representado por una sola coordenada $u(t)$.

La ecuación básica de vibración libre no amortiguada es:

$$
m\ddot{u}+ku=0
$$

Ejemplos usados en las diapositivas:

1. una pérgola;
2. un tanque elevado;
3. un pórtico de laboratorio.

Estas estructuras son “sencillas” porque su deformada puede describirse de forma aproximada con una sola variable de desplazamiento.

---

## 3. Ejemplos visuales de la lección

### 3.1 Pérgola dañada por sismo

El documento muestra una pérgola del Hotel Macuto-Sheraton, cerca de Caracas, Venezuela, dañada por el terremoto del 29 de julio de 1967. La descripción indica que el sismo tuvo magnitud 6.5 y que su epicentro estuvo a unos 25 km del hotel. El daño ocurrió por sobreesfuerzo en columnas de tubos de acero.

**Idea técnica:** estructuras aparentemente simples pueden tener una respuesta dinámica importante durante un sismo.

### 3.2 Tanque elevado

Se muestra un tanque de concreto reforzado sobre una columna única de 12 m de altura, ubicado en el Aeropuerto de Valdivia. Cuando el tanque está lleno, puede analizarse como un sistema de un grado de libertad.

**Idea técnica:** la masa de agua y tanque se puede idealizar como una masa concentrada, y la columna como una rigidez lateral.

### 3.3 Pruebas de laboratorio

El documento presenta pórticos de aluminio y plexiglás montados en una mesa vibratoria usada para docencia. También muestra registros de vibración libre. El modelo de plexiglás presenta una caída de amplitud más rápida, lo cual evidencia mayor amortiguamiento.

---

## 4. Grados de libertad

Un **grado de libertad** es el número de desplazamientos independientes necesarios para definir la posición o configuración deformada de una masa con respecto a una configuración de referencia.

Para un sistema UGL, basta una sola coordenada:

$$
u(t)
$$

Esta coordenada representa el desplazamiento relativo de la masa respecto a una posición de referencia.

---

## 5. Tipos de excitación dinámica en un sistema UGL

El documento distingue dos tipos principales de excitación dinámica:

### 5.1 Fuerza externa lateral

La estructura recibe una fuerza aplicada directamente sobre la masa:

$$
p(t)
$$

La ecuación del movimiento se formula en términos de esa fuerza externa.

### 5.2 Movimiento sísmico del terreno

La base de la estructura se mueve debido a un sismo. El movimiento basal se representa como:

$$
u_g(t)
$$

En este caso, la excitación se incorpora como una fuerza sísmica efectiva.

---

## 6. Relación fuerza-desplazamiento

La relación entre la fuerza resistente de la estructura y el desplazamiento puede ser:

### 6.1 Lineal

En el caso lineal:

$$
f_S=ku
$$

Donde:

- $f_S$ es la fuerza de restauración o fuerza elástica;
- $k$ es la rigidez lateral;
- $u$ es el desplazamiento.

La gráfica fuerza-desplazamiento es una línea recta.

### 6.2 No lineal

En el caso no lineal, la fuerza resistente ya no es proporcional al desplazamiento. La relación puede presentar ciclos histeréticos, plastificación o pérdida de rigidez.

En forma general:

$$
f_S=f_S(u)
$$

Para análisis inelástico, la ecuación de movimiento debe usar directamente la relación fuerza-desplazamiento no lineal.

---

## 7. Fuerza de amortiguamiento

El amortiguamiento representa mecanismos de disipación de energía. En estructuras reales, esta disipación puede provenir de:

- fricción en conexiones de acero;
- apertura y cierre de microgrietas en concreto;
- fricción entre la estructura y elementos no estructurales;
- fricción interna del material cuando se deforma;
- ciclos de carga y descarga.

Como es difícil modelar todos los mecanismos reales, se usa un modelo simplificado de **amortiguamiento viscoso equivalente**.

---

## 8. Modelo viscoso lineal

El modelo viscoso lineal expresa la fuerza de amortiguamiento como:

$$
f_D=c\dot{u}
$$

Donde:

- $f_D$ es la fuerza de amortiguamiento;
- $c$ es el coeficiente de amortiguamiento viscoso equivalente;
- $\dot{u}$ es la velocidad.

Este modelo se usa para representar la disipación de energía dentro del rango elástico lineal de la estructura.

---

## 9. Disipación por comportamiento inelástico

Cuando la estructura entra en comportamiento inelástico, se disipa energía adicional.

En ese caso, la disipación se considera mediante la curva fuerza-desplazamiento real del sistema. La energía disipada en un ciclo entre los límites de deformación $\pm u_o$ corresponde al área encerrada por el ciclo histerético.

**Idea clave:** en sistemas lineales se puede usar $f_D=c\dot{u}$; en sistemas inelásticos la relación fuerza-desplazamiento debe incluir el comportamiento histerético.

---

## 10. Ecuación de movimiento por fuerza externa

Para un sistema UGL sometido a una fuerza externa $p(t)$, las fuerzas que actúan sobre la masa son:

- fuerza externa: $p(t)$;
- fuerza de restauración: $f_S$;
- fuerza de amortiguamiento: $f_D$;
- fuerza inercial: $m\ddot{u}$.

Aplicando la segunda ley de Newton:

$$
p(t)-f_S-f_D=m\ddot{u}
$$

Reordenando:

$$
m\ddot{u}+f_D+f_S=p(t)
$$

---

## 11. Caso elástico lineal

Si el sistema es lineal:

$$
f_D=c\dot{u}
$$

$$
f_S=ku
$$

Entonces:

$$
m\ddot{u}+c\dot{u}+ku=p(t)
$$

Esta es la ecuación clásica del sistema masa-resorte-amortiguador de un grado de libertad.

---

## 12. Caso inelástico

Para un sistema inelástico:

$$
m\ddot{u}+c\dot{u}+f_S(u)=p(t)
$$

Aquí $f_S(u)$ no necesariamente es proporcional a $u$. Puede depender de la historia de carga y descarga.

---

## 13. Principio de D'Alembert

La ecuación de movimiento también se puede formular mediante equilibrio dinámico incluyendo una fuerza inercial ficticia:

$$
f_I=-m\ddot{u}
$$

Al considerar esta fuerza, el cuerpo libre queda en equilibrio:

$$
f_I+f_D+f_S-p(t)=0
$$

Esto es equivalente a:

$$
m\ddot{u}+f_D+f_S=p(t)
$$

---

## 14. Componentes puros del sistema dinámico

El sistema se puede visualizar como la combinación de tres componentes ideales:

1. **Rigidez:** marco sin masa ni amortiguamiento.
2. **Amortiguamiento:** marco sin rigidez ni masa.
3. **Masa:** masa sin rigidez ni amortiguamiento.

La respuesta total combina las acciones de estos tres componentes.

---

## 15. Sistema masa-resorte-amortiguador

El sistema clásico consiste en:

- una masa rígida $m$;
- un resorte sin masa de rigidez $k$;
- un amortiguador sin masa de coeficiente $c$;
- una superficie sin fricción;
- movimiento en una sola dirección.

Su ecuación es:

$$
m\ddot{u}+c\dot{u}+ku=p(t)
$$

---

## 16. Ejemplo 1.4: peso suspendido de un resorte y una viga en voladizo

El ejemplo deriva la ecuación de movimiento para un peso $w$ suspendido de un resorte ubicado en el extremo libre de una viga en voladizo de acero.

La fuerza de restauración se expresa como:

$$
f_S=k_e\bar{u}
$$

Donde $k_e$ es la rigidez efectiva del sistema combinado viga-resorte.

Al medir el desplazamiento total desde la configuración no deformada, la ecuación inicial incluye el peso:

$$
m\ddot{\bar{u}}+k_e\bar{u}=w+p(t)
$$

Luego se separa el desplazamiento total como:

$$
\bar{u}=\delta_{st}+u
$$

Donde:

- $\delta_{st}$ es el desplazamiento estático producido por el peso $w$;
- $u$ es el desplazamiento dinámico medido desde la posición de equilibrio estático.

Como:

$$
k_e\delta_{st}=w
$$

la ecuación se reduce a:

$$
m\ddot{u}+k_eu=p(t)
$$

### Idea clave del ejemplo

Para sistemas lineales, se puede formular el problema dinámico usando la posición de equilibrio estático como referencia. Así, las fuerzas gravitacionales se eliminan de la ecuación dinámica si no actúan como fuerzas restauradoras o desestabilizadoras.

---

## 17. Rigidez efectiva de elementos en serie

En el ejemplo 1.4, el resorte y la flexibilidad de la viga actúan en serie. La rigidez efectiva puede obtenerse a partir de flexibilidades:

$$
\frac{1}{k_e}=\frac{1}{k_{resorte}}+\frac{1}{k_{viga}}
$$

Para una viga en voladizo con carga en el extremo:

$$
k_{viga}=\frac{3EI}{L^3}
$$

Por tanto:

$$
k_e=\left(\frac{1}{k_{resorte}}+\frac{L^3}{3EI}\right)^{-1}
$$

---

## 18. Ejemplo 1.5: péndulo simple

El documento deriva la ecuación de movimiento libre de un péndulo simple compuesto por una masa puntual suspendida de una cuerda ligera de longitud $L$.

La coordenada generalizada es el ángulo $\theta$ medido desde la vertical.

La ecuación no lineal es:

$$
mL^2\ddot{\theta}+mgL\sin\theta=0
$$

Dividiendo entre $mL^2$:

$$
\ddot{\theta}+\frac{g}{L}\sin\theta=0
$$

Para oscilaciones pequeñas:

$$
\sin\theta\approx\theta
$$

Entonces:

$$
\ddot{\theta}+\frac{g}{L}\theta=0
$$

---

## 19. Ejemplo 1.6: barra con resorte rotacional

El sistema consiste en un peso $w$ unido a una barra sin masa de longitud $L$, con un resorte rotacional de rigidez $k$ en el apoyo.

La coordenada generalizada es el ángulo $\theta$ medido desde la vertical.

La ecuación de momento alrededor del apoyo lleva a:

$$
\frac{w}{g}L^2\ddot{\theta}+k\theta=wL\sin\theta
$$

Para pequeñas rotaciones:

$$
\sin\theta\approx\theta
$$

Entonces:

$$
\frac{w}{g}L^2\ddot{\theta}+(k-wL)\theta=0
$$

### Interpretación

- Si $k>wL$, el sistema tiene rigidez efectiva positiva y puede oscilar.
- Si $k=wL$, el sistema queda en condición crítica de estabilidad.
- Si $k<wL$, el sistema es inestable.

---

## 20. Ecuación de movimiento por excitación sísmica

En problemas sísmicos, la base de la estructura se mueve. El desplazamiento absoluto de la masa se expresa como:

$$
u^t(t)=u(t)+u_g(t)
$$

Donde:

- $u^t(t)$ es el desplazamiento absoluto;
- $u(t)$ es el desplazamiento relativo de la masa respecto a la base;
- $u_g(t)$ es el desplazamiento del terreno.

La aceleración absoluta es:

$$
\ddot{u}^t(t)=\ddot{u}(t)+\ddot{u}_g(t)
$$

Para un sistema elástico lineal:

$$
m\ddot{u}+c\dot{u}+ku=-m\ddot{u}_g(t)
$$

---

## 21. Fuerza sísmica efectiva

El movimiento basal puede sustituirse por una fuerza sísmica efectiva:

$$
p_{eff}(t)=-m\ddot{u}_g(t)
$$

Con esto, la ecuación sísmica queda en la misma forma que la ecuación por fuerza externa:

$$
m\ddot{u}+c\dot{u}+ku=p_{eff}(t)
$$

### Interpretación del signo negativo

La fuerza efectiva actúa en sentido opuesto a la aceleración del terreno.

---

## 22. Componente rotacional de excitación sísmica

Si la base experimenta una rotación $\theta_g(t)$, el desplazamiento absoluto puede escribirse como:

$$
u^t(t)=u(t)+h\theta_g(t)
$$

Donde $h$ es la altura de la masa respecto al punto de rotación.

La ecuación del movimiento queda:

$$
m\ddot{u}+c\dot{u}+ku=-mh\ddot{\theta}_g(t)
$$

La fuerza efectiva equivalente es:

$$
p_{eff}(t)=-mh\ddot{\theta}_g(t)
$$

---

## 23. Ejemplo 1.7: losa rígida con rotación de fundación

El ejemplo plantea una losa rígida uniforme apoyada sobre cuatro columnas y sometida a una rotación de la fundación alrededor de un eje vertical.

La respuesta se expresa mediante una coordenada rotacional relativa. En forma general:

$$
I_\theta\ddot{u}_\theta+f_S=-I_\theta\ddot{\theta}_g(t)
$$

Si la respuesta es lineal:

$$
f_S=k_\theta u_\theta
$$

Entonces:

$$
I_\theta\ddot{u}_\theta+k_\theta u_\theta=-I_\theta\ddot{\theta}_g(t)
$$

La rigidez torsional puede calcularse sumando el aporte de las columnas según su rigidez lateral y su distancia al centro de masa:

$$
k_\theta=\sum_i\left(k_{x,i}y_i^2+k_{y,i}x_i^2\right)
$$

Para columnas con extremos restringidos, una rigidez lateral típica es:

$$
k=\frac{12EI}{h^3}
$$

---

## 24. Planteamiento general del problema dinámico

Dados:

- la masa $m$;
- la rigidez $k$ o la relación $f_S(u)$;
- la fuerza externa $p(t)$ o fuerza sísmica efectiva $p_{eff}(t)$;
- las condiciones iniciales;

el problema fundamental de la dinámica estructural consiste en determinar la respuesta del sistema.

La respuesta puede incluir:

- desplazamiento;
- velocidad;
- aceleración;
- fuerzas internas;
- esfuerzos internos.

---

## 25. Respuesta relativa y absoluta

Para excitación sísmica se pueden necesitar respuestas absolutas y relativas.

La respuesta más importante para diseño estructural suele ser el desplazamiento relativo:

$$
u(t)
$$

porque este desplazamiento se relaciona directamente con la deformación de la estructura y con las fuerzas internas.

---

## 26. Fuerzas internas en los elementos

Una vez conocido $u(t)$, se pueden obtener fuerzas internas mediante análisis estático.

Hay dos formas equivalentes de verlo:

1. Usar el desplazamiento $u(t)$ y las rotaciones asociadas para calcular fuerzas internas.
2. Usar una fuerza estática equivalente $f_S(t)$ que produce el mismo desplazamiento.

Para un sistema lineal:

$$
f_S(t)=ku(t)
$$

---

## 27. Combinación de respuesta estática y dinámica

### 27.1 Sistemas elásticos lineales

En sistemas lineales se pueden calcular por separado:

- respuesta estática;
- respuesta dinámica.

Luego se suman para obtener la respuesta total.

### 27.2 Sistemas inelásticos

En sistemas inelásticos no se pueden separar las respuestas. El análisis dinámico debe incluir las fuerzas y deformaciones existentes antes del inicio de la excitación dinámica.

---

## 28. Métodos de solución de la ecuación diferencial

La ecuación general es:

$$
m\ddot{u}+c\dot{u}+ku=p(t)
$$

con condiciones iniciales.

Los métodos mencionados son:

1. solución clásica;
2. integral de Duhamel;
3. método en el dominio de frecuencia;
4. métodos numéricos.

---

## 29. Solución clásica

La solución clásica se expresa como suma de:

$$
u(t)=u_c(t)+u_p(t)
$$

Donde:

- $u_c(t)$ es la solución complementaria;
- $u_p(t)$ es la solución particular.

---

## 30. Ejemplo 1.8: fuerza escalón en sistema no amortiguado

Se considera:

$$
p(t)=p_0,\qquad t\geq0
$$

con $c=0$. La ecuación es:

$$
m\ddot{u}+ku=p_0
$$

Si el sistema parte del reposo, la respuesta es:

$$
u(t)=\frac{p_0}{k}\left(1-\cos\omega_n t\right)
$$

con:

$$
\omega_n=\sqrt{\frac{k}{m}}
$$

---

## 31. Integral de Duhamel

La integral de Duhamel representa una fuerza aplicada como una sucesión de impulsos muy pequeños. La respuesta total es la suma de las respuestas individuales desde $0$ hasta $t$.

Para un sistema no amortiguado en reposo inicial:

$$
u(t)=\frac{1}{m\omega_n}\int_0^t p(\tau)\sin\left[\omega_n(t-\tau)\right]d\tau
$$

Para una fuerza escalón $p(t)=p_0$, se obtiene el mismo resultado que con la solución clásica:

$$
u(t)=\frac{p_0}{k}\left(1-\cos\omega_n t\right)
$$

---

## 32. Casos donde la interacción con el entorno es importante

### 32.1 Interacción estructura-suelo

El documento menciona estructuras de contención de concreto reforzado en la planta nuclear de San Onofre, California. El período natural calculado cambia de 0.15 s, suponiendo base rígida, a 0.50 s, considerando la flexibilidad del suelo.

**Idea clave:** la flexibilidad del suelo puede cambiar de forma importante el período natural de una estructura.

### 32.2 Interacción represa-agua

También se menciona la represa Morrow Point, una represa de arco de 142 m en Colorado. Las pruebas de vibración forzada indicaron un período de 0.268 s con el reservorio parcialmente lleno y 0.303 s con el reservorio lleno.

**Idea clave:** el agua almacenada modifica la masa efectiva y la respuesta dinámica de la represa.

---

## 33. Métodos numéricos

Los métodos clásicos funcionan bien para sistemas lineales. Sin embargo, para estructuras que entran en comportamiento inelástico durante terremotos intensos, se requieren métodos numéricos.

El documento menciona el método de Newmark como referencia importante:

> Newmark, N. M., “A Method of Computation for Structural Dynamics,” Journal of the Engineering Mechanics Division, ASCE, 85, 1959, pp. 67-94.

---

## 34. Resumen de ecuaciones clave

| Tema | Ecuación |
|---|---|
| Vibración libre no amortiguada | $m\ddot{u}+ku=0$ |
| Fuerza de restauración lineal | $f_S=ku$ |
| Fuerza de amortiguamiento viscoso | $f_D=c\dot{u}$ |
| Fuerza externa | $m\ddot{u}+c\dot{u}+ku=p(t)$ |
| Sistema inelástico | $m\ddot{u}+c\dot{u}+f_S(u)=p(t)$ |
| Desplazamiento absoluto sísmico | $u^t(t)=u(t)+u_g(t)$ |
| Excitación sísmica | $m\ddot{u}+c\dot{u}+ku=-m\ddot{u}_g(t)$ |
| Fuerza sísmica efectiva | $p_{eff}(t)=-m\ddot{u}_g(t)$ |
| Rotación de base | $p_{eff}(t)=-mh\ddot{\theta}_g(t)$ |
| Solución clásica | $u(t)=u_c(t)+u_p(t)$ |
| Duhamel no amortiguado | $u(t)=\dfrac{1}{m\omega_n}\int_0^t p(\tau)\sin[\omega_n(t-\tau)]d\tau$ |
| Fuerza escalón no amortiguada | $u(t)=\dfrac{p_0}{k}(1-\cos\omega_n t)$ |

---

## 35. Ideas clave para usar como contexto en Claude

- Una estructura sencilla puede modelarse como un sistema UGL si su respuesta dominante se describe con una sola coordenada.
- La masa, rigidez y amortiguamiento son los tres componentes básicos de la dinámica estructural.
- La posición de equilibrio estático puede usarse como referencia para eliminar cargas gravitacionales de la ecuación dinámica, siempre que esas cargas no sean restauradoras ni desestabilizadoras.
- La excitación sísmica se transforma en una fuerza efectiva proporcional a la masa y a la aceleración del terreno.
- En sistemas lineales, la respuesta estática y la dinámica pueden separarse y sumarse.
- En sistemas inelásticos, la historia de carga y deformación importa; por eso se requieren métodos numéricos.

---

## 36. Referencia

[1] Universidad de Costa Rica, “Vibraciones Mecánicas: Lección 1, Introducción,” material de clase IC-0502, I Semestre 2026, 8 jun. 2026.
