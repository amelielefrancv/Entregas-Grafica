# Nombre: grafico_cantidad_entradas_radio
# Descripción: Gráfico de burbujas que muestra cuántas veces aparece cada artista en los rankings radiales para cada año.

!pip install plotly

import pandas as pd
import plotly.express as px
from google.colab import files

radio = pd.read_csv('RADIOUNIFICADO.csv', sep=';')
print(radio.head())

entradas = radio.groupby(['Año', 'Artista']).size().reset_index(name='CantidadEntradas')

fig = px.scatter(
    entradas,
    x='Año',
    y='CantidadEntradas',
    size='CantidadEntradas',
    color='Artista',
    hover_name='Artista',
    title='Cantidad de entradas por artista en los rankings radiales por año',
    size_max=60
)

fig.update_layout(
    xaxis_title='Año',
    yaxis_title='Cantidad de entradas en el ranking',
    template='plotly_white'
)

fig.show()

html_filename = 'grafico_cantidad_entradas.html'
fig.write_html(html_filename)
files.download(html_filename)


# Nombre: grafico_canciones_distintas_radio
# Descripción: Gráfico de burbujas interactivo que indica cuántas canciones únicas tiene cada artista en los rankings radiales por año.

!pip install plotly

import pandas as pd
import plotly.express as px
from google.colab import files

radio = pd.read_csv('RADIOUNIFICADO.csv', sep=';')
print(radio.head())

canciones_unicas = radio.groupby(['Año', 'Artista'])['Canción'].nunique().reset_index(name='CantidadCanciones')

fig2 = px.scatter(
    canciones_unicas,
    x='Año',
    y='CantidadCanciones',
    size='CantidadCanciones',
    color='Artista',
    hover_name='Artista',
    title='Cantidad de canciones distintas por artista en rankings radiales por año',
    size_max=60
)

fig2.update_layout(
    xaxis_title='Año',
    yaxis_title='Cantidad de canciones distintas en el ranking',
    template='plotly_white'
)

fig2.show()

html_filename2 = 'grafico_canciones_distintas.html'
fig2.write_html(html_filename2)
files.download(html_filename2)


# Nombre: grafico_posicion_promedio_radio
# Descripción: Gráfico de líneas que muestra la posición promedio en el ranking radial de cada artista a lo largo de los años (mejor posición arriba).

!pip install plotly

import pandas as pd
import plotly.express as px
from google.colab import files

radio = pd.read_csv('RADIOUNIFICADO.csv', sep=';')
print(radio.head())

posicion_promedio = radio.groupby(['Año', 'Artista'])['Posición'].mean().reset_index()

fig3 = px.line(
    posicion_promedio,
    x='Año',
    y='Posición',
    color='Artista',
    markers=True,
    hover_name='Artista',
    title='Posición promedio por artista en los rankings radiales por año'
)

fig3.update_layout(
    yaxis_autorange='reversed',
    xaxis_title='Año',
    yaxis_title='Posición promedio en el ranking',
    template='plotly_white'
)

fig3.show()

html_filename3 = 'grafico_posicion_promedio.html'
fig3.write_html(html_filename3)
files.download(html_filename3)


# Nombre: grafico_cantidad_entradas_spotify
# Descripción: Gráfico de burbujas que refleja la cantidad de veces que cada artista aparece en rankings de Spotify por año.

!pip install plotly

import pandas as pd
import plotly.express as px
from google.colab import files

spotify = pd.read_csv('Spotify_UnidoListo.csv', sep=';')
print(spotify.head())

entradas_spotify = spotify.groupby(['Año', 'Artista']).size().reset_index(name='CantidadEntradas')

fig_spot_1 = px.scatter(
    entradas_spotify,
    x='Año',
    y='CantidadEntradas',
    size='CantidadEntradas',
    color='Artista',
    hover_name='Artista',
    title='Cantidad de entradas por artista en rankings de Spotify por año',
    size_max=60
)

fig_spot_1.update_layout(
    xaxis_title='Año',
    yaxis_title='Cantidad de entradas en el ranking',
    template='plotly_white'
)

fig_spot_1.show()

html_spot_1 = 'spotify_cantidad_entradas.html'
fig_spot_1.write_html(html_spot_1)
files.download(html_spot_1)


# Nombre: grafico_canciones_distintas_spotify
# Descripción: Gráfico de burbujas interactivo que muestra la cantidad de canciones únicas de cada artista en rankings de Spotify por año.

!pip install plotly

import pandas as pd
import plotly.express as px
from google.colab import files

spotify = pd.read_csv('Spotify_UnidoListo.csv', sep=';')
print(spotify.head())

canciones_unicas_spotify = spotify.groupby(['Año', 'Artista'])['Canción'].nunique().reset_index(name='CantidadCanciones')

fig_spot_2 = px.scatter(
    canciones_unicas_spotify,
    x='Año',
    y='CantidadCanciones',
    size='CantidadCanciones',
    color='Artista',
    hover_name='Artista',
    title='Cantidad de canciones distintas por artista en rankings de Spotify por año',
    size_max=60
)

