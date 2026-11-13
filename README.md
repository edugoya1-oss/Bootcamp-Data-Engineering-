
# Bootcamp de Ingeniería de Datos

Repositorio de ejercicios y proyectos prácticos
desarrollados durante mi formación en Ingeniería
de Datos, utilizando Databricks, SQL y GitHub.

## Tecnologías

- Databricks SQL
- Unity Catalog
- Git y GitHub
- SQL avanzado: CTEs y Window Functions
- Análisis Exploratorio de Datos (EDA)

## Semana 2 — SQL avanzado y EDA

### 1. Práctica de SQL avanzado

Notebook: `01_CTEs_Window_Functions.ipynb`

Ejercicios de consultas SQL, CTEs, funciones
de ventana, rankings y análisis comparativos
sobre el dataset de taxis de Nueva York.

### 2. EDA de propiedades inmobiliarias

Notebook: `02_EDA_Propiedades.ipynb`

Análisis exploratorio de 1.246.131 registros
inmobiliarios almacenados en una tabla Bronze.

Se realizaron:
- Exploración inicial y revisión de tipos de datos.
- Análisis de valores nulos.
- Distribuciones de variables categóricas.
- Estadísticas descriptivas.
- Detección de posibles duplicados y outliers.
- Comparaciones mediante funciones de ventana.


## Principales hallazgos

El análisis exploratorio se realizó sobre
1.246.131 registros inmobiliarios.

### Distribución de propiedades

- Alquiler: 50,28 %.
- Venta: 48,42 %.
- Alquiler temporal: 1,17 %.

### Calidad de datos

- Orientación cardinal: 92,50 % de valores nulos.
- Antigüedad: 99,36 % de registros con valor 999,
  identificado como posible placeholder.
- Precios inválidos: 0,59 %.
- Superficies totales inválidas: 3,98 %.
- 134.227 registros adicionales en grupos
  potencialmente duplicados según precio y URL.

### Evaluación general de calidad

Según los controles definidos en el proyecto:

| Indicador | Resultado |
|---|---:|
| Registros válidos | 7.567 (0,61 %) |
| Registros inválidos | 1.238.564 (99,39 %) |

**Importante:** El elevado porcentaje de
registros clasificados como inválidos está
fuertemente relacionado con el valor 999
en la columna antiguedad.

Esto no significa que el 99,39 % de los registros
deba eliminarse, ya que muchas propiedades
pueden conservar información útil en otras variables.


## Próximos pasos

Diseñar una capa Silver con reglas de conversión
de tipos, estandarización, tratamiento de valores
faltantes y validación de posibles duplicados.
