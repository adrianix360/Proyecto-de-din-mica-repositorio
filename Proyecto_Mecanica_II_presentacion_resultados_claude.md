# Proyecto - Análisis y presentación de resultados

**Curso:** IC-0502 Mecánica II  
**Ciclo:** I Ciclo Lectivo de 2022  
**Instructor:** Guillermo Santana, DPhil.  
**Grupo:** 02  
**Tema:** Proyecto con mesa vibratoria - análisis y presentación de resultados

> Versión Markdown optimizada para usar en Claude. Se eliminaron saltos de página y elementos repetitivos, se conservaron instrucciones, fórmulas, tablas y códigos. Las figuras se describen como referencias textuales para ahorrar tokens.

---

## Apartado previo al análisis de resultados experimentales

Antes del análisis de los resultados experimentales, conviene incluir un apartado que presente y comente brevemente:

1. **Datos de los edificios:** dimensiones, tipo de material, secciones transversales, conexiones, empotramiento, etc.
2. **Método y fases constructivas:** proceso general de construcción del edificio y dificultades enfrentadas durante su construcción.

---

# 1. Caracterización dinámica del edificio

**Objetivo:** hallar las propiedades dinámicas intrínsecas de los edificios construidos mediante pruebas de vibración libre y vibración forzada.

---

## 1.1 Prueba de vibración libre

Realizar para cada edificio:

### a) Períodos de oscilación desde la forma de onda

Hallar los períodos de oscilación del edificio directamente de la forma de onda obtenida en vibración libre. En lo posible, obtener todos los períodos observables en las señales recolectadas de desplazamiento y aceleración.

**Nota importante:** el período de mayor duración de la estructura se llama **período fundamental**. Este es el período que suele leerse con mayor facilidad en el gráfico de desplazamientos de vibración libre. En los primeros segundos pueden observarse señales similares a ruido, especialmente por golpes súbitos; esas señales corresponden a vibraciones de modos superiores, con frecuencias más altas.

**Figura de referencia:** historia de vibración libre con desplazamiento en función del tiempo.

---

### b) Amortiguamiento por decremento logarítmico

Hallar el amortiguamiento de la estructura, para el modo fundamental, usando el método de decremento logarítmico y la historia de desplazamiento en el tiempo. Usar la medición del piso superior.

La fórmula base es:

\[
\delta = \ln\left(\frac{u_i}{u_{i+j}}\right)=j\,2\pi\xi
\]

Por tanto:

\[
\xi=\frac{\delta}{2\pi j}
\]

Donde:

- \(\delta\): decremento logarítmico.
- \(u_i\): amplitud de referencia.
- \(u_{i+j}\): amplitud después de \(j\) ciclos.
- \(j\): número de ciclos entre picos comparados.
- \(\xi\): razón de amortiguamiento.

---

### c) Análisis estadístico del amortiguamiento

Hacer un análisis estadístico del amortiguamiento identificado:

- Promedio.
- Desviación estándar.
- Comentario técnico sobre la dispersión y confiabilidad de los resultados.

---

## Ejemplo: cálculo de amortiguamiento por decremento logarítmico

Se obtuvo una historia de vibración libre para una estructura. Se solicita calcular la razón de amortiguamiento \(\xi\) mediante decremento logarítmico.

### Caso 1: picos máximos y mínimos sucesivos con \(j=1\)

| Número (k) | \(u_{máx}\) (mm) | \(u_{mín}\) (mm) | \(\delta\) para \(u_{máx}\), \(j=1\) | \(\delta\) para \(u_{mín}\), \(j=1\) | \(\xi\) desde \(u_{máx}\) | \(\xi\) desde \(u_{mín}\) |
|---:|---:|---:|---:|---:|---:|---:|
| 1 | 5.308 | -4.005 |  |  |  |  |
| 2 | 3.570 | -3.316 | 0.397 | 0.189 | 0.063 | 0.030 |
| 3 | 2.798 | -2.533 | 0.244 | 0.269 | 0.039 | 0.043 |
| 4 | 2.292 | -2.075 | 0.199 | 0.199 | 0.032 | 0.032 |
| 5 | 1.858 | -1.689 | 0.210 | 0.206 | 0.033 | 0.033 |
| 6 | 1.520 | -1.375 | 0.201 | 0.206 | 0.032 | 0.033 |
| 7 | 1.254 | -1.158 | 0.192 | 0.172 | 0.031 | 0.027 |
| 8 | 1.037 | -0.941 | 0.190 | 0.208 | 0.030 | 0.033 |
| 9 | 0.869 | -0.772 | 0.177 | 0.198 | 0.028 | 0.032 |
| **Promedio** |  |  |  |  | **0.032** | **0.033** |
| **Desviación estándar** |  |  |  |  | **0.003** | **0.004** |

