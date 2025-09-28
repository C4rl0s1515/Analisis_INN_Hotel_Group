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
|------ Excels
```

## 4. Descripción del Conjunto de Datos

El conjunto de datos utilizado para este proyecto contiene información sobre reservas realizadas en los hoteles del grupo INN Hotels Group. Las variables incluidas permiten analizar tanto el comportamiento del cliente como características específicas de cada reserva.

- **ID_reserva:**	Identificador único de la reserva.

- **nº_adultos:**	Número de adultos incluidos en la reserva.
- **nº_niños:**	Número de niños incluidos en la reserva.
- **noches_semana:**	Noches reservadas entre lunes y jueves.
- **noches_findesemana:**	Noches reservadas entre viernes y domingo.
- **tipo_plan_comida:**	Tipo de régimen de comidas contratado (por ejemplo, Sólo Alojamiento, Media Pensión, Pensión Completa).
necesita_parking	Indica si el huésped solicitó parking (Sí/No).
- **tipo_habitacion:**	Tipo de habitación reservada (Ej. Individual, Doble, Suite).
- **antelacion_reserva:**	Número de días entre la fecha de reserva y la fecha de llegada.
- **dia_llegada:**	Día de la semana en que está programada la llegada (Ej. Lunes, Martes…).
- **tipo_cliente:**	Tipo de cliente (por ejemplo, Recurrente, Nuevo, Grupo, Empresa).
- **nº_previas_cancelaciones:**	(Número de cancelaciones previas realizadas por el cliente).

## 5. Recap Sesiones
### Sesión 1.
- Creación del respositorio.
- Generación de archivo Readme y gitignore.
- Creación del sistema de carpetas del repo.
- Añadir el conjunto de datos original 'INNHotelsGroup.csv'

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
