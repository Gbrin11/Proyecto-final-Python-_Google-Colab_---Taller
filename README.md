# Análisis Global de casos de Tuberculosis con Python (Google Colab)

## Descripción del proyecto
Este proyecto consiste en el análisis, transformación, limpieza y exploración de una base de datos internacional sobre casos de tuberculosis, utilizando Python en Google Colab.

El propósito principal fue comprender la situación global de la tuberculosis mediante el procesamiento de datos provenientes de los conjuntos de datos **who** y **population**, para posteriormente analizar patrones, tasas de incidencia y distribución regional de la enfermedad entre los años 1995 y 2013.

A través de técnicas de carga de datos, manipulación estructurada y análisis exploratorio, se logró transformar datos complejos en información interpretable para evaluar el impacto de esta enfermedad a nivel mundial.

---

## Objetivos del proyecto

### Objetivo general
Analizar la incidencia global de tuberculosis mediante el procesamiento y exploración de bases de datos internacionales utilizando Python.

### Objetivos específicos
- Comprender la estructura del conjunto de datos.
- Limpiar, depurar y corregir inconsistencias en los datos.
- Transformar variables para facilitar su análisis.
- Clasificar casos por género, método de diagnóstico y grupo etario.
- Integrar datos poblacionales para calcular tasas de incidencia.
- Explorar patrones de afectación mundial.
- Visualizar la evolución de la tuberculosis mediante gráficas.

---

## Herramientas utilizadas
- Python
- Google Colab
- Google Drive
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly Express

---

## Conjuntos de datos utilizados
### Dataset principal:
- **who.csv**
  - Casos reportados de tuberculosis por país, año, sexo, método y grupo de edad.

### Dataset complementario:
- **population.csv**
  - Datos de población por país y año.

---

## Metodología del proceso

### 1. Revisión de documos
Se revisó la documentación técnica de las bases de datos:
- `who`
- `population`

Con el fin de comprender:
- Variables
- Estructura
- Códigos
- Clasificaciones

---

### 2. Preparación del entorno de trabajo
- Creación de carpeta en Google Drive
- Carga de archivos CSV
- Vinculación de Google Colab con Google Drive
- Importación de librerías necesarias

---

### 3. Carga inicial de datos
Se importaron ambos conjuntos de datos en Google Colab y se realizó una inspección preliminar mediante:

`head()`

Esto permitió visualizar las primeras filas y verificar la estructura de las tablas.

---

### 4. Investigación documental
Se realizó una investigación complementaria sobre:
- Tuberculosis
- Métodos diagnósticos

---

### 5. Limpieza y depuración de datos

#### Actividades realizadas:
- Identificación de valores nulos
- Detección de inconsistencias
- Corrección de errores de interpretación de datos

### Caso relevante:
Se detectó que:
- La categoría `NA` fue interpretada como valor nulo
- En realidad correspondía al código ISO2 de Namibia

### Solución:
Se utilizó:

`.loc[]`

Para corregir la asignación.

---

### 6. Tratamiento de valores faltantes
- Los campos de casos faltantes fueron reemplazados por valores de cero para garantizar integridad analítica.

---

### 7. Transformación estructural de datos
Se aplicó:

`melt()`

Para convertir columnas en filas y facilitar el análisis.

---

### 8. Integración de variables
Se añadieron nuevas columnas:

#### Género:
- Masculino
- Femenino

#### Método de diagnóstico:
- Relapse
- Negative pulmonary smear
- Positive pulmonary smear
- Extrapulmonary

#### Grupo de edad:
- 0–14
- 15–24
- 25–34
- 35–44
- 45–54
- 55–64
- 65+

---

### 9. Integración poblacional
Se realizó un merge entre:
- Casos de tuberculosis
- Población total

Esto permitió incorporar la variable:
- `population`

---

### 10. Exportación de base final
La tabla limpia y estructurada fue guardada como:

- tuberculosis.csv

---

## Exploración y análisis de datos

### Se realizaron agrupaciones por:
- Género
- Método diagnóstico
- Grupo etario
- País
- Año

---

### Principales hallazgos:
- **217 países afectados**
- Periodo analizado:
  - Inicio: 1995
  - Finalización: 2013

---

## Cálculo de tasa de incidencia

### Fórmula utilizada:
**Tasa de incidencia por cada 100,000 habitantes**

`100,000 * casos nuevos / población`

Esto permitió evaluar:
- Magnitud del problema
- Evolución temporal
- Comparabilidad internacional

---

## Visualización de resultados
Se desarrollaron gráficas utilizando:
- Matplotlib
- Seaborn
- Plotly

### Visualización principal:
- Tasa de incidencia anual global de tuberculosis