---

### Caso 2: picos máximos y mínimos con el pico 2 como referencia y \(j\) variable

| Número (k) | \(u_{máx}\) (mm) | \(u_{mín}\) (mm) | \(\delta\) para \(u_{máx}\), \(j\) variable | \(\delta\) para \(u_{mín}\), \(j\) variable | \(\xi\) desde \(u_{máx}\) | \(\xi\) desde \(u_{mín}\) |
|---:|---:|---:|---:|---:|---:|---:|
| 1 | 5.308 | -4.005 |  |  |  |  |
| 2 | 3.570 | -3.316 |  |  |  |  |
| 3 | 2.798 | -2.533 | 0.244 | 0.269 | 0.039 | 0.043 |
| 4 | 2.292 | -2.075 | 0.443 | 0.469 | 0.035 | 0.037 |
| 5 | 1.858 | -1.689 | 0.653 | 0.675 | 0.035 | 0.036 |
| 6 | 1.520 | -1.375 | 0.854 | 0.880 | 0.034 | 0.035 |
| 7 | 1.254 | -1.158 | 1.046 | 1.052 | 0.033 | 0.033 |
| 8 | 1.037 | -0.941 | 1.236 | 1.260 | 0.033 | 0.033 |
| 9 | 0.869 | -0.772 | 1.413 | 1.458 | 0.032 | 0.033 |
| **Promedio** |  |  |  |  | **0.034** | **0.036** |
| **Desviación estándar** |  |  |  |  | **0.002** | **0.003** |

---

### d) Transformada Rápida de Fourier, FFT

Realizar la Transformada Rápida de Fourier a:

1. La historia de desplazamiento en el tiempo.
2. La historia de aceleración en el tiempo.

Recomendación: no aplicar la transformada necesariamente a toda la historia en el tiempo, sino a historias selectas de vibración libre con por lo menos **2048 puntos**. Las frecuencias naturales se identifican tomando los picos dominantes del espectro.

**Figura de referencia:** espectro FFT con amplitud contra frecuencia; el pico dominante indica una frecuencia natural cíclica de vibración.

---

### e) Comparación antes y después de pruebas sísmicas

Si se dispone de historias de vibración libre después de las pruebas sísmicas, posiblemente con daños, obtener nuevamente las características dinámicas del edificio con los métodos anteriores y comentar las diferencias.

---

### f) Superposición de historias de vibración libre

Para cada edificio, seleccionar:

1. Una historia de desplazamiento en vibración libre.
2. Una historia de aceleración en vibración libre.

Luego:

- Superponerlas en el mismo gráfico.
- Usar un acercamiento suficiente para compararlas.
- Comentar los hallazgos y su relación con la teoría de vibraciones.

---

## Código MATLAB: Transformada Rápida de Fourier

```matlab
%% Transformada Rápida de Fourier (Fast Fourier Transform-FFT)
% La señal debe ser cargada a workspace con el comando load 'nombre_archivo.txt'
% y renombrado como X.
% El archivo .txt no debe tener encabezado.
% Escoja la columna que se desea analizar con FFT.
% Por ejemplo, si la 3era columna de X corresponde a la medición de laser:
% Y = X(:,3);
% Si la 5ta columna fuera de aceleración del edificio:
% Y = X(:,5);

dt = 0.01; % intervalo de tiempo entre los puntos de muestreo
sr = 1/dt; % tasa de muestreo
time = 0:dt:(length(Y)-1)*dt; % arreglo de tiempo para eje x

% Graficar la señal
figure
plot(time,Y,'-b'), xlabel('Tiempo (s)'), ylabel('Aceleracion (g)'), ...
    title(['Historia de aceleracion en el tiempo'])

NFFT = 2^(floor(log2(length(Y)))-1); % puntos a computar en FFT
Y_fft = fft(Y,NFFT)/NFFT; % algoritmo FFT predefinido en Matlab

freq = sr/2*linspace(0,1,NFFT/2+1); % arreglo de frecuencias para eje x

% Graficar el Espectro de Fourier
figure
semilogy(freq,abs(Y_fft(1:NFFT/2+1)),'-b'), ...
    xlabel('Frecuencia (Hz)'), ylabel('Amplitud'), ...
    title(['FFT de la historia de aceleracion'])
```

---

## Códigos MATLAB para graficar historias de vibración libre

