# CULTURA-DIGITAL-Y-SOCIEDAD

# Netflix

## 1. Descripción del proyecto

Netflix Analytics es un proyecto de análisis de datos desarrollado en Python. Su objetivo es procesar información sobre eventos de visualización para obtener indicadores relacionados con los hábitos de consumo de contenido.

El programa permite limpiar los datos, calcular métricas de visualización, clasificar los planes de suscripción y generar reportes para facilitar el análisis.

## 2. Objetivos

- Limpiar y validar los registros de visualización.
- Eliminar registros con edad desconocida y usuarios menores de 18 años.
- Clasificar los planes de suscripción mediante un nivel numérico.
- Calcular la tasa de finalización de los contenidos.
- Identificar visualizaciones con una tasa de finalización igual o superior al 80%.
- Pseudonimizar los identificadores de usuario.
- Generar reportes en Excel, CSV y Parquet.

## 3. Tecnologías utilizadas

- Python 3
- Pandas
- NumPy
- Matplotlib
- Google Colab
- OpenPyXL
- PyArrow

## 4. Estructura del proyecto

```text
Netflix_Analytics/
│
├── data/
│   ├── raw/
│   │   └── eventos_visualizacion.jsonl
│   │
│   └── processed/
│       └── reporte.parquet
│
├── notebooks/
│   └── Colab_NETFLIX_corregido.ipynb
│
├── reports/
│   └── reporte_netflix.xlsx
│
├── README.md
└── requirements.txt
```

## 5. Instalación

Instalar las dependencias necesarias:

```bash
pip install pandas numpy matplotlib openpyxl pyarrow
```

## 6. Ejecución

1. Abrir el notebook en Google Colab.
2. Cargar el archivo `eventos_visualizacion.jsonl`.
3. Ejecutar las celdas en orden.
4. Revisar los resultados de limpieza y análisis.
5. Descargar los reportes generados.

## 7. Procesamiento de los datos

El programa realiza las siguientes operaciones:

1. Carga los eventos de visualización.
2. Comprueba que existan las columnas necesarias.
3. Elimina registros con edad nula.
4. Excluye usuarios menores de 18 años.
5. Asigna un nivel numérico a cada plan.
6. Calcula la tasa de finalización.
7. Identifica las visualizaciones con alta finalización, utilizando un umbral del 80%.
8. Pseudonimiza los identificadores de usuario.
9. Genera tablas, gráficos y archivos de salida.

**Nota:** cuando la duración del contenido es cero, la tasa de finalización se registra como un valor nulo (NaN), evitando errores de división.

## 8. Archivos generados

- **Excel:** contiene los registros procesados y un resumen de resultados.
- **CSV:** permite consultar los datos procesados en formato tabular.
- **Parquet:** almacena los datos procesados en un formato eficiente para análisis.

## 9. Validación y pruebas

Se realizan comprobaciones para verificar:

- Que no existan edades nulas después de la limpieza.
- Que todos los usuarios incluidos tengan 18 años o más.
- Que las tasas de finalización estén dentro del intervalo esperado de 0 a 100%.
- Que los registros con duración cero no provoquen errores.
- Que los planes tengan asignado el nivel correspondiente.
- Que los archivos de salida se generen correctamente.

## 10. Consideraciones

El umbral del 80% para identificar una visualización de alta finalización es un criterio definido para este análisis y puede modificarse según las necesidades del proyecto.

La transformación de los identificadores de usuario es una pseudonimización: sustituye los identificadores originales por códigos, pero no garantiza anonimización irreversible.

## 11. Autoría

Proyecto académico de análisis de datos desarrollado en Python.
