# Vibraciones Mecánicas - Lección 2: Oscilación libre en sistemas UGL

**Archivo fuente:** `CHOPRA-Tema 2 Oscilacion libre en sistemas UGL (1).pdf`  
**Tipo de documento:** diapositivas de clase.  
**Curso indicado en el documento:** IC-0502, Vibraciones Mecánicas.  
**Fecha indicada en portada:** 8 de junio de 2026.  
**Uso recomendado:** contexto para explicar oscilación libre, frecuencia natural, período natural, amortiguamiento viscoso, decremento logarítmico y pruebas experimentales de vibración libre.

## Cita IEEE sugerida

[1] Universidad de Costa Rica, “Vibraciones Mecánicas: Lección 2, Oscilación libre en sistemas UGL,” material de clase IC-0502, I Semestre 2026, 8 jun. 2026.

> Nota: el PDF no muestra autor personal en la portada. Por eso se usa la institución como autor corporativo.

---

## 1. Objetivo general de la lección

La lección explica la **oscilación libre** de sistemas de un grado de libertad (UGL), tanto sin amortiguamiento como con amortiguamiento viscoso. También muestra cómo obtener propiedades dinámicas a partir de registros experimentales.

Los conceptos principales son:

- oscilación libre;
- frecuencia natural;
- período natural;
- razón de amortiguamiento;
- amortiguamiento crítico;
- decremento logarítmico;
- estimación experimental de propiedades dinámicas.

---

## 2. Oscilación libre

Un sistema está en **oscilación libre** cuando se separa de su posición de equilibrio estático y luego se deja oscilar sin excitación dinámica externa.

La oscilación libre permite identificar las propiedades dinámicas principales del sistema:

1. frecuencia natural de oscilación;
2. razón de amortiguamiento.

---

## 3. Oscilación libre no amortiguada

Para un sistema UGL sin amortiguamiento y sin fuerza externa:

$$
m\ddot{u}+ku=0
$$

Dividiendo entre $m$:

$$
\ddot{u}+\omega_n^2u=0
$$

Donde:

$$
\omega_n=\sqrt{\frac{k}{m}}
$$

es la frecuencia natural circular o frecuencia natural angular.

---

## 4. Solución de la vibración libre no amortiguada

Con condiciones iniciales:

$$
u(0)=u_0
$$

$$
\dot{u}(0)=\dot{u}_0
$$

la respuesta es:

$$
u(t)=u(0)\cos(\omega_n t)+\frac{\dot{u}(0)}{\omega_n}\sin(\omega_n t)
$$

También puede escribirse como:

$$
u(t)=\rho\cos(\omega_n t-\phi)
$$

Donde la amplitud es:

$$
\rho=\sqrt{[u(0)]^2+\left[\frac{\dot{u}(0)}{\omega_n}\right]^2}
$$

---

## 5. Período natural y frecuencia natural

El **período natural** $T_n$ es el tiempo requerido para completar un ciclo de oscilación.

$$
T_n=\frac{2\pi}{\omega_n}
$$

La frecuencia cíclica natural es:

$$
f_n=\frac{1}{T_n}
$$

También:

$$
f_n=\frac{\omega_n}{2\pi}
$$

---

## 6. Ejemplos de períodos naturales en estructuras reales

El documento presenta varios ejemplos de estructuras reales y sus períodos naturales medidos mediante pruebas o registros.

### 6.1 Edificio Alcoa, San Francisco

Edificio de acero de 27 pisos.

| Tipo de oscilación | Período natural |
|---|---:|
| Norte-Sur, longitudinal | 1.67 s |
| Este-Oeste, transversal | 2.21 s |
| Torsional alrededor del eje vertical | 1.12 s |

Los datos fueron obtenidos mediante pruebas de vibración forzada.

### 6.2 Edificio Transamerica, San Francisco

Edificio piramidal de acero de 60 pisos.

| Tipo de oscilación | Período natural |
|---|---:|
| Ambas direcciones principales | 2.94 s |
| Torsión | 2.24 s |

Los datos fueron obtenidos por EERC, UC Berkeley, en 1972, mediante pruebas de vibración forzada.

### 6.3 Medical Center Building, Richmond, California

Edificio de acero de tres pisos.

| Tipo de oscilación | Período natural |
|---|---:|
| Longitudinal | 0.63 s |
| Transversal | 0.74 s |
| Torsional alrededor del eje vertical | 0.46 s |

