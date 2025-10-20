# 🏨 Análisis de Datos para INN Hotels Group: Optimización de Reservas y Cancelaciones.

## 1. 📖 Contexto y Problema Actual
INNHotelsGroup, una cadena hotelera con múltiples ubicaciones repartidas por todo el mundo, ha identificado la necesidad de mejorar la gestión de sus reservas y así reducir el número de cancelaciones. Si bien cuentan con una plataforma digital de reservas, enfrentan ciertos desafíos, como:

- Alto número de cancelaciones previas a la llegada.

- Baja visibilidad sobre los factores que influyen en la cancelación de reservas.

- Falta de segmentación clara del tipo de cliente.

- Dificultades para optimizar la ocupación hotelera en función de la anticipación de las reservas, los planes de comidas o las necesidades específicas como el parking o los requerimientos realizamos por los clientes.

Mediante el análisis de los datos históricos de las reservas, este proyecto busca identificar patrones clave que ayuden a comprender mejor el comportamiento de los huéspedes, anticipar cancelaciones y mejorar la eficacia a la hora de gestionar las reservas.

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
  |---- INNHotelsGroup.csv   #Datos originales.
  |---- INNHotelsGroup_modificación_datos_csv #Datos columna avg_price_per_room modificados cambio . por , 
  |---- Datos_Transformados.csv #Datos listos para analisis en formato csv.
|------ Excels # Excels con el análisis de datos.
  |---- Carga_datos_originales.xlsx #Datos originales en formato excel.
  |---- Analisis_datos.xlsx # Preparación de datos para analisis.
  |---- Analisis_datos_listos.xlsx # Graficos y resultados del análisis.
  |---- Dashboard.xlsx # Dashboard con el analisis de datos finalizados.