```matlab
%% Comparación de desplazamiento entre edificio bajo y edificio alto
figure
plot(X(:,1),X(:,3),'-b')
hold on
plot(X(:,1),X(:,4),'-r')
hold off
legend('edificio bajo','edificio alto')
xlabel('tiempo (s)')
ylabel('desplazamiento (mm)')
title('historia de vibracion libre')

%% Desplazamiento del edificio alto
figure
plot(X(:,1),X(:,4),'-r')
legend('edificio alto')
xlabel('tiempo (s)')
ylabel('desplazamiento (mm)')
title('historia de vibracion libre del edificio alto')

%% Comparación de aceleración entre edificio bajo y edificio alto
figure
plot(X(:,1),X(:,6),'-b')
hold on
plot(X(:,1),X(:,7),'-r')
hold off
legend('edificio bajo','edificio alto')
xlabel('tiempo (s)')
ylabel('aceleracion (g)')
title('historia de vibracion libre')

%% Aceleración del edificio alto
figure
plot(X(:,1),X(:,7),'-r')
legend('edificio alto')
xlabel('tiempo (s)')
ylabel('aceleracion (g)')
title('historia de vibracion libre edificio alto (aceleracion)')
```

---

## 1.2 Prueba de vibración forzada

Realizar lo siguiente para cada edificio.

### a) Superponer desplazamiento y aceleración del piso superior

Graficar y superponer la historia de desplazamiento y aceleración del piso superior del mismo edificio en el mismo gráfico. Estudiar y comentar los hallazgos según la teoría estudiada en clase.

**Figura de referencia:** historia de vibración forzada y gráfico con dos ejes verticales, uno para desplazamiento y otro para aceleración.

---

### b) Superponer desplazamiento de la base y del piso superior

Graficar y superponer:

- Historia de desplazamiento de la base.
- Historia de desplazamiento del piso superior del edificio.

Mostrar gráficos de acercamiento para:

1. Frecuencias antes de resonancia.
2. Frecuencia de resonancia.
3. Frecuencias después de resonancia.

Estudiar y comentar los hallazgos.

**Figuras de referencia:** gráficos comparativos de desplazamiento de base y piso superior antes, durante y después de la resonancia.

---

### c) Verificación de frecuencia y ángulo de fase experimental

Con el mismo gráfico del punto b):

1. Verificar que la frecuencia en cada tramo de amplitud constante corresponde a la frecuencia de la mesa.
2. Calcular el tiempo de retraso de la respuesta de desplazamiento del edificio respecto al desplazamiento de la base.
3. Con ese tiempo de retraso, obtener el ángulo de fase experimental.
4. Mostrar en un gráfico la variación del ángulo de fase experimental respecto a la secuencia de frecuencias introducidas en la base.

Relación útil:

\[
\phi_{exp}=\omega_p\Delta t
\]

En grados:

\[
\phi_{exp}=\omega_p\Delta t\left(\frac{180}{\pi}\right)
\]

Donde:

- \(\phi_{exp}\): ángulo de fase experimental.
- \(\omega_p\): frecuencia angular de excitación.
- \(\Delta t\): tiempo de retraso entre la base y el piso superior.

---

### d) Amplitud estacionaria por frecuencia aplicada

Con el mismo gráfico del punto b), determinar la amplitud estacionaria representativa para cada frecuencia aplicada en la base, es decir, para cada tramo de amplitud constante.

Se puede hacer un análisis estadístico de las amplitudes sinusoidales:

- Promedio.
- Desviación estándar.
- Precisión e incertidumbre asociada.

---

### e) Curva de transmisibilidad

Graficar la curva de transmisibilidad \(TR\) contra la frecuencia de excitación en la base. Las frecuencias aplicadas en la base son las anotadas en laboratorio.

Se pueden realizar gráficos para:

- Amplitudes positivas.
- Amplitudes negativas.

La transmisibilidad de desplazamiento puede expresarse como:

\[
TR=\left|\frac{u_p}{u_0}\right|
\]

Donde:

- \(u_p\): amplitud de respuesta del piso superior.
- \(u_0\): amplitud de excitación de la base.

**Comentario teórico:** las curvas de ejemplo del documento corresponden a sistemas de 1 grado de libertad. Para sistemas de múltiples grados de libertad pueden aparecer varios picos en la curva de transmisibilidad, asociados a frecuencias resonantes, naturales o modales.

También puede tomarse en cuenta la incertidumbre asociada a la amplitud de respuesta del edificio para cada frecuencia de excitación y graficarla con un nivel de confianza seleccionado.

---

### f) Amortiguamiento por método de ancho de banda

Aplicar el método de ancho de banda para hallar el amortiguamiento del sistema.

Para una curva de transmisibilidad o FAD, se identifica la amplitud máxima y se calcula:

\[
\frac{TR_{max}}{\sqrt{2}}
\]

Luego se ubican las frecuencias \(f_1\) y \(f_2\) en las intersecciones con esa amplitud. El amortiguamiento se estima como:

\[
\xi=\frac{f_2-f_1}{2f_n}
\]

