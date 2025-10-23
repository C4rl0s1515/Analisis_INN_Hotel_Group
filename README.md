# 🏨 Análisis de Datos para INN Hotels Group: Optimización de Reservas y Cancelaciones.

## 1. 📖 Contexto y Problema Actual
INNHotelsGroup, una cadena hotelera con múltiples ubicaciones repartidas por todo el mundo, ha identificado la necesidad de mejorar la gestión de sus reservas y así reducir el número de cancelaciones. Si bien cuentan con una plataforma digital de reservas, enfrentan ciertos desafíos, como:

- Alto número de cancelaciones previas a la llegada.

- Baja visibilidad sobre los factores que influyen en la cancelación de reservas.

- Falta de segmentación clara del tipo de cliente.

- Dificultades para optimizar la ocupación hotelera en función de la anticipación de las reservas, los planes de comidas o las necesidades específicas como el parking o los requerimientos especiales realizamos por los clientes.

Mediante el análisis de los datos históricos de las reservas, este proyecto busca identificar patrones clave que ayuden a comprender mejor el comportamiento de los huéspedes, y así poder anticipar las cancelaciones y mejorar la eficacia a la hora de gestionar las reservas.

## 2. 🎯 Objetivo principal del Proyecto 

El objetivo principal de este análisis es desarrollar un dashboard interactivo que proporcione una visión clara y actualizada sobre las reservas y los tipos de clientes, facilitando la toma de decisiones a la hora de:

- Gestionar y predecir las cancelaciones.

- Optimizar la ocupación de las reservas según el tipo de habitación o el plan de comidas.

- Analizar las tendencias de reservas por meses del año y antelación de la reserva.

- Segmentar a los clientes según su comportamiento y preferencias.

Este dashboard estará acompañado de un informe final explicando las principales conclusiones obtenidas y recomendaciones para la mejora del negocio.

## 3. 📁 Estructura del Proyecto
```bash
|------ data # Archivos csv con datos crudos.                  
  |---- INNHotelsGroup_datos_originales.csv   #Datos originales.
  |---- INNHotelsGroup_datos_listos.csv #Datos listos para el análisis, columna avg_price_per_room modificada. (cambio . por , para que excel pueda leer el archivo)
|------ Excels # Archivo excel con el análisis de datos.
  |---- Análisis_datos_INNHotels.xlsx # Análisis de datos completo.
|------ README.md # Descripción del proyecto.
|------ Informe Final Cancelaciones INNHotelsGroup.pdf # Informe con el analisis, resultados y conclusiones obtenidos.
```

## 4. 📊 Descripción de las columnas del Conjunto de Datos

El conjunto de datos utilizado para este proyecto contiene información sobre reservas realizadas en los hoteles del grupo INN Hotels Group. Las variables incluidas permiten analizar tanto el comportamiento del cliente como características específicas de cada reserva.

- **ID_reserva:**	Identificador único de la reserva.

- **Nº_adultos:**	Número de adultos incluidos en la reserva.
- **Nº_niños:**	Número de niños incluidos en la reserva.
- **Nº_total_de_viajeros:** Número total de personas que viajan (incluye adultos y niños).
- **Solo_adultos:** Indica si en el viaje lo realizan solo adultos (Si, NO).
- **Nº_de_noches_fin_de_semana:**	Noches reservadas entre sabado y domingo.
- **Nº_de_noches_entre_semana:**	Noches reservadas entre lunes y viernes.
- **Nº_total_de_noches:** Noches reservadas en total, incluye días entre semana y fin de semana.
- **Plan_de_comida:**	Tipo de régimen de comidas contratado para el viaje (Desayuno, Media Pensión, Pensión Completa, No Seleccionado).
- **Plaza_de_parking:**	Indica si el huésped solicitó plaza de parking (Si, No).
- **Tipo_de_habitacion:**	Tipo de habitación reservada. (Los valores estan codificados por INN Hotels)
- **Fecha_de_reserva:** Día en que el cliente realiza la reserva.
- **Fecha_de_llegada:** Día en que el cliente llega al Hotel de destino.
- **Fecha_de_salida:** Día en que el cliente se va del Hotel.
- **Mes_de_reserva:** Mes en el que el cliente realiza la reserva.
- **Antelacion_de_la_reserva:**	Número de días entre la fecha de reserva y la fecha de llegada.
- **Tipo_de_segmento_de_mercado:** Muestra a que segemento del mercado al que pertenece el cliente, según la reserva realizada.
- **Cliente_repite:** Indica si el cliente repite estancia. (Si, NO)
- **Nº_de_cancelaciones_previas:** Número de cancelaciones previas realizadas por el cliente.
- **Nº_de_reservas_previas_no_canceladas:** Número de reservas previas realizadas por el cliente y no canceladas.
- **Precio_medio_por_habitación:** Precio medio por día de reserva, los precios de las habitaciones son dinamicos. (expresados en euros)
- **Total_gastado:** Gasto total realizado durante la estancia. (expresados en euros)
- **Precio_medio_por_persona:** Indica el gasto medio que realiza cada persona por día durante la estancia. (expresados en euros)
- **Nº_de_requerimientos_especiales:** Número de requerimientos especiales realizados por los clientes. (planta alta, vistas desde la habitación, etc)
- **Cliente_exigente:** Muetra como de exigente es el cliente en relación a los requerimientos realizados (Nada, Poco, Bastante, Mucho).
- **Estado_de_la_reserva:** Muestra el estado de la reserva. (Cancelada, No_cancelada)

