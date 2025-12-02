# Análisis Dinámico y Estadístico del Modelo SEIQR - COVID-19 (Argentina)

## Descripción del Proyecto
Este repositorio contiene el código fuente y los scripts de análisis estadístico para el estudio de la dinámica de propagación del COVID-19 en Argentina, basado en el modelo compartimental **SEIQR** (Susceptible-Exposed-Infected-Quarantined-Recovered).

El enfoque principal se centra en la validación y estimación de parámetros críticos, referenciados en este estudio como variables de interés (incluyendo las series `a` y `rui`), siguiendo los lineamientos teóricos presentados por **Nadia Barreiro et al.**

## Estructura del Repositorio
* `main_analysis.py`: Script principal de ejecución de tests estadísticos (Test de Normalidad, QQ-Plots, Histogramas).
* `data/`: Directorio para almacenar los arrays de datos (no incluido por privacidad, ver sección de uso).
* `requirements.txt`: Dependencias necesarias.

## Metodología Matemática
El estudio utiliza un enfoque de **Sistemas Dinámicos** y **Estadística Inferencial** para evaluar la robustez de los parámetros del modelo. Se aplican las siguientes técnicas:

1.  **Tests de Bondad de Ajuste:**
    * Shapiro-Wilk (para $n < 50$).
    * Kolmogorov-Smirnov / Lilliefors (para $n > 50$).
2.  **Análisis Gráfico:**
    * Histogramas de frecuencia con estimación de densidad (KDE).
    * Gráficos Q-Q (Quantile-Quantile) para evaluación de normalidad.
    * Boxplots para detección de outliers.

## Requisitos
El código fue desarrollado en Python 3.8+. Las dependencias principales son `numpy`, `scipy` y `matplotlib`.

## Uso
Para ejecutar el análisis de distribución sobre los parámetros obtenidos:

```bash
pip install -r requirements.txt
python main_analysis.py

Barreiro, N., et al. (2020). Modelling the COVID-19 epidemic in Argentina.