Donde \(f_n\) es la frecuencia natural asociada al pico de resonancia.

---

### g) Amortiguamiento usando datos de resonancia

Hallar el amortiguamiento del sistema utilizando datos cuando el sistema se encuentra en resonancia y comparar con el resultado del método de ancho de banda.

Una relación usual para estimar el amortiguamiento desde la amplitud máxima de la FAD es:

\[
FAD_{max}=\frac{\sqrt{1+(2\xi)^2}}{2\xi}
\]

---

### h) Curva teórica de transmisibilidad

Graficar la función teórica de la curva de transmisibilidad usando los amortiguamientos determinados por:

1. Vibración libre.
2. Ancho de banda.
3. Resonancia.

Luego superponerla con los puntos experimentales de la curva \(TR\). Comparar y comentar los resultados.

**Figura de referencia:** superposición entre FAD experimental y teórica.

---

### i) Ángulo de fase experimental vs. teórico

Graficar y comparar:

- Ángulo de fase experimental \(\phi_{0,exp}\).
- Ángulo de fase teórico \(\phi_{0,teórico}\).

La comparación debe hacerse usando como insumo la secuencia o vector de frecuencias aplicadas desde la base, anotadas durante la prueba.

**Figura de referencia:** comparación entre curva de ángulo de fase teórica y experimental.

---

### j) Comparación de frecuencias naturales o períodos naturales

Comparar las tres frecuencias naturales, o períodos naturales, obtenidos mediante:

1. Lectura directa de la curva de vibración libre.
2. Transformada Rápida de Fourier aplicada a datos de vibración libre.
3. Curva de transmisibilidad obtenida en vibración forzada.

Comentar similitudes, diferencias y posibles fuentes de error.

---

### k) Comparación de amortiguamientos

Comparar los amortiguamientos obtenidos mediante:

1. Decremento logarítmico.
2. Método de ancho de banda.
3. Prueba de resonancia.

Comentar cuál valor parece más consistente y por qué.

---

### l) Comparación entre edificios

Comparar los resultados entre los dos edificios y comentar los hallazgos. Considerar:

- Diferencias de rigidez.
- Diferencias de período.
- Diferencias de frecuencia natural.
- Diferencias de amortiguamiento.
- Respuesta ante vibración libre.
- Respuesta ante vibración forzada.

---

## Código MATLAB: curvas teóricas de FAD y ángulo de fase

```matlab
%% Curvas teóricas de FAD y ángulo de fase
f = 1.2; % Hz
omegaN = 2*pi*f;
omega = 0:0.01*omegaN:5*omegaN;
ksi = 0.02;
beta = omega/omegaN;
FAD = zeros(length(beta),1);
phi = zeros(length(beta),1);

FAD(:,1) = 1./sqrt((1-beta.^2).^2 + (2*ksi*beta).^2);
phi(:,1) = atan2(2*ksi*beta,(1-beta.^2))*180/pi;

figure
plot(beta,FAD,'-k','LineWidth',2)
xlim([0 5])
ylabel('FAD')
xlabel('razon de frecuencias')

figure
plot(beta,phi,'-k','LineWidth',2)
xlim([0 5])
ylabel('FAD')
xlabel('razon de frecuencias')
```

---

## Código MATLAB: gráfico con dos ejes verticales

```matlab
%% Gráfico con 2 ejes "y" con unidades diferentes
% Para edificio alto

tiempo = X(:,1);
despl = X(:,4);

figure
yyaxis left
plot(tiempo,despl)

acc = X(:,7);
yyaxis right
plot(tiempo,acc)
```

---

## Código MATLAB: superposición base y piso superior

```matlab
%% Gráfico que superpone la historia de desplazamiento de la base y la del piso superior
figure
plot(X(:,1),X(:,2),'-b')
hold on
plot(X(:,1),X(:,4),'-r')
hold on
legend('base','piso superior')
xlabel('tiempo (s)')
ylabel('desplazamiento (mm)')
title('grafico de desplazamiento de la base y del piso superior del edificio alto')
```

---

# 2. Formulación y calibración del modelo matemático del edificio

También se conoce como formulación de la **ecuación de movimiento**.

---

## 2.1 Determinación de la rigidez traslacional de cada grado de libertad

El modelo dinámico para un edificio de 2 pisos, considerando únicamente grados de libertad traslacionales, se representa con:

- Dos masas concentradas: \(m_1\) y \(m_2\).
- Dos desplazamientos laterales: \(u_1\) y \(u_2\).
- Dos rigideces: \(k_1\) y \(k_2\).
- Dos amortiguamientos: \(c_1\) y \(c_2\).
- Posibles fuerzas externas: \(p_1(t)\) y \(p_2(t)\).

