# Sistema de 2 grados de libertad

**Archivo fuente:** `Sistema de 2 grados de libertad.pdf`  
**Tipo de documento:** apunte de clase / derivación matemática.  
**Uso recomendado:** contexto técnico para resolver o explicar sistemas lineales de dos grados de libertad, matrices de masa, amortiguamiento y rigidez, vibración libre no amortiguada, frecuencias naturales y modos de oscilación.

## Cita IEEE sugerida

[1] Universidad de Costa Rica, “Sistema de 2 grados de libertad,” material de clase de Vibraciones Mecánicas, s. f.

> Nota: el PDF no muestra autor personal ni fecha explícita. Por eso se cita como material de clase sin fecha (`s. f.`).

---

## 1. Idea central del documento

El documento desarrolla el modelo dinámico de un sistema mecánico con **dos grados de libertad (2 GDL)**. El sistema está compuesto por:

- dos masas: $m_1$ y $m_2$;
- dos resortes lineales: $k_1$ y $k_2$;
- dos amortiguadores viscosos lineales: $c_1$ y $c_2$;
- dos desplazamientos independientes: $x_1(t)$ y $x_2(t)$;
- dos fuerzas externas: $p_1(t)$ y $p_2(t)$.

El objetivo principal es obtener la ecuación matricial del movimiento y luego analizar el caso particular de **vibración libre no amortiguada**, para determinar:

1. frecuencias naturales;
2. períodos naturales;
3. modos de oscilación.

---

## 2. Modelo físico del sistema

El sistema se idealiza de la siguiente manera:

```text
Pared fija -- k1,c1 -- m1 -- k2,c2 -- m2
                         |              |
                        x1(t)          x2(t)
```

La primera masa $m_1$ está conectada a una pared mediante el resorte $k_1$ y el amortiguador $c_1$. Además, $m_1$ y $m_2$ están conectadas entre sí mediante el resorte $k_2$ y el amortiguador $c_2$.

Los desplazamientos positivos se toman hacia la derecha.

---

## 3. Ecuaciones de movimiento por masa

### 3.1 Ecuación de la masa $m_1$

Aplicando la segunda ley de Newton sobre la masa $m_1$:

$$
m_1\ddot{x}_1 + k_1x_1 + c_1\dot{x}_1 - k_2(x_2-x_1)-c_2(\dot{x}_2-\dot{x}_1)=p_1(t)
$$

Al ordenar términos:

$$
m_1\ddot{x}_1+(c_1+c_2)\dot{x}_1-c_2\dot{x}_2+(k_1+k_2)x_1-k_2x_2=p_1(t)
$$

### 3.2 Ecuación de la masa $m_2$

Para la masa $m_2$:

$$
m_2\ddot{x}_2+k_2(x_2-x_1)+c_2(\dot{x}_2-\dot{x}_1)=p_2(t)
$$

Al ordenar términos:

$$
m_2\ddot{x}_2-c_2\dot{x}_1+c_2\dot{x}_2-k_2x_1+k_2x_2=p_2(t)
$$

---

## 4. Forma matricial del equilibrio dinámico

La forma matricial general del sistema es:

$$
\mathbf{M}\ddot{\mathbf{x}}+\mathbf{C}\dot{\mathbf{x}}+\mathbf{K}\mathbf{x}=\mathbf{P}(t)
$$

con:

$$
\mathbf{x}=\begin{Bmatrix}x_1\\x_2\end{Bmatrix},\qquad
\dot{\mathbf{x}}=\begin{Bmatrix}\dot{x}_1\\\dot{x}_2\end{Bmatrix},\qquad
\ddot{\mathbf{x}}=\begin{Bmatrix}\ddot{x}_1\\\ddot{x}_2\end{Bmatrix}
$$

$$
\mathbf{P}(t)=\begin{Bmatrix}p_1(t)\\p_2(t)\end{Bmatrix}
$$

### 4.1 Matriz de masa

$$
\mathbf{M}=\begin{bmatrix}
m_1 & 0\\
0 & m_2
\end{bmatrix}
$$

### 4.2 Matriz de amortiguamiento

$$
\mathbf{C}=\begin{bmatrix}
c_1+c_2 & -c_2\\
-c_2 & c_2
\end{bmatrix}
$$

### 4.3 Matriz de rigidez

$$
\mathbf{K}=\begin{bmatrix}
k_1+k_2 & -k_2\\
-k_2 & k_2
\end{bmatrix}
$$

---

## 5. Caso particular: vibración libre no amortiguada

Para vibración libre no amortiguada se eliminan las fuerzas externas y el amortiguamiento:

$$
\mathbf{P}(t)=\mathbf{0}, \qquad \mathbf{C}=\mathbf{0}
$$

La ecuación queda:

$$
\mathbf{M}\ddot{\mathbf{x}}+\mathbf{K}\mathbf{x}=\mathbf{0}
$$

Esta es una ecuación diferencial vectorial homogénea de segundo orden con coeficientes constantes.

---

## 6. Suposición de respuesta armónica

Se supone una solución armónica de la forma:

$$
\mathbf{x}(t)=\mathbf{c}\sin(\omega_n t+\phi)
$$

Entonces:

$$
\ddot{\mathbf{x}}(t)=-\omega_n^2\mathbf{c}\sin(\omega_n t+\phi)
$$

Sustituyendo en la ecuación de movimiento:

$$
\mathbf{M}\left[-\omega_n^2\mathbf{c}\sin(\omega_n t+\phi)\right]
+\mathbf{K}\left[\mathbf{c}\sin(\omega_n t+\phi)\right]=\mathbf{0}
$$

Factorizando:

$$
\left[\mathbf{K}-\omega_n^2\mathbf{M}\right]\mathbf{c}\sin(\omega_n t+\phi)=\mathbf{0}
$$

Como $\sin(\omega_n t+\phi)$ no es cero para todo instante, debe cumplirse:

$$
\left[\mathbf{K}-\omega_n^2\mathbf{M}\right]\mathbf{c}=\mathbf{0}
$$

Definiendo:

$$
\lambda=\omega_n^2
$$

se obtiene el problema de valores propios:

$$
\left[\mathbf{K}-\lambda\mathbf{M}\right]\mathbf{c}=\mathbf{0}
$$

---

## 7. Problema de valores y vectores propios

La ecuación:

$$
\mathbf{K}\mathbf{c}=\lambda\mathbf{M}\mathbf{c}
$$

es un problema matricial de valores propios. Aquí:

- $\lambda$ es un valor propio;
- $\omega_n=\sqrt{\lambda}$ es una frecuencia natural angular;
- $\mathbf{c}$ es un vector propio, también llamado **modo de oscilación**.

Para que exista una solución no trivial, debe cumplirse:

$$
\det(\mathbf{K}-\lambda\mathbf{M})=0
$$

---

## 8. Ecuación característica general para el sistema de 2 GDL

Con las matrices del sistema:

$$
\det\left(
\begin{bmatrix}
k_1+k_2 & -k_2\\
-k_2 & k_2
\end{bmatrix}
-
\lambda
\begin{bmatrix}
m_1 & 0\\
0 & m_2
\end{bmatrix}
\right)=0
$$

Esto equivale a:

$$
\begin{vmatrix}
(k_1+k_2)-\lambda m_1 & -k_2\\
-k_2 & k_2-\lambda m_2
\end{vmatrix}=0
$$

Desarrollando el determinante:

$$
\left[(k_1+k_2)-\lambda m_1\right](k_2-\lambda m_2)-k_2^2=0
$$

Al ordenar, se obtiene:

$$
\lambda^2-
\frac{m_1k_2+m_2k_1+m_2k_2}{m_1m_2}\lambda+
\frac{k_1k_2}{m_1m_2}=0
$$

---

## 9. Caso experimental simplificado: $k_1=k_2=k$ y $m_1=m_2=m$

Para el caso donde ambas masas y ambos resortes son iguales:

$$
k_1=k_2=k,\qquad m_1=m_2=m
$$

la ecuación característica se reduce a:

$$
\lambda^2-3\frac{k}{m}\lambda+\frac{k^2}{m^2}=0
$$

Los valores propios son:

$$
\lambda_1=\frac{3-\sqrt{5}}{2}\frac{k}{m}\approx0.38197\frac{k}{m}
$$

$$
\lambda_2=\frac{3+\sqrt{5}}{2}\frac{k}{m}\approx2.61803\frac{k}{m}
$$

Como $\omega_n=\sqrt{\lambda}$:

$$
\omega_n^{(1)}=0.61803\sqrt{\frac{k}{m}}
$$

$$
\omega_n^{(2)}=1.61803\sqrt{\frac{k}{m}}
$$

---

## 10. Períodos naturales

Los períodos naturales se calculan con:

$$
T=\frac{2\pi}{\omega_n}
$$

### 10.1 Primer período natural

$$
T_1=\frac{2\pi}{0.61803\sqrt{k/m}}
$$

$$
T_1=10.166\sqrt{\frac{m}{k}}\;\text{s}
$$

### 10.2 Segundo período natural

$$
T_2=\frac{2\pi}{1.61803\sqrt{k/m}}
$$

$$
T_2=3.883\sqrt{\frac{m}{k}}\;\text{s}
$$

---

## 11. Modos de oscilación

Los modos se obtienen sustituyendo cada valor propio en:

$$
(\mathbf{K}-\lambda\mathbf{M})\mathbf{c}=\mathbf{0}
$$

