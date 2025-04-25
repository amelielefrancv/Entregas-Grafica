# Ficha Técnica de la Base de Datos

## Fuente de los datos
Los datos utilizados vienen de los siguientes documentos: 

**[Música Chilena en Radios](https://www.scd.cl/difusion-de-la-musica/musica-chilena-en-radios/)**: es un sitio de Rankings donde las 100 canciones más reproducidas en radios nacionales son listadas y publicados por la Sociedad Chilena del Derecho de Autor (SCD) desde el año 2016. Conteniendo emisoras de todo el país y contabilizando al porcentaje de música chilena que suena mes a mes
**[Spotify Charts](https://charts.spotify.com/)**: Rankings semanales del Top 100 de canciones más escuchadas de manera semanal en Chile y el mundo disponibles a través de Spotify Charts con datos desde el 2016 que fue cuando llegó al país.

## Metodología de construcción de la base

La recolección de los datos fue muy particular para cada caso y se utilizaron distintos mecanismos. 
Para las estadísticas del SCD, como venían todas las cifras en formato PDF, usé la herramienta interna de excel para poder leer los datos y traducirlos a un formato en cual pudiera trabajar y poder armar la base de datos. Mientras que todos las cífras de Spotify ya venían en el formato solicitado, por ende, lo único que tuve que hacer fue agrupar esta inmensidad de números de los oyentes semanales a tarves de otra de las herramientas internas de excel como ens Power Query.

Spotify maneja sus datos en tiempo de semana, por ende, para poder equipararlo con la medicion de SCD, se consideró solo las 100 canciones más esuchadas de la primera semana de cada me

Al tener los datos en un formato comodo, me dediqué a recopilar los datos de reproducciones, artístas, género y nacionalidad de los artistas que suenan tanto en radio como Spotify, para finalmente tener una comparativa directa sobre que es lo que suena en el país a nivel radial y como se diferencia con el sistema más democrático y popular de los servicios de streaming. 

## Alcance de los datos

**Cobertura temporal**: 2021 a 2024 (4 años). 

**Cobertura geográfica**: Todo Chile en general (ranking de radios nacionales y Spotify Chile).

## Características de los datos
- Datos organizados de forma mensual dividido en un año calendario.
- Están ordenados en distintas con columnas .especificas: fecha de escucha, nombre de la cancion y el artísta que la canta, Cantidad neta de reproducciones, género y país de origen del artista princiapl

- Existen datos cualitativos: Posiciones1 del 1 al 100.
- Existen datos cualitativos: Artista, Canción, Genero,Nacionalidad.

## Variables incorporadas

- Canción: Titulo de la canción.

- Nacionalidad: Nacionalidad del artista principal.

- Fecha: Indica la fecha de la medición, mes por año para la radio y semana de mes por año para Spotify.

- Posición: Que lugar tiene segun popularidad. 

- Género: Género musical de las canciones.

## Otras observaciones

- Algunas canciones aparecen en ambos rankings, pero no en las mismas fechas.
- Se estableció la primera semana de cada mes para medir los datos de spotify ( los cuales son semanales)
