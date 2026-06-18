# Predicción del éxito comercial y la rentabilidad del cine

Este repositorio contiene el desarrollo del Trabajo Fin de Grado de Business Analytics:

**¿Qué hace que una película sea rentable? Predicción del éxito comercial y la rentabilidad del cine a partir de sus características de producción**

El objetivo del proyecto es analizar qué factores conocidos antes del estreno de una película permiten anticipar su resultado económico, y construir modelos capaces de predecir tanto su éxito comercial como su rentabilidad.

## Descripción del proyecto

La industria cinematográfica mueve grandes cantidades de dinero, pero el éxito de una película sigue siendo difícil de anticipar. Una producción puede recaudar mucho y aun así no ser rentable si su presupuesto fue demasiado alto, mientras que una película de bajo coste puede obtener un retorno muy elevado.

Por este motivo, el proyecto no se centra únicamente en la recaudación bruta, sino en el **retorno sobre la inversión (ROI)**, que permite medir la rentabilidad real de una película comparando sus ingresos con su presupuesto.

El trabajo sigue el ciclo completo de un proyecto de análisis de datos:

1. Ingeniería del dato.
2. Análisis del dato.
3. Análisis de negocio.

## Objetivos

Los principales objetivos del trabajo son:

- Construir una base de datos depurada a partir de fuentes públicas de información cinematográfica.
- Tratar valores ausentes, especialmente en presupuesto y recaudación.
- Crear variables derivadas como ROI, beneficio, rentabilidad, año, década, mes de estreno y géneros.
- Realizar un análisis exploratorio de las películas y su rentabilidad.
- Entrenar y comparar modelos de machine learning para predecir:
  - Si una película será rentable.
  - Cuál puede ser su recaudación.
- Identificar las variables más relevantes en el resultado económico de una película.
- Traducir los resultados en recomendaciones útiles para una productora.

## Datos utilizados

El proyecto parte de datos cinematográficos procedentes de fuentes públicas como TMDB e IMDb.

El dataset principal contiene información sobre películas, incluyendo variables como:

- Presupuesto.
- Recaudación.
- Género.
- Duración.
- Idioma original.
- Fecha de estreno.
- Popularidad.
- Valoración del público.
- Número de votos.
- Productoras.

Tras el proceso de limpieza, el conjunto final utilizado para el análisis contiene aproximadamente **3.210 películas** con datos económicos fiables.

## Metodología

### 1. Ingeniería del dato

En esta fase se preparan los datos para el análisis posterior. Las principales tareas realizadas son:

- Carga del dataset original.
- Diagnóstico de valores nulos y valores erróneos.
- Tratamiento de presupuestos y recaudaciones ausentes.
- Filtrado de películas sin información económica fiable.
- Imputación de duraciones ausentes mediante la mediana.
- Eliminación de columnas no relevantes.
- Transformación de fechas.
- Creación de variables derivadas.
- Generación de visualizaciones exploratorias.
- Almacenamiento del dataset depurado.

La variable central creada en esta fase es el **ROI**, calculado como:

```text
ROI = revenue / budget
