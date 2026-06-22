# Determinación de la ecuación de estado de la energía oscura mediante el estudio de supernovas de tipo Ia

## Descripción

Este repositorio contiene el material desarrollado para mi Trabajo de Fin de Grado en Física, centrado en el estudio de la energía oscura a través de observaciones de supernovas de tipo Ia.

El objetivo principal es determinar si la expansión acelerada del universo puede describirse mediante una constante cosmológica (modelo ΛCDM) o si la energía oscura presenta un comportamiento dinámico caracterizado por una ecuación de estado distinta de \(w=-1\).

Para ello se utilizan datos observacionales procedentes de los catálogos SCP Union2.1 y Pantheon+SH0ES, comparando las predicciones teóricas con las medidas observadas del módulo de distancia y el redshift.

---

## Motivación

El descubrimiento de la expansión acelerada del universo a finales de los años 90 constituyó uno de los avances más importantes de la cosmología moderna. Actualmente, el modelo cosmológico estándar ΛCDM describe esta aceleración mediante una constante cosmológica, asociada a una ecuación de estado:

\[
w = \frac{P_{DE}}{\rho_{DE}} = -1
\]

Sin embargo, la naturaleza física de la energía oscura sigue siendo desconocida. Cualquier desviación significativa de este valor podría indicar la existencia de nueva física o de modelos dinámicos de energía oscura.

Las supernovas de tipo Ia son herramientas fundamentales para estudiar este problema, ya que actúan como velas estándar y permiten medir distancias cosmológicas con gran precisión.

---

## Objetivos

- Comprender el marco teórico de la cosmología moderna y el modelo ΛCDM.
- Estudiar la relación entre distancia de luminosidad y redshift.
- Analizar la sensibilidad de las observaciones de supernovas al parámetro \(w\).
- Determinar los valores más probables de \(\Omega_M\) y \(w\).
- Evaluar la compatibilidad de los datos con el modelo ΛCDM.
- Comparar distintos métodos estadísticos de análisis.

---

## Metodología

### Marco teórico

El trabajo desarrolla los conceptos fundamentales necesarios para describir la expansión del universo:

- Métrica FLRW.
- Ecuaciones de Friedmann.
- Evolución de las distintas componentes cosmológicas.
- Distancia comóvil.
- Distancia de luminosidad.
- Módulo de distancia.
- Energía oscura y parámetro de ecuación de estado.

### Datos observacionales

Se utilizan dos de los catálogos de supernovas más relevantes:

- SCP Union2.1
- Pantheon+SH0ES

### Análisis estadístico

La estimación de parámetros cosmológicos se realiza mediante minimización de la función χ².

#### χ² con errores diagonales

\[
\chi^2 = \sum_i \frac{(\mu_{obs,i}-\mu_{teo,i})^2}{\sigma_i^2}
\]

#### χ² con matriz de covarianza

\[
\chi^2 = \Delta \mu^T C^{-1} \Delta \mu
\]

Además, se calculan regiones de confianza correspondientes a 1σ, 2σ y 3σ para el espacio de parámetros \((\Omega_M,w)\).

---

## Implementación numérica

Todo el análisis ha sido desarrollado en **Wolfram Mathematica**.

Las principales tareas computacionales incluyen:

- Integración numérica de distancias cosmológicas.
- Cálculo de módulos de distancia teóricos.
- Minimización de la función χ².
- Tratamiento de matrices de covarianza.
- Generación de contour plots y regiones de confianza.
- Comparación entre distintos catálogos observacionales.

---

## Resultados principales

Los mejores ajustes obtenidos son:

| Catálogo | ΩM | w |
|-----------|-----------|-----------|
| Pantheon+ | 0.314 | -0.928 |
| SCP Union2.1 (errores diagonales) | 0.278 | -1.000 |
| SCP Union2.1 (covarianza completa) | 0.308 | -1.060 |

Los resultados obtenidos son compatibles con el modelo cosmológico estándar ΛCDM dentro del nivel de confianza de 1σ.

En conjunto, el análisis favorece un universo espacialmente plano dominado por una componente de energía oscura cuya ecuación de estado es consistente con:

\[
w=-1
\]

---

## Líneas futuras de trabajo

Las posibles extensiones de este proyecto incluyen:

- Implementación de la parametrización CPL:
  
\[
w(z)=w_0+w_a\frac{z}{1+z}
\]

- Análisis mediante cadenas de Markov Monte Carlo (MCMC).
- Combinación con datos de BAO y CMB.
- Estudio de modelos de gravedad modificada.
- Aplicación a futuros catálogos de Euclid y Vera C. Rubin.

---