Los datos fueron obtenidos a partir de acelerogramas del terremoto de Loma Prieta de 1989.

### 6.4 Pine Flat Dam, California

Represa de gravedad de 120 m de altura.

| Nivel del reservorio | Período natural |
|---|---:|
| 94 m | 0.288 s |
| 105 m | 0.306 s |

El aumento del nivel del reservorio aumenta el período natural, porque cambia la interacción dinámica con el agua.

### 6.5 Golden Gate Bridge, San Francisco

Puente colgante con luz principal de 1280 m.

| Tipo de oscilación | Período natural |
|---|---:|
| Transversal | 18.2 s |
| Vertical | 10.9 s |
| Longitudinal | 3.81 s |
| Torsional | 4.43 s |

Los datos se obtuvieron a partir de registros de movimiento debidos a condiciones ambientales, como viento y tránsito.

### 6.6 Chimenea de concreto reforzado, Aramon, Francia

Chimenea de 250 m de altura.

| Tipo de estructura | Período natural |
|---|---:|
| Chimenea de concreto reforzado | 3.57 s |

El período fue medido a partir de registros de oscilación inducidos por viento.

---

## 7. Frecuencia natural de un pórtico de un piso

Para un pórtico idealizado de un piso:

$$
\omega_n=\sqrt{\frac{k}{m}}
$$

La rigidez lateral $k$ depende de las propiedades de vigas y columnas. El documento presenta una expresión donde la rigidez varía con la relación de rigidez viga-columna $\rho$:

$$
k=\frac{24EI_c}{h^3}\left(\frac{12\rho+1}{12\rho+4}\right)
$$

Donde:

- $E$ es el módulo de elasticidad;
- $I_c$ es el momento de inercia de las columnas;
- $h$ es la altura del pórtico;
- $\rho$ representa la relación de rigidez entre viga y columna.

### 7.1 Casos extremos

Para rigidez de viga muy grande:

$$
(\omega_n)_{\rho=\infty}=\sqrt{\frac{24EI_c}{mh^3}}
$$

Para rigidez de viga nula:

$$
(\omega_n)_{\rho=0}=\sqrt{\frac{6EI_c}{mh^3}}
$$

**Idea clave:** a mayor rigidez lateral, mayor frecuencia natural y menor período natural.

---

## 8. Oscilación libre con amortiguamiento viscoso

La ecuación del movimiento para un sistema con amortiguamiento viscoso es:

$$
m\ddot{u}+c\dot{u}+ku=0
$$

Dividiendo entre $m$:

$$
\ddot{u}+\frac{c}{m}\dot{u}+\frac{k}{m}u=0
$$

Se escribe de forma estándar como:

$$
\ddot{u}+2\zeta\omega_n\dot{u}+\omega_n^2u=0
$$

Donde:

$$
\omega_n=\sqrt{\frac{k}{m}}
$$

$$
\zeta=\frac{c}{c_{cr}}
$$

---

## 9. Amortiguamiento crítico

El coeficiente de amortiguamiento crítico es:

$$
c_{cr}=2m\omega_n
$$

También puede expresarse como:

$$
c_{cr}=2\sqrt{km}
$$

La razón de amortiguamiento es:

$$
\zeta=\frac{c}{2m\omega_n}=\frac{c}{2\sqrt{km}}
$$

---

## 10. Tipos de movimiento según la razón de amortiguamiento

| Caso | Condición | Comportamiento |
|---|---|---|
| Subamortiguado | $0<\zeta<1$ | Oscila con amplitud decreciente |
| Críticamente amortiguado | $\zeta=1$ | Vuelve al equilibrio sin oscilar, en el menor tiempo posible |
| Sobreamortiguado | $\zeta>1$ | Vuelve al equilibrio sin oscilar, más lentamente |

En estructuras reales, el caso más común es el subamortiguado.

---

## 11. Respuesta subamortiguada

Para $0<\zeta<1$, la frecuencia amortiguada es:

$$
\omega_D=\omega_n\sqrt{1-\zeta^2}
$$

La respuesta con condiciones iniciales $u(0)$ y $\dot{u}(0)$ es:

$$
u(t)=e^{-\zeta\omega_n t}\left[u(0)\cos(\omega_D t)+\frac{\dot{u}(0)+\zeta\omega_n u(0)}{\omega_D}\sin(\omega_D t)\right]
$$