Cada modo define una **dirección de movimiento relativo** entre las masas. La magnitud absoluta del vector no es única; por eso se puede normalizar fijando una de sus componentes.

---

## 12. Primer modo de oscilación

Se toma:

$$
\mathbf{c}_1=\begin{Bmatrix}C_{11}\\C_{12}\end{Bmatrix}
$$

Como el vector solo define una dirección, se puede asumir:

$$
C_{11}=1
$$

Para:

$$
\lambda_1=0.38197\frac{k}{m}
$$

se obtiene el sistema:

$$
\begin{bmatrix}
1.61803k & -k\\
-k & 0.61803k
\end{bmatrix}
\begin{Bmatrix}
1\\C_{12}
\end{Bmatrix}
=
\begin{Bmatrix}
0\\0
\end{Bmatrix}
$$

Usando la segunda fila:

$$
-k(1)+0.61803k(C_{12})=0
$$

$$
C_{12}=1.61803
$$

Por tanto:

$$
\mathbf{c}_1=\begin{Bmatrix}1\\1.61803\end{Bmatrix}
$$

**Interpretación:** en el primer modo, ambas masas se mueven en la misma dirección. La segunda masa tiene una amplitud relativa mayor.

---

## 13. Segundo modo de oscilación

Se toma:

$$
\mathbf{c}_2=\begin{Bmatrix}C_{21}\\C_{22}\end{Bmatrix}
$$

Asumiendo:

$$
C_{21}=1
$$

Para:

$$
\lambda_2=2.61803\frac{k}{m}
$$

se obtiene:

$$
\begin{bmatrix}
-0.61803k & -k\\
-k & -1.61803k
\end{bmatrix}
\begin{Bmatrix}
1\\C_{22}
\end{Bmatrix}
=
\begin{Bmatrix}
0\\0
\end{Bmatrix}
$$

Usando la segunda fila:

$$
-k(1)-1.61803k(C_{22})=0
$$

$$
C_{22}=-0.61803
$$

Por tanto:

$$
\mathbf{c}_2=\begin{Bmatrix}1\\-0.61803\end{Bmatrix}
$$

**Interpretación:** en el segundo modo, las masas se mueven en direcciones opuestas.

---

## 14. Resumen de resultados clave

| Magnitud | Resultado |
|---|---:|
| Valor propio 1 | $\lambda_1=0.38197\dfrac{k}{m}$ |
| Valor propio 2 | $\lambda_2=2.61803\dfrac{k}{m}$ |
| Frecuencia angular natural 1 | $\omega_n^{(1)}=0.61803\sqrt{\dfrac{k}{m}}$ |
| Frecuencia angular natural 2 | $\omega_n^{(2)}=1.61803\sqrt{\dfrac{k}{m}}$ |
| Período natural 1 | $T_1=10.166\sqrt{\dfrac{m}{k}}\;\text{s}$ |
| Período natural 2 | $T_2=3.883\sqrt{\dfrac{m}{k}}\;\text{s}$ |
| Primer modo | $\mathbf{c}_1=\begin{Bmatrix}1\\1.61803\end{Bmatrix}$ |
| Segundo modo | $\mathbf{c}_2=\begin{Bmatrix}1\\-0.61803\end{Bmatrix}$ |

---

## 15. Conceptos importantes para Claude

### Grado de libertad

Un grado de libertad es una coordenada independiente necesaria para describir la posición del sistema. En este caso hay dos coordenadas: $x_1(t)$ y $x_2(t)$.

### Frecuencia natural

Es la frecuencia con la que el sistema tiende a vibrar cuando se le perturba y luego se deja libre, sin excitación externa.

### Modo de oscilación

Es la forma relativa en que se mueven las masas cuando el sistema vibra en una frecuencia natural específica.

### Valor propio

En este problema:

$$
\lambda=\omega_n^2
$$

Por tanto, cada valor propio permite obtener una frecuencia natural.

### Vector propio

El vector propio asociado a cada valor propio representa el modo de oscilación.

---

## 16. Notas de consistencia

- En el segundo modo, el documento menciona “$C_{12}$” al multiplicar la segunda fila, pero por contexto corresponde a $C_{22}$.
- La escala de los modos no es única. Por ejemplo, $\begin{Bmatrix}1\\1.61803\end{Bmatrix}$ y $\begin{Bmatrix}0.61803\\1\end{Bmatrix}$ representan el mismo modo porque ambos apuntan en la misma dirección modal.
- Para sistemas reales con más grados de libertad se sigue la misma lógica, pero las matrices $\mathbf{M}$, $\mathbf{C}$ y $\mathbf{K}$ son de mayor tamaño.

---

## 17. Referencia

[1] Universidad de Costa Rica, “Sistema de 2 grados de libertad,” material de clase de Vibraciones Mecánicas, s. f.
