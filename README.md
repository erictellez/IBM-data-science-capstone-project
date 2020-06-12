# IBM Data Science Professional Certificate 
# Capstone Project

## Rain harvesting in Mexico City
#### 1. Introduction
Mexico City is a city where the amount of rain is more than 800 mm per year [1]. From May to October it rains almost daily. Despite this high amount of rain, there are some neighbourhoods where there is not enough water for the human needs all year around, specially in the poor ones. The water pumping system is very inefficient because it brings the water from a basin that is about 150 km, and shortages happen frequently. For that reason most of the venues pay a lot of money in pipes, specially hotels and restaurants in historic centre neighbourhood. 
Water scarcity in Mexico City is a fully identified problem. There are several public reports about this problem, one of them by The New York Times [2]. This great problem has dimensions of all kinds: societal, ecological, geological, urban. As early as 2001, Izazola, H. mentioned that "The solution to the crisis cannot be limited to increasing exploitation of the aquifer and the import of water from increasingly distant basins, instead that requires the competition for societal, economic, political and cultural solutions that promote more efficient use and more rational management of the resource. This includes, among many other actions, respecting the hydrological cycle, reducing waste from leaks that currently are approaching 40% of the available supply, taking advantage of stormwater, promoting water reuse, avoiding the growth of the urban area towards the periphery of the city especially in aquifer recharge zones, reducing access inequality between societal groups to safe drinking water and promoting the fair payment of actual costs. To ensure the permanence of the city, given the complexity and interdependence of the solutions demanded by the current situation of Mexico City water system, a strong effort is required by the various sectors including government, non-governmental, private sector, academia and civil society in general" [3].

During the months of March and April, which are the hottest and the driest [4], it is normal and even understandable, though not desirable, to see pipes carrying the liquid to residential and commercial areas. This is understandable since these are the last months of the dry season, when water from aquifers and lakes near the city is already ending [2]. However, also during the rainy season there is water scarcity in many neighbourhoods and you can see pipes supplying the liquid. Ironically, the supply is affected by torrential rains and when it rains the most there is also water scarcity [5]. The lack of water is constant throughout the year in the highlands of the city, because the pressure of the bombs is not enough to get the water there [6], however it is in these areas where it rains the most because they are more forested in general. During dry season there is not much to do, but during wet season the rain harvesting could be one solution. This will also save money to the city, save energy and reduce the carbon footprint produced by bringing water from far away, by pulling it out from deep wells or by pumping it to highlands. For every thousand tons of water that rises a height of 1 meter, 4.5 kWh of electricity is used, which is equivalent to 1.7 L of diesel [7]. In terms of price in Mexico, this equates to $1.44 dollars (June 2020 price).

Rain harvesting is a possible solution to this problem. In fact, this solution would serve a dual purpose: since it is not possible to store all the rainwater, a part of rain would recharge aquifers and it would serve as a reserve for the dry season. Maybe this is not a definitive solution, however it is very necessary trying to push it to its limits. Part of the problem is that this solution is expensive because we believe or we know that every house needs a large space of storage so the rain can be harnessed most of the year. In particular, Isla Urbana mentions that to live only with rainwater for 10 months in the CDMX it is best to have a 40 thousand-litre tank [8], unfortunately not all houses have the space for a tank of this volume and not many families can afford it. Zambrano mentions it takes each house to have the equivalent in space of 171 tanks of 1000 litres to live in rainwater all year around [9]. A frequency-based analysis could show that rainwater could be used during 7 months in some areas with much less storage space, maybe even 1 tank of 1000 litres.

One more variable of this problem is that the distribution of water is uneven because of diverse geographically conditions and, in fact, rain harvesting will also be uneven. That's why a geographical analysis of precipitation would be very useful to guarantee the best possible access to water for most of the people and to reduce operation costs to venues and companies.

In this project, the differences in amount of rain by county and borough in Mexico City to make a prospection of the water harvesting is calculated. By doing so, the amount of money each venue can save by harvesting water will be calculated.

#### 2. Database description
To tackle this problem, we need to download several databases as we list below: 
- The historical database of the rain for the entire city: https://oh-iiunam.mx/mapalluvia2.html 
- Also here: www.conagua.gob.mx 
- And here http://www.sacmex.cdmx.gob.mx/sacmex/index.php/atencion-a-usuarios/factibilidad-hidrica
- In case some additional data is needed it could be found here: https://www.ncdc.noaa.gov/cdo-web/
- The geographical data of the boroughs in Mexico city is here: https://datos.cdmx.gob.mx/explore/dataset/coloniascdmx/table/
- Foursquare API to get the most common venues in Mexico City.
- Use of Google Earth to map each borough polygon.
- In case, another map is needed: https://www.inegi.org.mx/app/mapas/default.html?t=0150001000000000&ag=21

Important:  Unfortunately, the actual metropolitan urban area is divided by two different states and the more confident data is just in the state that is formerly known as Federal District.

#### 3. Methodology

#### 4. Results

#### 5. Discussion

#### 6. Conclusion

##### 7. References
[1] Mexico City climate. Taken from https://en.wikipedia.org/wiki/Mexico_City#Climate

[2] Kimmelman, M. (February 17th, 2017). Mexico City, Parched and Sinking, Faces a Water Crisis. Mexico City. The New York Times. Taken from
https://www.nytimes.com/interactive/2017/02/17/world/americas/mexico-city-sinking.html

[3] Izazola, Haydea. Agua y sustentabilidad en la Ciudad de México. Estudios Demográficos y Urbanos, núm. 47, mayo-agosto, 2001, pp. 285-320. El Colegio de México, A.C. Distrito Federal, México. (In Spanish)

[4] Zambrano, Luis. (26 de mayo de 2015) 171 tinacos. Ciudad de México, Nexos. Taken from http://labrujula.nexos.com.mx/?p=344 (In Spanish)

[5] Cohen, J., Hagerman, L. (Directores). 2014. H2Omx (documental). Cactus Film México.
Taken from http://www.h2o.mx/ (In Spanish)

[6] Reporte de factibilidad hídrica, Sistema de aguas de la Ciudad de México. Taken from http://www.sacmex.cdmx.gob.mx/sacmex/index.php/atencion-a-usuarios/factibilidad-hidrica (In Spanish)

[7] Foley, J. Fundamentals of energy use in water pumping. Department of industry and Science. Australian Government. Mayo 2015. Taken from
http://www.cottoninfo.com.au/sites/default/files/documents/Fundamentals%20EnergyFS_A_3a.pdf

[8] Isla Urbana A.C. (2016) Taken from http://islaurbana.org/sistemas-de-ciudad/ (In Spanish)

[9] Zambrano, Luis. (26 de mayo de 2015) 171 tinacos. Ciudad de México, Nexos. Taken from http://labrujula.nexos.com.mx/?p=344 (In Spanish)
