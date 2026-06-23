# Ejemplos Chopra — Dinámica

**Curso:** IC-0502-2026-I-G02 Dinámica  
**Profesor:** G. Santana, EIC/UCR  
**Tema:** Ejemplos de vibración libre, periodo natural, razón de amortiguamiento, rigidez, masa y coeficiente de amortiguamiento.

---

## Ejemplo A

### Enunciado

Determinar el periodo natural de vibración y la razón de amortiguamiento del marco de acrílico mostrado en la figura, usando el registro de aceleración de vibración libre adjunto.

### Datos extraídos del registro

Los valores máximos de aceleración y los instantes de tiempo en los que ocurren pueden ser leídos del registro de vibración u obtenidos de los datos almacenados durante el experimento.

| Pico | Tiempo, $t_i$ (s) | $\ddot{u}_i$ (g) |
|---|---:|---:|
| I | 1.110 | 0.915 |
| II | 3.844 | 0.076 |

### Cálculo del periodo amortiguado

Se sabe que entre ambos picos hay 10 ciclos completos.

$$
T_D = \frac{3.844 - 1.110}{10}
$$

$$
T_D = 0.273\,s
$$

### Cálculo de la razón de amortiguamiento

$$
\xi =
\frac{1}{2\pi(10)}
\ln\left(
\frac{0.915g}{0.076g}
\right)
$$

$$
\xi = 0.0396 = 3.96\%
$$

### Resultado

| Parámetro | Valor |
|---|---:|
| Periodo amortiguado, $T_D$ | 0.273 s |
| Razón de amortiguamiento, $\xi$ | 0.0396 |
| Razón de amortiguamiento | 3.96 % |

---

## Ejemplo B

### Enunciado

Un tanque de concreto reforzado sobre una única columna de 12 m de altura, ubicado en el Aeropuerto de Valdivia, Chile, no sufrió daño debido al terremoto de mayo de 1960.

Cuando el tanque está lleno, la estructura puede analizarse como un sistema de un grado de libertad.

Se realiza una prueba de vibración libre con un cable atado al tanque. El cable aplica una fuerza de 80 kN y desplaza el tanque 50 mm. Luego, el cable se corta repentinamente y se graba la vibración resultante.

Al final de cuatro ciclos completos se registran:

- Tiempo: 2.0 s
- Amplitud final: 25 mm

Se pide obtener:

1. Razón de amortiguamiento.
2. Periodo natural de vibración no amortiguada.
3. Rigidez.
4. Peso o masa equivalente.
5. Coeficiente de amortiguamiento.
6. Número de ciclos requeridos para que el desplazamiento decrezca a 5 mm.

---

### a) Razón de amortiguamiento

Datos:

$$
u_i = 50\,mm
$$

$$
j = 4
$$

$$
u_{i+j} = 25\,mm
$$

Fórmula:

$$
\xi =
\frac{1}{2\pi j}
\ln\left(
\frac{u_i}{u_{i+j}}
\right)
$$

Sustitución:

$$
\xi =
\frac{1}{2\pi(4)}
\ln\left(
\frac{50}{25}
\right)
$$

Resultado:

$$
\xi = 0.0276 = 2.76\%
$$

La suposición de amortiguamiento pequeño implícita en la ecuación anterior es válida.

---

### b) Periodo natural de vibración no amortiguada

El periodo amortiguado se obtiene como:

$$
T_D = \frac{2.0\,s}{4}
$$

$$
T_D = 0.5\,s
$$

Como el amortiguamiento es pequeño:

$$
T_n \approx T_D
$$

Por tanto:

$$
T_n \approx 0.5\,s
$$

---

### c) Rigidez

Datos:

$$
F = 80\,kN = 80\times 10^3\,N
$$

$$
\Delta = 50\,mm = 0.05\,m
$$

Fórmula:

$$
k = \frac{F}{\Delta}
$$

Sustitución:

$$
k =
\frac{80\times 10^3\,N}{0.05\,m}
$$

Resultado:

$$
k = 1.6\times 10^6\,N/m
$$

$$
k = 1600\,kN/m
$$

---

### d) Masa equivalente

Primero se calcula la frecuencia natural circular:

$$
\omega_n = \frac{2\pi}{T_n}
$$

Sustitución:

$$
\omega_n =
\frac{2\pi}{0.5\,s}
$$

Resultado:

$$
\omega_n = 12.57\,rad/s
$$

Luego se despeja la masa a partir de:

$$
\omega_n = \sqrt{\frac{k}{m}}
$$

Por tanto:

$$
m = \frac{k}{\omega_n^2}
$$

Sustitución:

$$
m =
\frac{1.6\times 10^6\,N/m}{(12.57\,rad/s)^2}
$$

Resultado:

$$
m = 10126\,kg
$$

---

### e) Coeficiente de amortiguamiento

Fórmula:

$$
c = \xi(2\sqrt{km})
$$

