# Documentación de limpieza de datos

## 1. Proceso de limpieza de datos

El proceso de limpieza de datos se realizó con el objetivo de obtener comparaciones entre las canciones mas populares que se registran en los rankings de la radio en Chile y en Spotify Chile, de manera que identifiquemos que medio es mas diverso y cual es el mas homogeneo.

### Paso 1: Revisión de los archivos originales

Primero revisé y descargué  los archivos de las fuentes oficiales (SCD y Spotify Charts). Algunos estaban en formato PDF o CSV, por lo cual transforme estos documentos por la herramienta de Excel "Obtener Datos" para que dejara los datos estructurados. Al tenerlos mas ordenados pude trabajar mejor con ellos para copiar y pegar en las columnas de mi base de datos oficial. En este paso, tuve que tomar la decisión de solo considerar los años 2021 a 2024 ya que los datos del SCD solo comenzaron a incluir un ranking de canciones nacionales y internacionales mezcladas en sus reportes el 2021. Hice esto para que las bases del SCD y Spotify Charts fueron un poco mas parejas en el analisis. 

### Paso 2: Creación de columnas

A ambas bases (Radio y Spotify) les puse las mismas columnas ya que quiero que se rigan por los mismos criterios poder identificar las diferencias entre ellas.

Columnas:
- Fecha  
- Medio (Radio o Spotify)  
- Posición (ranking del 1 al 100)  
- Artista  
- Canción  
- Género  
- Nacionalidad  

### Paso 3: Traspaso de texto

Para hacer mas rapido el traspaso de texto, en el caso de los nombres de los artistas y titulos lo copie y pegue de los datos transformados. Asimismo los datos de Fecha y Medio lo escribi una vez y luego lo iba multiplicando en el Excel. Para la columna de posición utilice la formula "=SECUENCIA(100,1,1,1)" para no tener que hacerlo uno por uno. Al crear la base de datos me di cuenta de que podia mezclar los titulos de las canciones y sus respectivos artistas sin que cambiara mucho el resultado del analisis, por tanto para lo ultimos año hice esto, ademas para no poder tanto tiempo dividiendolos uno por uno. 

### Paso 4: Completar datos faltantes

En algunos casos, faltaba la nacionalidad o el género musical. Busque esta información en fuentes como Wikipedia, Spotify o Google y la rellene en las columnas correspondientes.


### Herramientas utilizadas:

- Microsoft Excel (para revisar, transformar y editar los datos manualmente)
- Google/Wikipedia (para comprobar ciertos datos como genero o nacionalidad)
- ChatGPT (para ayuda en copiar y pegar datos en celdas de excel que se pegaban mal)

## 2. Fuentes de datos utilizadas

- **[Música Chilena en Radios](https://www.scd.cl/difusion-de-la-musica/musica-chilena-en-radios/)**: Rankings mensuales de las 100 canciones más reproducidas en radios nacionales, publicados por la Sociedad Chilena del Derecho de Autor (SCD) desde 2016. Esta fuente es muy importante para nuestra investigación ya que nos presenta de manera clara y ordenada los rankings por mes y año en un mismo lugar.

- **[Spotify Charts](https://charts.spotify.com/)**: Rankings semanales del Top 100 de canciones más escuchadas en Chile. Elegimos esta fuente para poder hacer el contraste con los datos de la radio en Chile, al igual que los datos del SCD estos estan muy bien ordenados. La cantidad de información disponible es crucial para armar nuestra propia base de datos. 

## 3. Preguntas que se pueden responder con la base limpia

1. **¿Qué géneros aparecen más en el ranking de radios y cuáles en el de Spotify?**  
2. **¿Qué porcentaje de canciones del top 100 de Spotify corresponde a música urbana?**  
3. **¿Qué artistas o géneros aparecen frecuentemente en la radio pero no en Spotify, y viceversa?**  
4. **¿En el ranking de Spotify se escuchan mas chilenos o extranjeros?**  
5. **¿En los 5 años de analisis ha aumentado o disminuido la diversidad musical (géneros) en cada medio?**  