<h1>Simulacion para la implementacion de un sistema de trenes de larga distancia para el traslado de personas hacia diferentes provincias del país en el menor tiempo posible</h1>

_Se busca en un principio, determinar los tiempos de duración del trayecto Santo Domingo - Santiago de los Caballeros por carretera utilizando el servicio de transporte
Caribe Tours/Caribe Express, asumiendo valores fijos y predeterminados como la velocidad promedio de los autobuses, distancias del trayecto basadas en carreteras (obtenidas a través de google maps) y realizar, comparaciones en cuanto a tiempos de trayecto se refiere, planteando la hipotética implementación de un sistema de trenes que cubra la misma ruta considerando las mismas paradas, asumiendo que, en lugar de sucursales de la empresa de transporte Caribe Tours existen estaciones de tren donde los pasajeros que deseen utilizar el servicio tendrán la posibilidad de abordar el mismo._

_El modelo de tren a implementar será un Commuter Rail convencional similar, o más bien basado en el diseño de la empresa Tri Rail que provee servicio a la zona de South Florida, USA. Considerando que los trayectos exhiben, en la realidad, un tiempo de duración medio de 3 horas aproximadamente, esta simulación pretende acercarse a los tiempos de duración del trayecto en términos de viaje en vehículo y mejorar los mismos en términos de viajes en tren. Así mismo, brindar la posibilidad de exhibir una comparación realista en términos de, tiempos de trayecto, precios y afluencia de pasajeros y probar que, de hecho, existe una mejora sustancial si se implementara el sistema de trenes para cubrir este y otros trayectos._

## Tecnologias utilizadas 🛠️

* Python
* Modsim
* Numpy
* MatPlotLib

## Analisis del sistema actual

Para el transporte entre provincias, el sistema utilizado es el de autobuses, en nuestro caso utilizamos la empresa Caribe Tours la cual es una de las empresas más importantes en este ámbito 
Utilizando la información proporcionada por Caribe Tours tenemos que: 
* La capacidad de sus autobuses es de 54 asientos 
* El precio de los viajes oscila entre RD$200.00 y RD$350.00 
* El punto de partida principal en la provincia de Santo Domingo se encuentra en la Calle 27 de febrero, Esq. Leopoldo Navarro, Santo Domingo, D. N. 
* El tiempo de parada es de 15 minutos (900 segundos) 
* Los usuarios solo pueden abordar el autobús en la primera parada
Usando la información obtenida tenemos que: 

![imagen](https://user-images.githubusercontent.com/59454398/149786106-eafff050-eeee-4ad9-8b70-05860f41bd8f.png)

Al utilizar un autobús de Caribe Tours para llegar a Santiago desde Santo Domingo, con paradas en Bonao y La Vega y sin tapones o horas pico, el tiempo final al destino es de 3.44 horas si el autobús no realiza ninguna parada y de 3.94 horas si el autobús realiza paradas en Bonao y La Vega 

Tomando en cuanto los tapones que puedan ocurrir en las horas pico del día se obtiene que: 

![imagen](https://user-images.githubusercontent.com/59454398/149786269-4e032d07-2802-4c0a-98a7-389c5979a379.png)

El tiempo final para llegar a Santiago desde Santo Domingo, con paradas en Bonao y La Vega, oscila entre 4.2 horas y 4.39 horas 
Dicho trayecto tendría un costo de RD$300.00 según las tarifas ofrecidas por Caribe Tours 

## Sistema Propuesto

Para desarrollar el sistema propuesta utilizamos el tren Tri Rail el cual sería una buena opción para implementar como mejora del sistema actual. Dicho tren cuenta con las siguientes características: 
* La capacidad del tren es de alrededor de 182 personas 
* El precio de utilizar el tren hacia cualquier punto es de US$6.00 lo que en moneda local serían unos RD$300.00 
* El tren tiene una velocidad promedio de 26.11 m/s 
* El tren tiene una velocidad máxima de 35.27 m/s 
* El tiempo de parada es de 3 minutos (180 segundos) 
* Los usuarios pueden abordar el tren en cualquier parada
Usando la información obtenida tenemos que: 

![imagen](https://user-images.githubusercontent.com/59454398/149786514-50561c42-c460-4169-b4fb-438cdc85c79f.png)

Al utilizar un tren de Tri Rail para llegar a Santiago desde Santo Domingo, con paradas en Bonao y La Vega y sin tapones o horas pico, el tiempo final al destino es de 2.96 horas si el tren no realiza ninguna parada y de 3.06 horas si el tren realiza paradas en Bonao y La Vega 
Dicho trayecto tendría un costo de RD$345.00  

## Analisis de resultados

Tomando en cuenta los datos obtenidos previamente podemos proceder a analizar y comparar ambos sistemas: 

![imagen](https://user-images.githubusercontent.com/59454398/149786623-077471ac-de0b-4a96-944e-fa058c2d2327.png)

Como se puede observar en la gráfica, la implementación del tren en la ruta Santo Domingo-Santiago reduce el tiempo de llegada de 3.94 horas utilizando los autobuses de Caribe Tours y con paradas en Bonao y La Vega, a 3.07 horas utilizando el tren Tri Rail con paradas en Bonao y La Vega, una diferencia de 0.87 horas 

![imagen](https://user-images.githubusercontent.com/59454398/149786660-6f4d1623-0a21-4403-a74e-0e805e559bc3.png)

En el caso de que se utilice la velocidad máxima del tren, este tiempo se reduce aún más, siendo este de 2.3 horas de trayecto desde Santo Domingo a Santiago, con paradas en Bonao y La Vega 
La siguiente grafica resume las diferencias mencionadas: 

![imagen](https://user-images.githubusercontent.com/59454398/149786720-9c59eb14-9542-4a05-ae1a-becdbe926fd6.png)

* Autobús con paradas: 3.94 horas 
* Autobús sin paradas: 3.44 horas 
* Tren a velocidad promedio: 3.07 horas 
* Tren a velocidad máxima: 2.3 horas 
Para el trayecto hacia las paradas de manera independiente obtenemos los siguientes resultados: 

![imagen](https://user-images.githubusercontent.com/59454398/149786805-80bf090c-a60b-4643-b645-bd8f5eddd651.png)

Donde el tiempo al usar autobús en horas pico desde Santo Domingo a La Vega es de 3.12 horas con un precio de RD$250 según la tarifa indicada por Caribe Tours, mientras que al usar el tren a velocidad promedio el tiempo sería de 2.31 horas con un precio de RD$345 
Para el trayecto de Santo Domingo a Bonao: 

![imagen](https://user-images.githubusercontent.com/59454398/149786856-5d7ad033-19d2-4a10-a047-194c54594cee.png)

Donde el tiempo al usar autobús en horas pico desde Santo Domingo a Bonao es de 2.07 horas con un precio de RD$200 según la tarifa indicada por Caribe Tours, mientras que al usar el tren a velocidad promedio el tiempo sería de 1.56 horas con un precio de RD$345 

## Autores ✒️

* **Cristian Tejeda** - *Codificacion de la simulacion* - [elcris-s](https://github.com/elcris-s)
* **Andres Nuñez** - *Levantamiento de informacion y analisis de resultados*
