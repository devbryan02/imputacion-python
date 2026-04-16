# Análisis e Imputación de Datos Faltantes

Este proyecto realiza un análisis exploratorio de datos (EDA) sobre un dataset de accidentes, enfocándose en la detección, análisis e imputación de valores nulos.

---

## Dataset

El dataset contiene 500 registros relacionados con accidentes, incluyendo variables como:

- `heridos`
- `fallecidos`
- `daños_materiales_usd`

Se identificó que estas columnas presentan aproximadamente un **25% de valores nulos**.

---

## Tecnologías utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Missingno

---

## Proceso realizado

### 1. Carga de datos
Se cargó el dataset desde un archivo `.csv` utilizando Pandas.

### 2. Análisis inicial
- Uso de `.info()` para estructura del dataset
- Uso de `.describe()` para estadísticas descriptivas

### 3. Detección de valores nulos
- `.isna().sum()` → cantidad de nulos  
- `.isna().mean() * 100` → porcentaje de nulos  

### 4. Visualización
- Gráfica de barras con Seaborn
- Visualización estructural con Missingno

### 5. Análisis de datos
- Se verificó que los valores faltantes son independientes  
- Se observó que las variables presentan distribuciones estables  
- No se detectaron outliers significativos  

---

## Imputación de datos

Se aplicó imputación mediante la **mediana** en las columnas:

- `heridos`
- `fallecidos`
- `daños_materiales_usd`

### Justificación
- La mediana representa adecuadamente el valor central  
- Es robusta frente a posibles valores extremos  
- Permite mantener la integridad del dataset sin eliminar información  

---

## Resultados

- Se eliminaron todos los valores nulos en las columnas analizadas  
- Se preservó el 100% de los registros originales  
- El dataset quedó listo para análisis o modelado posterior  

---

## Conclusión

La imputación por mediana resultó adecuada debido a la naturaleza de los datos y la distribución observada.  
Este enfoque permitió manejar los valores faltantes de forma efectiva sin introducir sesgos significativos.

---