La amplitud decrece por el factor exponencial:

$$
e^{-\zeta\omega_n t}
$$

---

## 12. Período amortiguado

El período amortiguado es:

$$
T_D=\frac{2\pi}{\omega_D}
$$

Como:

$$
\omega_D=\omega_n\sqrt{1-\zeta^2}
$$

entonces:

$$
T_D=\frac{T_n}{\sqrt{1-\zeta^2}}
$$

Para razones de amortiguamiento menores a 20%, el efecto del amortiguamiento sobre la frecuencia natural o el período natural suele ser pequeño.

---

## 13. Efecto principal del amortiguamiento

El efecto más importante del amortiguamiento no es cambiar mucho la frecuencia, sino hacer que la amplitud disminuya con el tiempo.

A mayor $\zeta$:

- la oscilación decae más rápido;
- se requieren menos ciclos para que la amplitud se reduzca;
- la respuesta se acerca más rápido al equilibrio.

---

## 14. Decremento logarítmico

El decremento logarítmico mide la caída de amplitud entre dos picos sucesivos.

Para dos máximos consecutivos:

$$
\delta=\ln\left(\frac{u_i}{u_{i+1}}\right)
$$

Para un sistema subamortiguado:

$$
\delta=\frac{2\pi\zeta}{\sqrt{1-\zeta^2}}
$$

Si $\zeta$ es pequeña:

$$
\delta\approx2\pi\zeta
$$

---

## 15. Decremento logarítmico usando varios ciclos

Si se usan dos amplitudes separadas por $j$ ciclos:

$$
\delta=\frac{1}{j}\ln\left(\frac{u_i}{u_{i+j}}\right)
$$

Para amortiguamiento leve:

$$
\zeta\approx\frac{1}{2\pi j}\ln\left(\frac{u_i}{u_{i+j}}\right)
$$

Esta forma es útil porque reduce el error experimental al no depender solo de dos picos consecutivos.

---

## 16. Uso de aceleraciones en vez de desplazamientos

En pruebas experimentales puede usarse la razón entre máximos de aceleración:

$$
\zeta\approx\frac{1}{2\pi j}\ln\left(\frac{\ddot{u}_i}{\ddot{u}_{i+j}}\right)
$$

Esto es válido para amortiguamiento leve.

---

## 17. Número de ciclos para reducir la amplitud al 50%

El documento muestra una relación aproximada entre la razón de amortiguamiento y el número de ciclos necesarios para reducir la amplitud a la mitad:

$$
j_{50\%}\approx\frac{0.11}{\zeta}
$$

Esta aproximación aplica para amortiguamiento leve.

---

## 18. Pruebas de oscilación libre

En una prueba de oscilación libre:

1. se perturba la estructura desde su equilibrio;
2. se deja vibrar libremente;
3. se registra la respuesta en el tiempo;
4. se miden picos sucesivos y tiempos entre ciclos;
5. se calculan período natural y razón de amortiguamiento.

El período amortiguado $T_D$ se obtiene midiendo el tiempo necesario para completar un ciclo.

Si el amortiguamiento es leve:

$$
T_D\approx T_n
$$

---

## 19. Comparación entre modelo idealizado y prueba experimental

El período medido en una prueba de vibración libre puede compararse con el período calculado a partir de la masa y rigidez de un modelo idealizado.

Esta comparación indica:

- qué tan bien se estimaron la masa y la rigidez;
- qué tan representativo es el modelo idealizado;
- si se deben ajustar las propiedades dinámicas del modelo.

---

## 20. Ejemplo 2.5: pórtico de plexiglás

Se pide encontrar el período natural y la razón de amortiguamiento del marco de plexiglás a partir de un registro de aceleraciones de oscilación libre.

Datos extraídos del registro:

| Pico | Tiempo $t_i$ | Máximo $\ddot{u}_i$ |
|---:|---:|---:|
| 1 | 1.110 s | 0.915 g |
| 11 | 3.844 s | 0.076 g |

Como los picos están separados por 10 ciclos:

$$
j=10
$$

### 20.1 Período amortiguado

$$
T_D=\frac{3.844-1.110}{10}
$$

$$
T_D=0.2734\;\text{s}
$$

### 20.2 Decremento logarítmico

$$
\delta=\frac{1}{10}\ln\left(\frac{0.915}{0.076}\right)
$$

$$
\delta\approx0.2488
$$

### 20.3 Razón de amortiguamiento aproximada