fig_spot_2.update_layout(
    xaxis_title='Año',
    yaxis_title='Cantidad de canciones distintas en el ranking',
    template='plotly_white'
)

fig_spot_2.show()

html_spot_2 = 'spotify_canciones_distintas.html'
fig_spot_2.write_html(html_spot_2)
files.download(html_spot_2)


# Nombre: grafico_posicion_promedio_spotify
# Descripción: Gráfico de líneas que representa la posición promedio en el ranking de Spotify para cada artista a lo largo de los años (mejor posición arriba).

!pip install plotly

import pandas as pd
import plotly.express as px
from google.colab import files

spotify = pd.read_csv('Spotify_UnidoListo.csv', sep=';')
print(spotify.head())

posicion_promedio_spotify = spotify.groupby(['Año', 'Artista'])['Posición'].mean().reset_index()

fig_spot_3 = px.line(
    posicion_promedio_spotify,
    x='Año',
    y='Posición',
    color='Artista',
    markers=True,
    hover_name='Artista',
    title='Posición promedio por artista en rankings de Spotify por año'
)

fig_spot_3.update_layout(
    yaxis_autorange='reversed',
    xaxis_title='Año',
    yaxis_title='Posición promedio en el ranking',
    template='plotly_white'
)

fig_spot_3.show()

html_spot_3 = 'spotify_posicion_promedio.html'
fig_spot_3.write_html(html_spot_3)
files.download(html_spot_3)


# Nombre: grafico_generos_radio_vertical
# Descripción: Gráfico de barras apiladas que muestra la cantidad de entradas en rankings radiales agrupadas por género musical y año, con colores fijos para cada género.

!pip install plotly

import pandas as pd
import plotly.express as px
from google.colab import files

radio = pd.read_csv('RADIOUNIFICADO.csv', sep=';')
print(radio.head())

entradas_genero = radio.groupby(['Año', 'Género']).size().reset_index(name='CantidadEntradas')

colores_fijos = {
    'Pop': 'red',
    'Rock': 'blue',
    'Reggaetón': 'green',
    'Música urbana': 'purple',
    'Electrónica': 'orange',
    'Balada': 'pink',
    'Latina': 'brown',
    'Otro': 'gray'
}

fig = px.bar(
    entradas_genero,
    x='Año',
    y='CantidadEntradas',
    color='Género',
    color_discrete_map=colores_fijos,
    title='Cantidad de entradas por género en rankings radiales por año',
    labels={'CantidadEntradas': 'Cantidad de entradas en el ranking'}
)

fig.update_layout(
    barmode='stack',
    template='plotly_white'
)

fig.show()

html_filename = 'grafico_generos_radio.html'
fig.write_html(html_filename)
files.download(html_filename)


# Nombre: grafico_generos_radio_horizontal
# Descripción: Versión horizontal del gráfico anterior, visualizando la cantidad de entradas por género y año en rankings radiales con barras apiladas y colores fijos.

!pip install plotly

import pandas as pd
import plotly.express as px
from google.colab import files

radio = pd.read_csv('RADIOUNIFICADO.csv', sep=';')
print(radio.head())

entradas_genero = radio.groupby(['Año', 'Género']).size().reset_index(name='CantidadEntradas')

colores_fijos = {
    'Pop': 'red',
    'Rock': 'blue',
    'Reggaetón': 'green',
    'Música urbana': 'purple',
    'Electrónica': 'orange',
    'Balada': 'pink',
    'Latina': 'brown',
    'Otro': 'gray'
}

fig_horizontal = px.bar(
    entradas_genero,
    y='Año',
    x='CantidadEntradas',
    color='Género',
    orientation='h',
    color_discrete_map=colores_fijos,
    title='Cantidad de entradas por género en rankings radiales por año (horizontal)',
    labels={'CantidadEntradas': 'Cantidad de entradas en el ranking'}
)

fig_horizontal.update_layout(
    barmode='stack',
    template='plotly_white',
    yaxis_title='Año',
    xaxis_title='Cantidad de entradas'
)

fig_horizontal.show()

html_horizontal = 'grafico_generos_radio_horizontal.html'
fig_horizontal.write_html(html_horizontal)
files.download(html_horizontal)

# Este código analiza la diversidad musical en los rankings de radio y Spotify en Chile.

# =========================
# 1. CARGA DE BASES DE DATOS
# =========================

# Instalar plotly para crear visualizaciones interactivas
!pip install plotly

# Importar librerías necesarias
import pandas as pd
import plotly.express as px
import plotly.graph_objects as go
from google.colab import files

# Cargar base de datos de los rankings de radio
radio = pd.read_csv('RADIOUNIFICADO.csv', sep=';')

# Cargar base de datos de los rankings de Spotify
spotify = pd.read_csv('Spotify_UnidoListo.csv', sep=';')

# =========================
# 2. NORMALIZACIÓN DE GÉNEROS
# =========================

# Crear diccionario para agrupar géneros similares bajo categorías comunes
normalizacion_generos = {
    'Urbano': 'Música urbana',
    'Urban': 'Música urbana',
    'Pop urbano': 'Música urbana',
    'Folk': 'Folk/Indie',
    'Indie': 'Folk/Indie',
    'Latina': 'Latino/Tropical',
    'Tropical': 'Latino/Tropical',
}