**Figura de referencia:** modelo equivalente de edificio de dos pisos representado como sistema de dos grados de libertad traslacionales.

Para determinar la rigidez traslacional de cada grado de libertad, es decir, cada planta, y luego ensamblar la matriz de rigidez y determinar las frecuencias o períodos naturales del edificio, se debe consultar el documento titulado:

> "Ejemplo de determinación de constante de rigidez de resorte y de cada piso del edificio".

### Procedimiento experimental de rigidez

1. Jalar y desplazar los grados de libertad de interés usando un resorte previamente calibrado.
2. Medir la deformación que experimenta el resorte.
3. Medir el desplazamiento del grado de libertad.
4. Usar una cámara de video fija y una referencia para convertir pixeles a milímetros.
5. Calcular la fuerza aplicada:

\[
F=k_{resorte}\Delta_{resorte}
\]

6. Calcular la rigidez del grado de libertad:

\[
k=\frac{F}{\Delta_{GDL}}
\]

Este procedimiento debe repetirse para los 2 niveles del edificio.

---

## 2.2 Formulación y calibración del modelo dinámico del edificio

Para cada edificio realizar lo siguiente.

### a) Matriz de masa

Ensamblar la matriz de masa a partir de los datos de las masas que cargaron los 2 edificios.

Para un sistema de dos grados de libertad:

\[
\mathbf{M}=\begin{bmatrix}
m_1 & 0 \\
0 & m_2
\end{bmatrix}
\]

---

### b) Matriz de rigidez

Ensamblar la matriz de rigidez a partir de los resultados obtenidos en el apartado 2.1.

Para un sistema de dos grados de libertad:

\[
\mathbf{K}=\begin{bmatrix}
k_1+k_2 & -k_2 \\
-k_2 & k_2
\end{bmatrix}
\]

---

### c) Valores y vectores propios

Realizar el análisis de valores y vectores propios a las matrices de masa y rigidez determinadas experimentalmente.

El problema modal se puede expresar como:

\[
\left(\mathbf{K}-\omega_n^2\mathbf{M}\right)\boldsymbol{\phi}_n=\mathbf{0}
\]

Con este análisis se determinan:

- Frecuencias naturales.
- Períodos naturales.
- Formas modales.

Luego se comparan con los valores identificados experimentalmente en vibración libre.

**Nota:** los períodos o frecuencias naturales determinados a partir del análisis de valores y vectores propios pueden diferir de los identificados experimentalmente.

---

### d) Retrocálculo de la rigidez del edificio

Realizar el retrocálculo de la rigidez mediante la ecuación A-4:

\[
m_1m_2\omega_n^4-
\left[m_1k_2+m_2(k_1+k_2)\right]\omega_n^2+k_1k_2=0
\]

Dado que se conocen con exactitud:

- \(m_1\)
- \(m_2\)
- Las dos frecuencias naturales experimentales

se obtienen dos ecuaciones usando los dos \(\omega_n\) experimentales. Recordar convertir las frecuencias de Hz a rad/s:

\[
\omega_n=2\pi f_n
\]

Luego se resuelven las dos incógnitas:

- \(k_1\)
- \(k_2\)

Se comparan las soluciones obtenidas para \(k_1\) y \(k_2\) con las determinadas en el apartado 2.1.

Puede haber múltiples soluciones. Se deben escoger los valores de \(k_1\) y \(k_2\) que permitan obtener, a través del análisis de valores y vectores propios, las mismas frecuencias naturales experimentales, o al menos una coincidencia exacta para la frecuencia del modo fundamental.

---

### e) Ecuación de movimiento calibrada

Resumir:

1. La ecuación de movimiento finalmente calibrada.
2. Las frecuencias naturales que se obtienen de ella.
3. Las formas modales.

La ecuación de movimiento libre sin excitación externa puede escribirse como:

\[
\mathbf{M}\ddot{\mathbf{u}}+\mathbf{K}\mathbf{u}=\mathbf{0}
\]

Para el caso de dos grados de libertad:

\[
\begin{bmatrix}
m_1 & 0 \\
0 & m_2
\end{bmatrix}
\begin{bmatrix}
\ddot{u}_1 \\
\ddot{u}_2
\end{bmatrix}
+
\begin{bmatrix}
k_1+k_2 & -k_2 \\
-k_2 & k_2
\end{bmatrix}
\begin{bmatrix}
u_1 \\
u_2
\end{bmatrix}
=
\begin{bmatrix}
0 \\
0
\end{bmatrix}
\]

---

# 3. Simulación numérica de la respuesta del edificio ante solicitaciones sísmicas

La simulación se aplica a solicitaciones sísmicas introducidas en la mesa vibratoria y se compara con la respuesta experimental en el tiempo.