Para amortiguamiento leve:

$$
\zeta\approx\frac{\delta}{2\pi}
$$

$$
\zeta\approx0.0396
$$

$$
\zeta\approx3.96\%
$$

---

## 21. Ejemplo 2.6: tanque elevado vacío

Se realiza una prueba de oscilación libre en un tanque elevado vacío.

Datos:

- fuerza lateral aplicada: $16.4$ kips;
- desplazamiento inicial: $2$ in;
- al final de 4 ciclos: tiempo $2$ s;
- amplitud luego de 4 ciclos: $1$ in.

### 21.1 Razón de amortiguamiento

Con:

$$
u_i=2\;\text{in},\qquad u_{i+4}=1\;\text{in},\qquad j=4
$$

$$
\zeta\approx\frac{1}{2\pi(4)}\ln\left(\frac{2}{1}\right)
$$

$$
\zeta\approx0.0276
$$

$$
\zeta\approx2.76\%
$$

### 21.2 Período natural no amortiguado

El período amortiguado es:

$$
T_D=\frac{2}{4}=0.5\;\text{s}
$$

Como el amortiguamiento es leve:

$$
T_n\approx T_D\sqrt{1-\zeta^2}
$$

$$
T_n\approx0.4998\;\text{s}
$$

### 21.3 Rigidez

La rigidez se obtiene de la prueba estática inicial:

$$
k=\frac{F}{u}=\frac{16.4}{2}
$$

$$
k=8.2\;\text{kip/in}
$$

### 21.4 Peso del tanque vacío

Usando:

$$
\omega_n=\frac{2\pi}{T_n}
$$

$$
\omega_n\approx12.57\;\text{rad/s}
$$

Además:

$$
\omega_n^2=\frac{k}{m}=\frac{kg}{w}
$$

Despejando:

$$
w=\frac{kg}{\omega_n^2}
$$

Con $g=386.4\;\text{in/s}^2$:

$$
w\approx20.05\;\text{kips}
$$

### 21.5 Coeficiente de amortiguamiento

$$
c=2\zeta m\omega_n
$$

Como $m=w/g$:

$$
c=2\zeta\frac{w}{g}\omega_n
$$

$$
c\approx0.036\;\text{kip·s/in}
$$

### 21.6 Ciclos para disminuir la amplitud a 0.2 in

Si la amplitud pasa de 2 in a 0.2 in:

$$
j=\frac{1}{2\pi\zeta}\ln\left(\frac{2}{0.2}\right)
$$

$$
j\approx13.3\;\text{ciclos}
$$

---

## 22. Ejemplo 2.7: tanque lleno

El tanque del ejemplo anterior se llena con agua. El peso del agua es:

$$
w_{agua}=80\;\text{kips}
$$

El peso total es:

$$
w_{total}=w_{tanque}+w_{agua}
$$

$$
w_{total}\approx20.05+80=100.05\;\text{kips}
$$

La rigidez $k$ se mantiene igual:

$$
k=8.2\;\text{kip/in}
$$

### 22.1 Nuevo período natural

$$
T_n=2\pi\sqrt{\frac{m}{k}}=2\pi\sqrt{\frac{w_{total}}{gk}}
$$

$$
T_n\approx1.12\;\text{s}
$$

### 22.2 Nueva razón de amortiguamiento

Si el coeficiente $c$ se mantiene aproximadamente igual, pero la masa aumenta, el amortiguamiento crítico aumenta. Por eso la razón de amortiguamiento disminuye.

$$
\zeta=\frac{c}{2m\omega_n}
$$

Resultado aproximado:

$$
\zeta\approx0.0123
$$

$$
\zeta\approx1.23\%
$$

**Idea clave:** al aumentar la masa, el período natural aumenta y la razón de amortiguamiento disminuye si $c$ permanece constante.

---

## 23. Composición energética de la oscilación libre

En un sistema no amortiguado, la energía se intercambia entre:

- energía cinética;
- energía potencial elástica.

La energía total permanece constante en el tiempo.

Para sistemas con amortiguamiento viscoso, la energía total decrece porque una parte se disipa.

---

## 24. Derivación de la solución no amortiguada

Para:

$$
m\ddot{u}+ku=0
$$

se propone:

$$
u(t)=Ae^{st}
$$

Sustituyendo:

$$
(ms^2+k)Ae^{st}=0
$$

La ecuación característica es:

