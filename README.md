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


Pasos ejecutados
Estructura, Relaciones y Finanzas

    Conexión y Carga: compartir la carpeta creada para conectar Colab con Drive para no tener que subir los CSVs manualmente cada vez que abramos el proyecto. Montar Google Drive y leer los CSVs tmdb_5000_movies.csv y tmdb_5000_credits.csv .
    
    Merge de Tablas
      Ambos datasets comparten la columna llamada title, el parámetro axis indica la dirección (el eje) sobre el que se va a aplicar la operación, "Busca la etiqueta 'title' en las columnas (en vertical):(axis=1) y borra toda esa columna".
      Unir los datasets por id de película usando pd.merge().
  
  Eliminar "Basura" (Columnas innecesarias)
    Hay columnas que tienen demasiados nulos o que no aportan nada para un análisis estándar.
    
    Tratamiento de Fechas: Pandas lee las fechas como texto. Convertir release_date a datetime y extraer release_year.

    Limpieza Financiera (Ceros Encubiertos): Convertir los presupuestos (budget) e ingresos (revenue) con valor 0 a NaN para no distorsionar promedios.

    Exportación Intermedia: Guardar en Drive el archivo procesado tmdb_estructurado_parte1.csv.
    
    
  Cómo ejecutar el notebook, Resumen de decisiones de limpieza