|------ README.md # Descripción del proyecto.
```

## 4. 📊 Descripción de las columnas del Conjunto de Datos

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
- **Mes_de_reserva:** Mes en el que el cliente realiza la reserva (expresado de forma numérica).
- **Antelacion_de_la_reserva:**	Número de días entre la fecha de reserva y la fecha de llegada.
- **Cliente_previsor:**	Muestra como de previsor es el cliente respecto a la reserva del viaje (Nada_previsor, Poco_previsor, Previsor, Bastante_previsor, Extremadamente_previsor).
- **Tipo_de_segmento_de_mercado:** Muestra a que segemento del mercado al que pertenece el cliente, según la reserva realizada.
- **Cliente_repite:** Indica si el cliente repite estancia (Si, NO).
- **Nº_de_cancelaciones_previas:** Número de cancelaciones previas realizadas por el cliente.
- **Nº_de_reservas_previas_no_canceladas:** Número de reservas previas realizadas por el cliente y no canceladas.
- **Precio_medio_por_habitación:** Precio medio por día de reserva, los precios de las habitaciones son dinamicos (expresados en euros).
- **Total_gastado:** Gasto total realizado durante la estancia (expresados en euros).
- **Precio_medio_por_persona:** Indica el gasto medio que realiza cada persona por día durante la estancia (expresados en euros).
- **Nº_de_requerimientos_especiales:** Número de requerimientos especiales realizados por los clientes (planta alta, vistas desde la habitación, etc)
- **Cliente_exigente:** Muetra como de exigente es el cliente en relación a los requerimientos realizados (Nada, Poco, Bastante, Mucho).
- **Estado_de_la_reserva:** Muestra el estado de la reserva (Cancelada, No_cancelada)

## 5.  Instalación y Requisitos
- Este proyecto usa Excel, Python 3.12 y la biblioteca pandas.

## 6. 💼 Recap Sesiones

### Sesión 1.
- Creación del respositorio en Github.

- Generación de archivo Readme y gitignore.
- Creación del sistema de carpetas del repositorio.
- Añadir el conjunto de datos original 'INNHotelsGroup.csv'.
- Se cambia . por , columna avg_price_per_room para poder trabjar con decimales en la tabla de datos y se crea 'INNHotelsGroup_modificación_datos.csv'.
- Se crea el excel 'carga_datos_originales.xlsx' y se crea una tabla con el nombre Datos_Transformados para poder realizar el análisis de datos.

### Sesión 2.
- Se unieron las columnas "arrival_year", "arrival_month", "arrival_date" para crear "Fecha_de_llegada".

- Se cambiaron los valores de las columnas "required_car_parking_sapace", "repeated_guest", 0 = No y 1 = Si.
- Traducción completa de la Tabla de datos de Ingles a Español.
- Creación de columnas complementarias para la realización del análisis, "Nº_total_de_viajeros", "Viaja_con_niños", "Nº_total_de_noches", "Fecha_de_reserva", "Fecha_de_salida" "Cliente_previsor", "Fiabilidad_de_la_reserva", "Total_gastado", "Precio_medio_por_persona", "Cliente_exigente".  
- Eliminación de las filas donde el número total de noches es igual a 0, ya que una reserva donde el número total de noches es igual a 0 no tiene sentido.
- Se mantienen las filas donde el precio total es igual a 0 o con importes muy pequeños aunque a priori no tenga mucho sentido, ya que puede deberse a una promoción donde el viajero es invitado por el hotel o que el viajero este canjeando puntos y por esta razón no tenga que pagar nada o el precio a pagar sea muy pequeño.
- Creación del archivo en formato csv para mayor facilidad de trabajo en nuestra tabala de datos. (Datos_Transformados.csv)
- Creación de tabla excel con datos listos para el análisis. (Analisis_datos_listos.xlsx) 

### Sesión 3.
- Se crea la hoja de Analisis_descriptivo_numérico, dentro de nuestro excel, y se crean los resumenes de estadísticas, las tablas dinamicas, los graficos dinamicos y los Box de las columnas númericas de nuestro analisis de datos.

### Sesión 4.
- Se crea la hoja de Analisis_categórico, dentro de nuestro excel, y se crean las tablas dinamicas, los graficos dinamicos de las columnas categoricas.

- Se crea la hoja de Analisis_temporales, dentro de nuestro excel, y se crean las tablas dinamicas. los graficos dinamicos de las columnas temporales.

### Sesión 5.
- Se crea la hoja Analisis_Bv_num, para analizar la relación de las variables numéricas con el estado de la reserva.

- Se crean las tablas dinamicas de las columnas númericas incluyendo la variable Estado_de_la_reserva en cada tabla, para observar como afectan las distintas variables a las cancelaciones.
- Se crean los graficos dinamicos de las tablas númericas para observar con mayor facilidad la influencia de cada viriable en el estado de la reserva.
- Se crea la hoja de Analisis_Bv_categoricas para analizar la relación que existe entre las variables categóricas con el estado de la reserva.
- Se crean las tablas dinamicas de las columnas categoricas incluyendo la variable Estado_de_la_reserva en cada tabla, para observar como afectan las distintas variables a las cancelaciones.
- Se crean los graficos dinamicos de las tablas categoricas para observar con mayor claridad la influencia de estas variables con las cancelaciones.
- Se crea la hoja de Analisis_bv_temporales para analizar la relación que existe entre las variables temporales con el estado de la reserva. 
- Se crean las tablas dinamicas de las columnas temporales incluyendo la variable Estado_de_la_reserva en cada tabla, para observar como afectan las diferentes variables a las cancelaciones.
- Se crean los graficos dinamicos de las tablas dinamicas temporales para observar la relación que existe entre estas variables y las cancelaciones.

### Sesión 6.
- Se crean las KPIs 
- Se crean los Dashboard para tener una visión actualizada de las cancelaciones.

### Sesión 7.

 
## 7. 🧾 Resultados y Conclusiones

-

## 8. Contribuciones

- Cualquier contribucion es bien venida, si quiere colaborar en el proyecto, abre un pull request.

## 9. Autores 

- Carlos Hernando
- https://github.com/C4rl0s1515









