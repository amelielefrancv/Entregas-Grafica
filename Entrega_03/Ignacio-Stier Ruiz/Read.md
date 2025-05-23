Readme.md 
# Documentación del Proyecto de Visualización 

## Proceso
 Para esta visualización, se tuvo que arreglar la base de datos de la entrega 2 (muchas gracias profe la GOAT) y con eso quedo manualmente rellenar ciertas cosas y datos para que las bases esten completas. Luego de eso fueron directo a Google Colab para empezar a visualizar.

 Yo me encargue del lado de Spotify, donde a traves de la limpia manueal pude aclarar mucho más la página de lo que queríamos contar. Usando librerías de Panda y Altier, logre empezar a entender como funcionaba el proceso de visualización hasta poder llegar a una que me dejara conforme. 

Aun así siento que podemos hacer lecturas mucho más complejas y ricas en cuant a muestra de datos, me tiene muy emocionado para las estapas siguientes.


## Base de datos
Nuestra investigación se basa en dos fuentes principales de datos:

- Ranking mensual Top 100 de música chilena en radios, publicado por la Sociedad Chilena del Derecho de Autor (SCD), con registros disponibles desde 2016. Para este proyecto, acotamos el análisis al período comprendido entre 2020 y 2024.

- Ranking semanal Top 100 de Spotify Chile, disponible en Spotify Charts desde 2017. Para asegurar la comparabilidad entre ambas fuentes, también seleccionamos los años 2020 a 2024.

- Para procesar esta información, descargamos los archivos en formato PDF y CSV, los que posteriormente organizamos en Excel, seleccionando las columnas clave: Fecha, Medio, Año, Posición, Artista, Canción y Género. Como cada medio entrega 100 registros por mes, el total de datos procesados fue significativo. Finalmente, estructuramos la información en ocho archivos Excel: cuatro correspondientes a la radio (2021 a 2024) y cuatro a Spotify (2021 a 2024).

- Uno de los principales desafíos fue la categorización de los géneros musicales. Como grupo, decidimos agrupar los géneros específicos en categorías macro para facilitar el análisis y la visualización de los datos. Las categorías definidas fueron: Pop, Rock, Latino/Tropical, Folk/Indie, Electrónica, Urbano y Otros.

- Utilizamos esta información porque era la más actualizada y completa disponible, y nos permitía comparar de forma directa la radio y Spotify en Chile.

## Preguntas que responde la visualización
- ¿Como ha crecido el género urbano en porcentaje de escucha tanto en streaming como en radio desde 2021 hasta 2024?
- ¿Cual son los disintos géneros que esuchan los chilenos además del urbano?
- ¿ Que tanta diferencia existe entre el consumo de música urbana y el resto de géneros?
- ¿ Como varía e consumo de géneros musicales segun medio de consumición (radio o spotify)?

## Obsservaciones finales
Queda camino por recorrer claramente, el tema de como clasificar los generos fue un tema. Además que podemos aun mejorar la limpiza para dejar la base más pulcra, pero definitivamente vamos por buen camino.
