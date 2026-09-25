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
Ambos datasets comparten la columna llamada title, el parámetro axis indica la dirección (el eje) sobre el que se va a aplicar la operación, "Busca la etiqueta 'title' en las columnas (en vertical):(axis=1) y borra toda esa columna".
Unir los datasets por id de película usando pd.merge().
  
  Eliminar "Basura" (Columnas innecesarias)
    Hay columnas que tienen demasiados nulos o que no aportan nada para un análisis estándar.
    
    Tratamiento de Fechas: Pandas lee las fechas como texto. Convertir release_date a datetime y extraer release_year.

    Limpieza Financiera (Ceros Encubiertos): Convertir los presupuestos (budget) e ingresos (revenue) con valor 0 a NaN para no distorsionar promedios.

    Exportación Intermedia: Guardar en Drive el archivo procesado tmdb_estructurado_parte1.csv.
    
    
  Cómo ejecutar el notebook, Resumen de decisiones de limpieza
