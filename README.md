# ChallengeTiendaAlura
El análisis para la toma de decisión sobre cual tienda es más factible vender
### Análisis Exploratorio de Ventas por Tienda
Este proyecto realiza un análisis exploratorio de datos sobre las ventas de 4 tiendas diferentes, utilizando Python y bibliotecas como pandas y matplotlib. El objetivo principal fue entender el comportamiento de ventas, satisfacción del cliente y distribución geográfica, para extraer insights clave sobre el rendimiento de cada tienda.

#### Estructura del data set
Cada tienda cuenta con su propio archivo CSV y las columnas son:
•	Producto: nombre del artículo vendido.
•	Categoría del Producto: tipo de producto.
•	Precio: monto de venta.
•	Costo de envío: valor pagado por envío.
•	Fecha de Compra: cuándo se hizo la venta.
•	Vendedor: persona encargada de la venta.
•	Lugar de Compra: ciudad donde se compró.
•	Calificación: valoración del cliente (1 a 5).
•	Método de pago: tipo de transacción usada.
•	Cantidad de cuotas: número de pagos.
•	lat, lon: coordenadas geográficas.

#### Análisis Realizado
1. Ingreso Total por Tienda
Se sumaron los valores de la columna Precio por tienda.
Resultado visual: gráfico de barras con etiquetas mostrando el ingreso total de cada tienda.

2. Productos Vendidos por Categoría
Se utilizó value_counts() para agrupar por Categoría del Producto y contar la cantidad de ventas por categoría.
Resultado visual: gráficos de barras horizontales por tienda mostrando las categorías más populares.

3. Calificación Promedio
Se calculó la satisfacción del cliente con:
df_tiendaX['Calificación'].mean()
 Resultado: valores numéricos formateados + gráfico de dispersión cruzando ingresos vs calificación promedio.

4. Producto Más y Menos Vendido
Se usó value_counts() sobre Producto para identificar:
•	 Producto más vendido
•	Producto menos vendido
 También se graficó el Top 10 de productos más vendidos por tienda.

5. Costo de Envío Promedio
Se calculó el promedio de la columna Costo de envío para cada tienda:
df_tiendaX['Costo de envío'].mean()
Resultado en consola con formato monetario.

####  Análisis Geográfico
Se exploraron las coordenadas (lat, lon) de cada transacción para visualizar la distribución geográfica de ventas.
•	 Gráfico de dispersión: muestra los puntos de venta en el espacio geográfico por tienda.
•	Opcional: como opcional se generó un Heatmap con Folium para visualizar zonas de alta concentración de ventas.

#### Visualizaciones Generadas
1.	Gráfico de barras – Ingreso total por tienda
2.	Gráficos de barras horizontales – Categorías más populares
3.	Gráfico de dispersión – Ingreso vs calificación promedio
4.	Gráfico de barras horizontales – Top 10 productos más vendidos
5.	Gráfico de puntos geográficos – Distribución de ventas por tienda

#### Conclusiones
•	Tienda 1 generó el mayor ingreso, pero tuvo la calificación promedio más baja.
•	Tienda 3 combinó buen ingreso con la mejor calificación.
•	Muebles fue una de las categorías más populares, aunque productos como microondas lideraron individualmente.
•	Las ventas se concentran en ciudades principales como Bogotá y Medellín, lo cual podría influir en los resultados de cada tienda.
•	Existen diferencias claras entre ingresos, satisfacción y ubicación que pueden ayudar a tomar decisiones estratégicas.

 Herramientas utilizadas
•	Python
•	Pandas
•	Matplotlib
•	Seaborn (opcional)
