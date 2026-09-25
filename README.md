# Proyecto_2-MariaG_y_CarolR
## Descripción del proyecto:
excelente punto de partida para demostrar habilidades avanzadas de limpieza exploratoria de datos (EDA) en Python mediante la librería pandas.


## Dataset Utilizado
https://www.kaggle.com/datasets/shivamb/netflix-shows

Al ser dos archivos obliga a hacer cruces de tablas (merge) basándose en el ID de la película para consolidar la información, lo cual es fundamental en ciencia de datos.
Desempaquetar los diccionarios JSON.
"Datos sucios" reales: películas con presupuesto cero o ingresos cero son trampas reales de la industria. 
Nulos (NaN): un alto porcentaje de valores faltantes reales que requerirán dropna.
Limpieza de fechas: columna date_added tiene espacios en blanco iniciales o finales y texto que debe limpiarse antes de poder usar pd.to_datetime().


## Tecnologías y librerías:
Python (Google Colab)

Librerías: pandas

Control de versiones: git (repositorio), README.md


## Pasos ejecutados
Compartir con permisos de Editor la carpeta de Google Drive proyecto_datos, seleccionar "Añadir acceso directo a Drive", subir ahí los CSVs (tmdb_5000_movies.csv y tmdb_5000_credits.csv) iniciales y guardarlo directamente dentro de "Mi unidad".
Leemos ambos datasets, al importar la librería pandas, que comparten columna y la borra.
Unir los datasets por id de película usando pd.merge().
Eliminamos: películas con el parámetro subset para que revise la columna que no tenga fecha de estreno, demasiados nulos...    
Pandas lee las fechas como texto, ajustamos. 
Convertir los presupuestos (budget), ingresos (revenue) y duración (runtime) con valor 0 para no distorsionar promedios.
Exportamos el archivo procesado tmdb_estructurado_parte1.csv.
    
    
  Cómo ejecutar el notebook, Resumen de decisiones de limpieza
