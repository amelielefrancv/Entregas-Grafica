# Ficha Técnica de la Base de Datos

## Fuente de los datos
Los datos utilizados vienen de los siguientes documentos: 

**[Música Chilena en Radios](https://www.scd.cl/difusion-de-la-musica/musica-chilena-en-radios/)**: Rankings mensuales de las 100 canciones más reproducidas en radios nacionales, publicados por la Sociedad Chilena del Derecho de Autor (SCD) desde el año 2016-2024.
**[Spotify Charts](https://charts.spotify.com/)**: Rankings semanales del Top 100 de canciones más escuchadas en Chile, disponibles a través de Spotify Charts con datos desde el 2016.

## Metodología de construcción de la base

Recolecté y descargue los rankings mensuales de las radios desde el sitio de la SCD para el período 2021-2024. Al descargar los datos en formato pdf por cada mes, luego los abrí en Excel con la opción de "Obtener Datos". Los datos despues fueron transcritos por el programa y organizados en una tabla. Luego copie y pegue estos datos a mi propia base de datos.

Para Spotify, descargue los rankings semanales desde 2020 a 2024. Para que calzara con los datos mensuales del SCD seleccione la última semana de cada mes para representar de forma mensual el comportamiento del streaming(Desde el ultimo lunes del mes). Los datos se descargaron en formato CSV lo cual tambien pase a Excel en "Obtener Datos". 

Ambos datos de artistas y titulos de canciones fueron copiados y pegados gracias a la herramienta de obtener datos de Excel. Tambien se utilizó la formula "=SECUENCIA(100,1,1,1) para escribir mas rapido los numeros del ranking. Finalmentes se agregaron manualmente los géneros musicales y nacionalidad de los artistas, usando fuentes como Wikipedia, Spotify y Google.

## Alcance de los datos

**Cobertura temporal**: 2021 a 2024 (4 años). 

**Cobertura geográfica**: Chile (ranking nacional en radios y Spotify Chile).

## Características de los datos
- Datos organizados de forma mensual y semanal.
- Están ordenados en dilas con columnas .especificas: fecha, artistas, genero, posición y nacionalidad.

- Existen datos cualitativos: Posiciones (1-100).
- Existen datos cualitativos: Artista, Canción, Genero,Nacionalidad.

## Variables incorporadas

- Fecha: Indica la fecha de la medición, mes por año para la radio y semana de mes por año para Spotify.

- Medio: Para diferenciar si los datos son de Radio o de Spotify.

- Posicióon: Lugar que ocupa en el ranking.

- Artista: Nombre del artista o banda interpretes de los temas.

- Canción: Titulo de la canción.

- Género: Género musical de las canciones.

- Nacionalidad: Nacionalidad del artista/banda.

## Otras observaciones

- La elección de los géneros musicales es subjetiva en algunos casos, debido a fusiones/mezcla de estilos en ciertas canciones.
- Algunas canciones aparecen en ambos rankings, pero no en las mismas fechas.