Una vez que se tienen las matrices de masa y rigidez calibradas, de modo que exista concordancia entre las frecuencias naturales experimentales y las obtenidas mediante valores y vectores propios, se puede usar la **integral de Duhamel** para obtener la respuesta modal de cada modo ante la aceleración sísmica aplicada en la base.

La respuesta total del sistema ante la historia sísmica se obtiene sumando las respuestas modales multiplicadas por sus formas modales.

---

## Integral de Duhamel para respuesta modal

Para el modo \(n\), la respuesta modal se puede expresar como:

\[
q_n(t)=
-\frac{\Gamma_n}{\omega_{Dn}}
\int_0^t
\ddot{u}_g(\tau)
e^{-\xi_n\omega_n(t-\tau)}
\sin[\omega_{Dn}(t-\tau)]
\,d\tau
\]

Donde:

- \(q_n(t)\): respuesta modal del modo \(n\).
- \(\Gamma_n\): factor de participación modal.
- \(\omega_n\): frecuencia circular natural del modo \(n\).
- \(\omega_{Dn}\): frecuencia circular amortiguada del modo \(n\).
- \(\xi_n\): razón de amortiguamiento modal.
- \(\ddot{u}_g(\tau)\): aceleración sísmica aplicada en la base.

El factor de participación modal se calcula como:

\[
\Gamma_n=\frac{\boldsymbol{\phi}_n^T\mathbf{m}\mathbf{1}}{M_n}
\]

La respuesta real del sistema se calcula sumando las contribuciones modales:

\[
\mathbf{u}(t)=
\boldsymbol{\phi}_1q_1(t)+\boldsymbol{\phi}_2q_2(t)
\]

Para dos grados de libertad:

\[
\begin{bmatrix}
u_1(t) \\
u_2(t)
\end{bmatrix}
=
\begin{bmatrix}
\phi_{11} \\
\phi_{21}
\end{bmatrix}q_1(t)
+
\begin{bmatrix}
\phi_{12} \\
\phi_{22}
\end{bmatrix}q_2(t)
\]

---

## Código MATLAB: implementación de respuesta sísmica con Duhamel

```matlab
%% Propiedades dinámicas del edificio
m = [2,0; 0,2]; % matriz de masa en kg
k = [230,-100; -100,100]; % matriz de rigidez en N/m
ksi = [0.03,0.04]; % vector de razón de amortiguamiento modal
n = size(m,1);

[V D] = eig(k,m); % V: vectores propios, D: valores propios wn^2
M = V'*m*V; % matriz de masa modal
C = 2*ksi'.*diag(M).*diag(sqrt(D)); % matriz de amortiguamiento modal
c = V*diag(C)*V'; % matriz de amortiguamiento proporcional
w = diag(sqrt(D)); % frecuencias modales circulares
w1 = w(1);
w2 = w(2);

% Frecuencias modales amortiguadas
w1D = w1*sqrt(1-ksi(1)^2);
w2D = w2*sqrt(1-ksi(2)^2);
```

---

## Código MATLAB: graficar formas modales

```matlab
%% Graficar formas modales
V1 = zeros(length(V(:,1))+1,1);
V2 = zeros(length(V(:,2))+1,1);
V1(2:end,1) = V(:,1);
V2(2:end,1) = V(:,2);

figure
subplot(1,2,1)
plot(V1,[0,1,2],'o-b')
xlabel('Amplitud modal'), ylabel('grado de libertad'), title(['1era forma modal'])

subplot(1,2,2)
plot(V2,[0,1,2],'o-b')
xlabel('Amplitud modal'), ylabel('grado de libertad'), title(['2da forma modal'])
```

---

## Código MATLAB: datos de aceleración de la mesa vibratoria

```matlab
%% Datos de aceleración de la mesa vibratoria
dt = 0.01; % intervalo de tiempo de las muestras de la historia de aceleración
acc_data = load('nombre_del_sismo.txt'); % cargar historia de sismo al Workspace
% Es importante asegurarse de que la unidad esté en m/s^2

point = length(acc_data); % puntos de datos en la historia de aceleración
time = 0:dt:(point-1)*dt; % vector de tiempo

% Graficar datos de aceleración de la mesa vibratoria
figure
plot(time,acc_data,'-b')
xlabel('tiempo (s)'), ylabel('m/s^2'), ...
    title(['historia de aceleracion de la meas vibratoria'])
```

---

## Código MATLAB: respuesta al impulso unitario

```matlab
%% Respuesta al impulso unitario
h1 = (1/w1D)*exp(-ksi(1)*w1*time).*sin(w1D*time);
h2 = (1/w2D)*exp(-ksi(2)*w2*time).*sin(w2D*time);
```

---

## Código MATLAB: factor de participación modal