$$
ms^2+k=0
$$

Por tanto:

$$
s=\pm i\omega_n
$$

La solución se expresa en funciones trigonométricas:

$$
u(t)=A\cos(\omega_n t)+B\sin(\omega_n t)
$$

Usando condiciones iniciales:

$$
A=u(0)
$$

$$
B=\frac{\dot{u}(0)}{\omega_n}
$$

Entonces:

$$
u(t)=u(0)\cos(\omega_n t)+\frac{\dot{u}(0)}{\omega_n}\sin(\omega_n t)
$$

---

## 25. Derivación de la solución amortiguada

Para:

$$
\ddot{u}+2\zeta\omega_n\dot{u}+\omega_n^2u=0
$$

se propone:

$$
u(t)=Ae^{st}
$$

La ecuación característica es:

$$
s^2+2\zeta\omega_ns+\omega_n^2=0
$$

Las raíces son:

$$
s=-\zeta\omega_n\pm\omega_n\sqrt{\zeta^2-1}
$$

Para $0<\zeta<1$:

$$
s=-\zeta\omega_n\pm i\omega_D
$$

con:

$$
\omega_D=\omega_n\sqrt{1-\zeta^2}
$$

La respuesta subamortiguada es:

$$
u(t)=e^{-\zeta\omega_n t}\left[A\cos(\omega_D t)+B\sin(\omega_D t)\right]
$$

con:

$$
A=u(0)
$$

$$
B=\frac{\dot{u}(0)+\zeta\omega_nu(0)}{\omega_D}
$$

---

## 26. Resumen de ecuaciones clave

| Tema | Ecuación |
|---|---|
| Oscilación libre no amortiguada | $m\ddot{u}+ku=0$ |
| Frecuencia natural angular | $\omega_n=\sqrt{k/m}$ |
| Período natural | $T_n=2\pi/\omega_n$ |
| Frecuencia cíclica | $f_n=1/T_n=\omega_n/(2\pi)$ |
| Respuesta no amortiguada | $u(t)=u(0)\cos\omega_nt+\dfrac{\dot{u}(0)}{\omega_n}\sin\omega_nt$ |
| Amplitud no amortiguada | $\rho=\sqrt{u(0)^2+[\dot{u}(0)/\omega_n]^2}$ |
| Ecuación amortiguada | $m\ddot{u}+c\dot{u}+ku=0$ |
| Forma estándar | $\ddot{u}+2\zeta\omega_n\dot{u}+\omega_n^2u=0$ |
| Amortiguamiento crítico | $c_{cr}=2m\omega_n=2\sqrt{km}$ |
| Razón de amortiguamiento | $\zeta=c/c_{cr}$ |
| Frecuencia amortiguada | $\omega_D=\omega_n\sqrt{1-\zeta^2}$ |
| Período amortiguado | $T_D=T_n/\sqrt{1-\zeta^2}$ |
| Decremento logarítmico | $\delta=\ln(u_i/u_{i+1})$ |
| Decremento y amortiguamiento | $\delta=2\pi\zeta/\sqrt{1-\zeta^2}$ |
| Aproximación para $\zeta$ pequeña | $\delta\approx2\pi\zeta$ |
| Varios ciclos | $\zeta\approx\dfrac{1}{2\pi j}\ln\left(\dfrac{u_i}{u_{i+j}}\right)$ |
| Ciclos para 50% | $j_{50\%}\approx0.11/\zeta$ |

---

## 27. Ideas clave para usar como contexto en Claude

- La oscilación libre se usa para identificar propiedades dinámicas de un sistema.
- La frecuencia natural depende de la relación entre rigidez y masa: mayor rigidez aumenta $\omega_n$; mayor masa reduce $\omega_n$.
- El amortiguamiento leve cambia poco la frecuencia, pero reduce la amplitud con el tiempo.
- El decremento logarítmico permite estimar la razón de amortiguamiento a partir de registros experimentales.
- Para datos ruidosos conviene usar picos separados por varios ciclos.
- En estructuras reales, el período natural depende del tipo de oscilación: longitudinal, transversal, vertical o torsional.
- El aumento de masa, como llenar un tanque con agua, aumenta el período natural.

---

## 28. Referencia

[1] Universidad de Costa Rica, “Vibraciones Mecánicas: Lección 2, Oscilación libre en sistemas UGL,” material de clase IC-0502, I Semestre 2026, 8 jun. 2026.
