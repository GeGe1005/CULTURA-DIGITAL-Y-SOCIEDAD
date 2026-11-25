# CULTURA-DIGITAL-Y-SOCIEDAD

# Netflix 

## Objetivo
Procesar eventos de visualización para analizar consumo de contenidos, planes y tasa de finalización.

## Requisitos
Python 3.10 o superior. Dependencias: pandas, numpy, matplotlib, openpyxl, pyarrow y pytest.

## Instalación
```bash
pip install -r requirements.txt
```

## Ejecución
Abrir `Colab_NETFLIX_corregido.ipynb` en Google Colab, ejecutar las celdas en orden y subir el archivo JSONL/TXT de eventos.

## Estructura propuesta
- `data/raw/`: datos de entrada.
- `data/processed/`: resultados procesados.
- `src/`: carga, limpieza, métricas y visualización.
- `tests/`: pruebas automatizadas.
- `README.md`: documentación del proyecto.

## Reglas de procesamiento
- Se excluyen registros con campos obligatorios nulos.
- Se conservan usuarios de 18 años o más.
- Los eventos con duración cero se conservan; su tasa queda como NaN.
- La alta finalización se define como una tasa >= 80%.
- Los identificadores se reemplazan por códigos enteros locales.

## Salidas
- `reporte_netflix.xlsx`: hojas Registros y Resumen.
- `reporte_netflix.parquet`: registros procesados.
- `resumen_netflix.csv`: resumen por título.