Sustitución:

$$
c =
0.0276
\left[
2\sqrt{(1.6\times 10^6)(10126)}
\right]
$$

Resultado:

$$
c = 7026\,N\cdot s/m
$$

---

### f) Número de ciclos para que el desplazamiento decrezca a 5 mm

Se utiliza la relación aproximada:

$$
\xi \approx
\frac{1}{2\pi j}
\ln\left(
\frac{u_1}{u_{1+j}}
\right)
$$

Despejando:

$$
j \approx
\frac{1}{2\pi\xi}
\ln\left(
\frac{u_1}{u_{1+j}}
\right)
$$

Datos:

$$
u_1 = 50\,mm
$$

$$
u_{1+j} = 5\,mm
$$

$$
\xi = 0.0276
$$

Sustitución:

$$
j \approx
\frac{1}{2\pi(0.0276)}
\ln\left(
\frac{50}{5}
\right)
$$

Resultado:

$$
j = 13.28 \approx 13\,ciclos
$$

---

## Ejemplo C

### Enunciado

El peso del agua requerida para llenar el tanque del Ejemplo B es de 40000 kg.

Determinar:

1. Periodo natural de vibración.
2. Razón de amortiguamiento de la estructura con el tanque lleno.

---

### Datos

Del Ejemplo B:

$$
m_{estructura} = 10132\,kg
$$

Masa del agua:

$$
m_{agua} = 40000\,kg
$$

Masa total:

$$
m = 10132 + 40000
$$

$$
m = 50132\,kg
$$

Rigidez:

$$
k = 1.6\times 10^6\,N/m
$$

Coeficiente de amortiguamiento:

$$
c = 7026\,N\cdot s/m
$$

---

### Periodo natural de vibración

Fórmula:

$$
T_n = 2\pi\sqrt{\frac{m}{k}}
$$

Sustitución:

$$
T_n =
2\pi
\sqrt{
\frac{50132}{1.6\times 10^6}
}
$$

Resultado:

$$
T_n = 1.11\,s
$$

---

### Razón de amortiguamiento

Fórmula:

$$
\xi =
\frac{c}{2\sqrt{km}}
$$

Sustitución:

$$
\xi =
\frac{7026}{
2\sqrt{(1.6\times 10^6)(50132)}
}
$$

Resultado:

$$
\xi = 0.0124 = 1.24\%
$$

### Observación

La razón de amortiguamiento es menor con el tanque lleno porque la masa total aumenta. Al aumentar la masa, también aumenta el amortiguamiento crítico:

$$
c_{cr} = 2\sqrt{km}
$$

Por tanto, aunque el coeficiente de amortiguamiento $c$ se mantenga igual, la razón:

$$
\xi = \frac{c}{c_{cr}}
$$

disminuye.

---

# Fórmulas importantes extraídas

## Periodo amortiguado usando varios ciclos

$$
T_D =
\frac{t_{i+j}-t_i}{j}
$$

## Decremento logarítmico aproximado

$$
\xi \approx
\frac{1}{2\pi j}
\ln\left(
\frac{u_i}{u_{i+j}}
\right)
$$

## Frecuencia natural circular

$$
\omega_n =
\frac{2\pi}{T_n}
$$

## Relación entre rigidez, masa y frecuencia natural

$$
\omega_n =
\sqrt{\frac{k}{m}}
$$

## Rigidez a partir de fuerza y desplazamiento estático

$$
k =
\frac{F}{\Delta}
$$

## Masa equivalente

$$
m =
\frac{k}{\omega_n^2}
$$

## Coeficiente de amortiguamiento crítico

$$
c_{cr} =
2\sqrt{km}
$$

## Coeficiente de amortiguamiento

$$
c =
\xi c_{cr}
$$

$$
c =
\xi(2\sqrt{km})
$$

## Razón de amortiguamiento

$$
\xi =
\frac{c}{2\sqrt{km}}
$$

## Número de ciclos para alcanzar una amplitud objetivo

$$
j \approx
\frac{1}{2\pi\xi}
\ln\left(
\frac{u_1}{u_{1+j}}
\right)
$$

---

# Notas para usar como contexto en Claude

Este documento contiene ejemplos resueltos de dinámica estructural enfocados en vibración libre de sistemas de un grado de libertad.

Los ejemplos muestran cómo:

- Obtener el periodo amortiguado a partir de picos separados por varios ciclos.
- Calcular la razón de amortiguamiento mediante decremento logarítmico.
- Aproximar el periodo no amortiguado cuando el amortiguamiento es pequeño.
- Calcular rigidez a partir de una prueba estática de fuerza-desplazamiento.
- Obtener masa equivalente usando $\omega_n^2 = k/m$.
- Calcular el coeficiente de amortiguamiento a partir de $c = \xi(2\sqrt{km})$.
- Evaluar el efecto de aumentar la masa del sistema sobre el periodo natural y la razón de amortiguamiento.
