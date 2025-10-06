# Análisis de Datos para INN Hotels Group

## 1. Contexto y Problema Actual
INNHotelsGroup, una cadena hotelera con múltiples ubicaciones, ha identificado la necesidad de mejorar la gestión de sus reservas y reducir el número de cancelaciones. Si bien cuentan con una plataforma digital de reservas, enfrentan ciertos desafíos, como:

- Alta frecuencia de cancelaciones previas a la llegada.

- Baja visibilidad sobre los factores que influyen en la cancelación de reservas.

- Falta de segmentación clara del tipo de cliente.

- Dificultades para optimizar la ocupación hotelera en función de la anticipación de las reservas, los planes alimenticios o las necesidades específicas como el parking.

Mediante el análisis de los datos históricos de reservas, este proyecto busca identificar patrones clave que ayuden a comprender mejor el comportamiento de los huéspedes, anticipar cancelaciones y mejorar la eficiencia operativa.

## 2. Objetivo del Proyecto 

El objetivo principal de este análisis es desarrollar un dashboard interactivo que brinde una visión clara y actualizada sobre las reservas y los tipos de clientes, facilitando la toma de decisiones en distintas áreas como:

- Gestión de cancelaciones.

- Optimización de la ocupación según el tipo de habitación o el plan alimenticio.

- Análisis de tendencias de reservas por días de la semana y antelación.

- Segmentación de clientes según su comportamiento y preferencias.

Este dashboard estará acompañado de un informe explicativo con las principales conclusiones obtenidas y recomendaciones para la mejora del negocio.

## 3.Estructura del Repositorio
```bash
|------ data                  
  |---- INNHotelsGroup.csv   #Datos originales
  |---- INNHotelsGroup_modificación_datos_csv #Datos columna avg_price_per_room modificados cambio . por , 
  |---- Datos_Transformados.csv #Datos listos para analisis en formato csv
|------ Excels
  |---- Carga_datos_originales.xlsx #Datos originales en formato excel
  |---- Analisis_datos.xlsx # Preparación de datos para analisis.
  |---- Analisis_datos_listos.xlsx # Datos listos para analisis formato excel.
```

## 4. Descripción del Conjunto de Datos

El conjunto de datos utilizado para este proyecto contiene información sobre reservas realizadas en los hoteles del grupo INN Hotels Group. Las variables incluidas permiten analizar tanto el comportamiento del cliente como características específicas de cada reserva.

- **ID_reserva:**	Identificador único de la reserva.