# Aplicar normalización de géneros a la base de radio
radio['Género_normalizado'] = radio['Género'].replace(normalizacion_generos)

# Aplicar normalización de géneros a la base de Spotify
spotify['Género_normalizado'] = spotify['Género'].replace(normalizacion_generos)

# =========================
# 3. VISUALIZACIÓN ENTRADAS RADIO
# =========================

# Agrupar y contar entradas por año y género en la radio
radio_grouped = radio.groupby(['Año', 'Género_normalizado']).size().reset_index(name='Entradas')

# Crear gráfico de barras apiladas para la radio por género y año
fig_radio = px.bar(radio_grouped, x='Año', y='Entradas', color='Género_normalizado',
                   title='Entradas por Género en la Radio (2019-2024)',
                   labels={'Entradas': 'Cantidad de Entradas', 'Año': 'Año', 'Género_normalizado': 'Género'})

# Mostrar el gráfico
fig_radio.show()

# =========================
# 4. VISUALIZACIÓN ENTRADAS SPOTIFY
# =========================

# Agrupar y contar entradas por año y género en Spotify
spotify_grouped = spotify.groupby(['Año', 'Género_normalizado']).size().reset_index(name='Entradas')

# Crear gráfico de barras apiladas para Spotify por género y año
fig_spotify = px.bar(spotify_grouped, x='Año', y='Entradas', color='Género_normalizado',
                     title='Entradas por Género en Spotify (2019-2024)',
                     labels={'Entradas': 'Cantidad de Entradas', 'Año': 'Año', 'Género_normalizado': 'Género'})

# Mostrar el gráfico
fig_spotify.show()

# =========================
# 5. VISUALIZACIÓN PARTICIPACIÓN ARTISTAS CHILENOS RADIO
# =========================

# Calcular porcentaje de artistas chilenos y extranjeros por año en la radio
radio_participacion = radio.groupby(['Año', 'Nacionalidad']).size().reset_index(name='Entradas')
radio_totales = radio_participacion.groupby('Año')['Entradas'].transform('sum')
radio_participacion['Porcentaje'] = radio_participacion['Entradas'] / radio_totales * 100

# Crear gráfico de áreas apiladas para la radio
fig_radio_part = px.area(radio_participacion, x='Año', y='Porcentaje', color='Nacionalidad',
                         title='Participación de Artistas Chilenos y Extranjeros en la Radio (2019-2024)',
                         labels={'Porcentaje': 'Porcentaje de Entradas', 'Año': 'Año', 'Nacionalidad': 'Nacionalidad'})

# Mostrar el gráfico
fig_radio_part.show()

# =========================
# 6. VISUALIZACIÓN PARTICIPACIÓN ARTISTAS CHILENOS SPOTIFY
# =========================

# Calcular porcentaje de artistas chilenos y extranjeros por año en Spotify
spotify_participacion = spotify.groupby(['Año', 'Nacionalidad']).size().reset_index(name='Entradas')
spotify_totales = spotify_participacion.groupby('Año')['Entradas'].transform('sum')
spotify_participacion['Porcentaje'] = spotify_participacion['Entradas'] / spotify_totales * 100

# Crear gráfico de áreas apiladas para Spotify
fig_spotify_part = px.area(spotify_participacion, x='Año', y='Porcentaje', color='Nacionalidad',
                           title='Participación de Artistas Chilenos y Extranjeros en Spotify (2019-2024)',
                           labels={'Porcentaje': 'Porcentaje de Entradas', 'Año': 'Año', 'Nacionalidad': 'Nacionalidad'})

# Mostrar el gráfico
fig_spotify_part.show()

# =========================
# 7. VISUALIZACIÓN TOP 10 ARTISTAS RADIO
# =========================

# Identificar los 10 artistas con más entradas en la radio
top_artistas_radio = radio['Artista'].value_counts().nlargest(10).reset_index()
top_artistas_radio.columns = ['Artista', 'Entradas']

# Crear gráfico de barras para el top 10 de la radio
fig_top_radio = px.bar(top_artistas_radio, x='Artista', y='Entradas', color='Artista',
                       title='Top 10 Artistas con Más Entradas en la Radio',
                       labels={'Entradas': 'Cantidad de Entradas', 'Artista': 'Artista'})

# Mostrar el gráfico
fig_top_radio.show()

# =========================
# 8. VISUALIZACIÓN TOP 10 ARTISTAS SPOTIFY
# =========================

# Identificar los 10 artistas con más entradas en Spotify
top_artistas_spotify = spotify['Artista'].value_counts().nlargest(10).reset_index()
top_artistas_spotify.columns = ['Artista', 'Entradas']

# Crear gráfico de barras para el top 10 de Spotify
fig_top_spotify = px.bar(top_artistas_spotify, x='Artista', y='Entradas', color='Artista',
                         title='Top 10 Artistas con Más Entradas en Spotify',
                         labels={'Entradas': 'Cantidad de Entradas', 'Artista': 'Artista'})

# Mostrar el gráfico
fig_top_spotify.show()
