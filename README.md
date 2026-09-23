# Proyecto_2-MariaG_y_CarolR
Descripción del proyecto:
excelente punto de partida para cualquier flujo de trabajo de limpieza exploratoria de datos (EDA) en Jupyter Notebooks.


Dataset Utilizado
https://www.kaggle.com/datasets/shivamb/netflix-shows
Al ser dos archivos (movies.csv y credits.csv), obliga a hacer cruces de tablas (merge), lo cual es fundamental en ciencia de datos.

Demuestra verdadero dominio de Python: 
  Desempaquetar los diccionarios JSON (extraer al director o los géneros de una estructura de texto).

Manejo de "datos sucios" reales: Las películas con presupuesto cero o ingresos cero son trampas reales de la industria. Tendrán que decidir si imputan esos datos con la media, si usan modelos predictivos o si los descartan.
Desafíos de limpieza que encontrarán:

    Manejo de nulos (NaN): Las columnas director, cast y country tienen un alto porcentaje de valores faltantes reales que requerirán decisiones de imputación o eliminación (fillna o dropna).

    Extracción de texto (Regex/Split): La columna duration mezcla dos tipos de unidades: "minutos" para películas y "Seasons" para series. Tendrán que separar la base de datos o crear nuevas columnas numéricas extrayendo el texto.

    Limpieza de fechas: La columna date_added tiene espacios en blanco iniciales o finales y texto que debe limpiarse antes de poder usar pd.to_datetime().
Tecnologías y librerías:
 Python (Google Colab)
 Librerías: pandas
 Control de versiones: git (repositorio), README.md