## 5.  Instalación y Requisitos
- Este proyecto usa Excel, Python 3.12 y la biblioteca pandas.

## 6. 💼 Recap Sesiones

### Sesión 1.

- Creación del respositorio en Github.

- Generación de archivo Readme.
- Creación del sistema de carpetas del repositorio.
- Se añade el conjunto de datos original 'INNHotelsGroup_datos_originales.csv'.
- Se cambia . por , en la columna avg_price_per_room para poder trabjar con decimales en la tabla de datos y se crea 'INNHotelsGroup_datos_listos.csv'.
- Se crea el excel 'Análisis_datos_INNHotels.xlsx' y se crea una tahojabla con el nombre Datos_Transformados para realizar el análisis de datos.

### Sesión 2.

- Se unieron las columnas "arrival_year", "arrival_month", "arrival_date" para crear "Fecha_de_llegada".

- Se cambiaron los valores de las columnas "required_car_parking_sapace", "repeated_guest", 0 = No y 1 = Si.
- Se crea la hoja de Tablas_Auxiliares para poder realizar los cambios requeridos en la hoja de Datos_transformados.
- Traducción completa de la Tabla de datos de Ingles a Español.
- Creación de columnas complementarias para la realización del análisis, "Nº_total_de_viajeros", "Solo_adultos", "Nº_total_de_noches", "Fecha_de_reserva", "Fecha_de_salida" "Mes_de_reserva", "Total_gastado", "Precio_medio_por_persona", "Cliente_exigente".  
- Eliminación de las filas donde el número total de noches es igual a 0, ya que una reserva donde el número total de noches de un viaje es igual a 0 no tiene sentido.
- Se eliminan las filas donde el número de adultos es igual a 0, porque los niños no pueden viajar solos.
- Se mantienen las filas donde el precio total es igual a 0 o con importes muy pequeños aunque a priori no tenga mucho sentido, ya que puede deberse a una promoción donde el viajero es invitado por el hotel o que el viajero este canjeando puntos y por esta razón no tenga que pagar nada o el precio a pagar sea muy pequeño.

### Sesión 3.

- Se crean las hojas de Analisis_descriptivo_numérico, Analisis_categórico, Analisis_temporales.

### Sesión 4.

- Se crea la hoja Analisis_Bv_num, Analisis_Bv_categoricas, Analisis_bv_temporales, para analizar la relación que existe entre las distintas variables con el estado de la reserva. 

### Sesión 5.

- Se crea la hoja con la Matriz de correlación y se calcula el coeficiente de correlación.

### Sesión 6.

- Se crean las KPIs. 
- Se crea el Dashboard_Clientes y el Dashboard_Reservas para tener una visión actualizada de las cancelaciones.
 
## 7. 🧾 Resultados y Conclusiones

Los resultados nos muestran que la demanda es mayoritariamente adulta. Predominan viajes de dos personas (>65 %) y estancias de 2–3 noches (70 %). Un 33 % de las reservas se realizan entre 0–29 días de antelación. El precio por habitación se concentra entre 50–150 € (>88 %) y el gasto total entre 0–500 € (>85 %, con 45 % <250 €). 

La opción solo "desayuno” supera el 75 % de las reservas, el canal online es el más usado (60 %) y la habitación Tipo 1 es la más solicitada (75 %). La fidelidad ronda el 97,5 % y el parking se solicita en menor medida (3 %). Las llegadas se concentran entre agosto–octubre y caen en enero. 

La cancelación supera el 30 %, baja con mayor antelación y mayor gasto, y es menor en repetidores y en quienes solicitan parking.

En conclusión podemos decir que la antelación es la palanca principal, por eso incentivar la reserva temprana reduce cancelaciones y estabiliza la ocupación. Aplicar políticas por tramos, más flexibilidad cuando falta mucho y menos en última hora, con opciones no reembolsables.

Enfocar precios y paquetes promocionales en el rango 50–150 € por noche, potenciar la fidelización con ventajas a clientes repetidores y a reservas con más de 21 días de antelación. Controlar el canal online con cupos y condiciones homogéneas, ajustar el inventario hacia las habitaciones Tipo 1 en picos de llegada. 

Con estos ajustes se espera menor tasa de cancelación, mayor ocupación efectiva y mejor previsión en temporada alta.

## 8. Contribuciones

- Cualquier contribucion es bien venida, si quiere colaborar en el proyecto, abre un pull request.

## 9. Autores 

- Carlos Hernando
- https://github.com/C4rl0s1515