- **Nº_adultos:**	Número de adultos incluidos en la reserva.
- **Nº_niños:**	Número de niños incluidos en la reserva.
- **Nº_total_de_viajeros:** Número total de personas que viajan (incluye adultos y niños).
- **Viaja_con_niños:** Indica si en el viaje se incluyen niños (Si, NO).
- **Nº_de_noches_fin_de_semana:**	Noches reservadas entre sabado y domingo.
- **Nº_de_noches_entre_semana:**	Noches reservadas entre lunes y viernes.
- **Nº_total_de_noches:** Noches reservadas en total, incluye días entre semana y fin de semana.
- **Plan_de_comida:**	Tipo de régimen de comidas contratado para el viaje (Desayuno, Media Pensión, Pensión Completa, No Seleccionado).
- **Plaza_de_parking:**	Indica si el huésped solicitó plaza de parking (Si, No).
- **Tipo_de_habitacion:**	Tipo de habitación reservada (Los valores estan codificados por INN Hotels)
- **Fecha_de_reserva:** Día en que el cliente realiza la reserva.
- **Fecha_de_llegada:** Día en que el cliente llega al Hotel de destino.
- **Fecha_de_salida:** Día en que el cliente se va del Hotel.
- **Antelacion_de_la_reserva:**	Número de días entre la fecha de reserva y la fecha de llegada.
- **Cliente_previsor:**	Muestra como de previsor es el cliente respecto a la reserva del viaje (Nada_previsor, Poco_previsor, Previsor, Bastante_previsor, Extremadamente_previsor).
- **Tipo_de_segmento_de_mercado:** Muestra a que segemento del mercado al que pertenece el cliente, según la reserva realizada.
- **Cliente_repite:** Indica si el cliente repite estancia (Si, NO).
- **Nº_de_cancelaciones_previas:** Número de cancelaciones previas realizadas por el cliente.
- **Nº_de_reservas_previas_no_canceladas:** Número de reservas previas realizadas por el cliente y no canceladas.
- **Fiabilidad_de_la_reserva:** Indica el grado de fiabilidad de la reserva realizada por el cliente (Baja, Media, Alta, Muy_Alta).
- **Precio_medio_por_habitación:** Precio medio por día de reserva, los precios de las habitaciones son dinamicos (expresados en euros).
- **Total_gastado:** Gasto total realizado durante la estancia (expresados en euros).
- **Precio_medio_por_persona:** Indica el gasto de cada persona durante la estancia (expresados en euros).
- **Nº_de_requerimientos_especiales:** Número de requerimientos especiales realizados por los clientes (planta alta, vistas desde la habitación, etc)
- **Cliente_exigente:** Muetra como de exigente es el cliente en relación a los requerimientos realizados (Nada, Poco, Bastante, Mucho).
- **Estado_de_la_reserva:** Muestra el estado de la reserva.

## 5. Recap Sesiones
### Sesión 1.
- Creación del respositorio.
- Generación de archivo Readme y gitignore.
- Creación del sistema de carpetas del repo.
- Añadir el conjunto de datos original 'INNHotelsGroup.csv'.
- Cambio . por , columna avg_price_per_room para poder trabjar con los datos 'INNHotelsGroup_modificación_datos.csv'.

### Sesión 2.
- Traducción de la Tabla de datos de Ingles a Español. 
- Creación de columnas complementarias para la realización del analisis.
- Creación del archivo en formato csv para mayor facilidad de trabajo en nuestra tabala de datos. (Datos_Transformados.csv)
- Creación de tabla excel con datos listos para el analisis, (Analisis_datos_listos.xlsx) 

## 6. Transformación y Limpieza de los Datos

Durante la etapa de limpieza se realizaron las siguientes tareas:

- Eliminación de valores nulos o imputación en columnas clave.

- Conversión de tipos de datos (por ejemplo, fechas, variables categóricas).

- Agrupación y simplificación de categorías poco frecuentes.

- Detección y tratamiento de outliers en variables como antelación o número de noches.

## 7. Análisis Descriptivo

El análisis descriptivo permitió identificar comportamientos interesantes:

- Los clientes con más de una cancelación previa tienen mayor probabilidad de volver a cancelar.

- Las reservas con menor antelación tienden a tener una menor tasa de cancelación.

- El día de llegada tiene un impacto en la duración de la estancia: las llegadas los viernes suelen tener más noches reservadas.

- El tipo de plan alimenticio y la solicitud de parking varían significativamente según el tipo de cliente.

## 8. Dashboard

Se ha desarrollado un dashboard interactivo utilizando herramientas como Power BI / Tableau / Looker Studio / Python + Plotly/Dash (especifica aquí la herramienta que hayas usado).

#### Este dashboard permite visualizar:

Distribución de reservas por tipo de cliente, habitación, y plan alimenticio.

Análisis de cancelaciones según antelación y número de noches.

Comparativas entre días de la semana y comportamiento del cliente.

Segmentación de clientes por historial de cancelaciones.

## 9. Informe del Análisis

El informe final del análisis se incluye:

- Introducción y contexto del proyecto.

- Metodología de análisis.

- Insights clave encontrados.

- Recomendaciones estratégicas para INN Hotels Group.

- Conclusiones generales y pasos sugeridos para acciones futuras.

## 10. Conclusiones