```matlab
%% Factor de participacion modal
F1 = V(:,1)'*diag(m)/M(1,1);
F2 = V(:,2)'*diag(m)/M(2,2);
```

---

## Código MATLAB: integral de Duhamel versión eficiente

```matlab
%% Integral de Duhamel versión eficiente
% Definir longitud de respuesta al impulso unitario que se desea tomar, en segundos
Th1 = 60;
Th2 = 30;

% Cantidad de puntos en la longitud de respuesta tomada
L1 = Th1/dt;
L2 = Th2/dt;

% Respuesta al impulso unitario de los 2 modos
h1 = h1(1:L1);
h2 = h2(1:L2);

% Graficar respuestas a los impulsos unitarios
figure
subplot(2,1,1)
plot(time(1:L1),h1,'-b')
xlabel('tiempo (s)'), ylabel('s/rad'), title(['Respuesta del 1er modo ante impulso unitario'])

subplot(2,1,2)
plot(time(1:L2),h2,'-b')
xlabel('tiempo (s)'), ylabel('s/rad'), title(['Respuesta del 2do modo ante impulso unitario'])

q = zeros(2,point+L1-1); % vector para almacenar respuesta modal en el tiempo
% Se usa point+L1-1 para tomar en cuenta el aporte del último dato de acc_data.
% Se asume que L1 tiene más puntos porque es el modo fundamental de período más largo.

% Integral de Duhamel sumando vectores de respuestas ante impulsos sísmicos
tic
for jj = 1:1:(point)
    q(1,jj:(jj+L1-1)) = q(1,jj:(jj+L1-1)) - dt*acc_data(jj)*h1;
    q(2,jj:(jj+L2-1)) = q(2,jj:(jj+L2-1)) - dt*acc_data(jj)*h2;
end
toc

% Multiplicar por el factor de participación modal para obtener respuestas modales
q(1,:) = q(1,:)*F1;
q(2,:) = q(2,:)*F2;
```

---

## Código MATLAB: respuestas modales en el tiempo

```matlab
%% Graficar las respuestas modales en el tiempo
figure
subplot(2,1,1)
plot(time,q(1,1:point),'-b')
xlabel('tiempo (s)'), title(['Respuesta del 1er modo ante el sismo'])

subplot(2,1,2)
plot(time,q(2,1:point),'-b')
xlabel('tiempo (s)'), title(['Respuesta del 2do modo ante el sismo'])
```

---

## Código MATLAB: desplazamientos por grado de libertad

```matlab
%% El vector de desplazamiento en el tiempo
% Se suma el aporte de todas las respuestas modales
u = V(:,1)*q(1,:) + V(:,2)*q(2,:);

figure
subplot(2,1,1)
plot(time,u(1,1:point),'-b')
xlabel('tiempo (s)'), ylabel('desplazamiento (m)'), title(['desplazamiento del piso 1 u_1(t)'])

subplot(2,1,2)
plot(time,u(2,1:point),'-b')
xlabel('tiempo (s)'), ylabel('desplazamiento (m)'), title(['desplazamiento del piso 2 u_2(t)'])
```

---

## Código MATLAB: aporte modal a los desplazamientos

```matlab
%% Revisando el aporte de cada respuesta modal a los desplazamientos en los grados de libertad
uq1 = V(:,1)*q(1,:); % desplazamiento debido al modo 1
uq2 = V(:,2)*q(2,:); % desplazamiento debido al modo 2

figure
subplot(2,1,1)
plot(time,u(1,1:point),'-b')
hold on
plot(time,uq1(1,1:point),':r')
hold off
xlabel('tiempo (s)'), ylabel('desplazamiento (m)'), ...
    title(['comparacion del desplazamiento total con el contribuido por el 1er modo piso 1 u_1(t)'])
legend('total','modo 1')

subplot(2,1,2)
plot(time,u(2,1:point),'-b')
hold on
plot(time,uq1(2,1:point),':r')
legend('total','modo 1')
xlabel('tiempo (s)'), ylabel('desplazamiento (m)'), title(['piso 2 u_2(t)'])
hold off
```

---

## Código MATLAB: desplazamientos máximos

```matlab
%% Cálculo de los desplazamientos máximos y sus ubicaciones
umax = zeros(2,1); % desplazamientos máximos en cada grado de libertad
umaxposi = zeros(2,1); % posición, en puntos, de los desplazamientos máximos

[umax(1,1), umaxposi(1,1)] = max(abs(u(1,:))); % máximo en GDL 1
[umax(2,1), umaxposi(2,1)] = max(abs(u(2,:))); % máximo en GDL 2

umaxseg = umaxposi*dt; % convertir posición del máximo a segundos
```

---

## Resultados que deben mostrarse para un sismo selecto y para cada edificio

Para un sismo selecto, mostrar para cada edificio:

### a) Aceleración de la mesa vibratoria

Gráfico de la historia de aceleración en la mesa vibratoria.

### b) Desplazamiento relativo del piso superior respecto a la base

Gráfico de la historia de desplazamiento relativo del piso superior respecto a la base.

Se calcula como:

\[
u_{relativo}=u_{piso\ superior, absoluto}-u_{mesa}
\]

### c) Aceleración del piso superior

Gráfico de la historia de aceleración del piso superior del edificio.

### d) Estudio y análisis de las historias

Obtener la siguiente información:

1. Aceleración máxima en la mesa y tiempo en que ocurrió.
2. Desplazamiento relativo máximo del edificio y tiempo en que ocurrió.
3. Aceleración absoluta máxima del edificio y tiempo en que ocurrió.
4. Listar la información anterior en una tabla de comparación entre diferentes sismos.
5. Indicar si el edificio se dañó o colapsó en algún sismo.
6. Analizar si de la historia de aceleración de la mesa se puede obtener información sobre la frecuencia con que la mesa se sacudió durante la ocurrencia de los máximos.
7. Indicar, en forma general, con cuál frecuencia oscila el edificio durante el sismo.
8. Si ocurrió daño o colapso, indicar en qué tiempo ocurrió y si se relaciona con la aceleración máxima o la frecuencia del sismo en ese instante.

### e) Comparación teoría vs experimento

Superponer:

- Historia de desplazamiento relativo del piso superior predicha por la teoría mediante integración numérica de la integral de Duhamel.
- Historia experimental de desplazamiento relativo.

Luego analizar y discutir los hallazgos.

---

## Notas finales de presentación gráfica

1. Las historias de aceleración de la mesa, desplazamiento relativo y aceleración absoluta del edificio deben graficarse como gráficos paralelos usando `subplot(k,n,m)` en Matlab.
2. Deben tener la misma escala e inicio en el tiempo para facilitar la comparación, especialmente en acercamientos.
3. Es importante hacer acercamientos suficientes para visualizar el evento principal y el comportamiento en amplitudes máximas absolutas.
4. Como hay 2 edificios, se recomienda graficar en paralelo las historias de desplazamiento relativo y aceleración absoluta de ambos edificios para facilitar la comparación del mismo evento sísmico.
5. Los máximos de ambos edificios deben listarse en una tabla comparativa entre los diferentes sismos, indicando si hubo daño o colapso.

---

# Checklist rápido para Claude

Usar este checklist para revisar si un informe cumple con el documento:

## Antes del análisis

- [ ] Describe dimensiones, material, secciones, conexiones y empotramiento.
- [ ] Describe método constructivo, fases y dificultades.

## Vibración libre

- [ ] Calcula períodos desde desplazamiento y aceleración.
- [ ] Identifica período fundamental.
- [ ] Calcula amortiguamiento por decremento logarítmico.
- [ ] Presenta promedio y desviación estándar.
- [ ] Aplica FFT a desplazamiento y aceleración.
- [ ] Identifica frecuencias dominantes.
- [ ] Compara historias de desplazamiento y aceleración entre edificios.

## Vibración forzada

- [ ] Superpone desplazamiento y aceleración del piso superior.
- [ ] Superpone desplazamiento de base y piso superior.
- [ ] Presenta acercamientos antes, durante y después de resonancia.
- [ ] Calcula tiempo de retraso y ángulo de fase experimental.
- [ ] Calcula amplitud estacionaria por frecuencia.
- [ ] Grafica transmisibilidad.
- [ ] Calcula amortiguamiento por ancho de banda.
- [ ] Calcula amortiguamiento por resonancia.
- [ ] Superpone curva teórica y experimental.
- [ ] Compara ángulo de fase teórico y experimental.
- [ ] Compara frecuencias por los tres métodos.
- [ ] Compara amortiguamientos por los tres métodos.
- [ ] Compara ambos edificios.

## Modelo matemático

- [ ] Determina rigidez experimental por nivel.
- [ ] Ensambla matriz de masa.
- [ ] Ensambla matriz de rigidez.
- [ ] Realiza análisis modal.
- [ ] Retrocacula rigideces con frecuencias experimentales.
- [ ] Presenta ecuación de movimiento calibrada.
- [ ] Presenta frecuencias y formas modales.

## Simulación sísmica

- [ ] Grafica aceleración de la mesa.
- [ ] Grafica desplazamiento relativo del piso superior.
- [ ] Grafica aceleración del piso superior.
- [ ] Calcula máximos y tiempos de ocurrencia.
- [ ] Presenta tabla comparativa por sismo y edificio.
- [ ] Compara Duhamel contra respuesta experimental.
- [ ] Discute daño o colapso, si aplica.
