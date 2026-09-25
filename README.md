# Proyecto_2-MariaG_y_CarolR
## Descripción 
Este proyecto tiene como objetivo realizar el procesamiento, la limpieza y la estructuración del dataset de películas **TMDB 5000** utilizando **Python** y **Pandas** en Google Colab, garantizando un flujo de trabajo colaborativo, reproducible y sin dependencias innecesarias.


## 📌 Dataset Utilizado
https://www.kaggle.com/datasets/shivamb/netflix-shows

Al ser dos archivos obliga a hacer cruces de tablas (merge) basándose en el ID de la película para consolidar la información, lo cual es fundamental en ciencia de datos.


## 🛠️ Tecnologías y librerías:
Python (Google Colab)

Librerías: pandas

Control de versiones: git (repositorio), README.md


## Pasos ejecutados
### 1. Estructura - Limpieza Inicial
- [x] Montaje e integración con Google Drive (`/content/drive/MyDrive/proyecto_datos/`).
- [x] Unión de las tablas `tmdb_5000_movies.csv` y `tmdb_5000_credits.csv` mediante `merge()` por `id`.
- [x] Eliminación de columnas redundantes o con exceso de nulos (`homepage`, `tagline`, `status`, `movie_id`).
- [x] Conversión de la columna `release_date` a formato `datetime` y extracción de `release_year`.
- [x] Reemplazo de ceros en métricas financieras (`budget`, `revenue`, `runtime`) por valores nulos (`pd.NA`).
- [x] Exportación del archivo intermedio `tmdb_estructurado_parte1.csv`.
        
## Cómo ejecutar el notebook
1. Clonar el repositorio.
2. Subir los archivos `tmdb_5000_movies.csv` y `tmdb_5000_credits.csv` a la carpeta `proyecto_datos` en Google Drive.
3. Abrir y ejecutar las celdas en Google Colab siguiendo el orden de las partes 1 y 2.
 
## Resumen de decisiones de limpieza
* **Carol R (Parte 1):** Unión de datasets (`merge`), depuración estructural de columnas, conversión de formatos de fecha y tratamiento de datos numéricos/financieros.
* **María G (Parte 2):** Desempaquetado de estructuras JSON (`genres`, `keywords`, `cast`, `crew`) utilizando la librería estándar `json` de Python.
