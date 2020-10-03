IBM Data Science Professional Certificate
Capstone Project
Rain harvesting in Mexico City
1. Introduction
Mexico City is a city where the amount of rain is more than 800 mm per year [1]. From May to October it rains almost daily. Despite this high amount of rain, there are some neighbourhoods where there is not enough water for the human needs all year around, specially in the poor ones. The water pumping system is very inefficient because it brings the water from a basin that is about 150 km, and shortages happen frequently. For that reason most of the venues pay a lot of money in pipes, specially hotels and restaurants in historic centre neighbourhood. Water scarcity in Mexico City is a fully identified problem. There are several public reports about this problem, one of them by The New York Times [2]. This great problem has dimensions of all kinds: societal, ecological, geological, urban. As early as 2001, Izazola, H. mentioned that "The solution to the crisis cannot be limited to increasing exploitation of the aquifer and the import of water from increasingly distant basins, instead that requires the competition for societal, economic, political and cultural solutions that promote more efficient use and more rational management of the resource. This includes, among many other actions, respecting the hydrological cycle, reducing waste from leaks that currently are approaching 40% of the available supply, taking advantage of stormwater, promoting water reuse, avoiding the growth of the urban area towards the periphery of the city especially in aquifer recharge zones, reducing access inequality between societal groups to safe drinking water and promoting the fair payment of actual costs. To ensure the permanence of the city, given the complexity and interdependence of the solutions demanded by the current situation of Mexico City water system, a strong effort is required by the various sectors including government, non-governmental, private sector, academia and civil society in general" [3].

During the months of March and April, which are the hottest and the driest [4], it is normal and even understandable, though not desirable, to see pipes carrying the liquid to residential and commercial areas. This is understandable since these are the last months of the dry season, when water from aquifers and lakes near the city is already ending [2]. However, also during the rainy season there is water scarcity in many neighbourhoods and you can see pipes supplying the liquid. Ironically, the supply is affected by torrential rains and when it rains the most there is also water scarcity [5]. The lack of water is constant throughout the year in the highlands of the city, because the pressure of the bombs is not enough to get the water there [6], however it is in these areas where it rains the most because they are more forested in general. During dry season there is not much to do, but during wet season the rain harvesting could be one solution. This will also save money to the city, save energy and reduce the carbon footprint produced by bringing water from far away, by pulling it out from deep wells or by pumping it to highlands. For every thousand tons of water that rises a height of 1 meter, 4.5 kWh of electricity is used, which is equivalent to 1.7 L of diesel [7]. In terms of price in Mexico, this equates to $1.44 dollars (June 2020 price).

Rain harvesting is a possible solution to this problem. In fact, this solution would serve a dual purpose: since it is not possible to store all the rainwater, a part of rain would recharge aquifers and it would serve as a reserve for the dry season. Maybe this is not a definitive solution, however it is very necessary trying to push it to its limits. Part of the problem is that this solution is expensive because we believe or we know that every house needs a large space of storage so the rain can be harnessed most of the year. In particular, Isla Urbana mentions that to live only with rainwater for 10 months in the CDMX it is best to have a 40 thousand-litre tank [8], unfortunately not all houses have the space for a tank of this volume and not many families can afford it. Zambrano mentions it takes each house to have the equivalent in space of 171 tanks of 1000 litres to live in rainwater all year around [4]. A frequency-based analysis could show that rainwater could be used during 7 months in some areas with much less storage space, maybe even 1 tank of 1000 litres.

One more variable of this problem is that the distribution of water is uneven because of diverse geographically conditions and, in fact, rain harvesting will also be uneven. That's why a geographical analysis of precipitation would be very useful to guarantee the best possible access to water for most of the people and to reduce operation costs to venues and companies.

In this project, the differences in amount of rain by county and borough in Mexico City to make a prospection of the water harvesting is calculated. By doing so, the amount of money each venue can save by investing in rain harvesting technology will be calculated.

2. Database description
To tackle this problem, we need to download several databases as we list below:

The historical database of the rain for the entire city: https://oh-iiunam.mx/mapalluvia2.html
Also here: www.conagua.gob.mx
And here http://www.sacmex.cdmx.gob.mx/sacmex/index.php/atencion-a-usuarios/factibilidad-hidrica
In case some additional data is needed it could be found here: https://www.ncdc.noaa.gov/cdo-web/
The geographical data of the boroughs in Mexico city is here: https://datos.cdmx.gob.mx/explore/dataset/coloniascdmx/table/
The water consumption in México City: https://datos.cdmx.gob.mx/explore/dataset/consumo-agua/table/
Foursquare API to get the most common venues in Mexico City.
Use of Google Earth to map each borough polygon.
In case, another map is needed: https://www.inegi.org.mx/app/mapas/default.html?t=0150001000000000&ag=21
Important: Unfortunately, the actual metropolitan urban area is divided by two different states and the more confident data is just in the state that is formerly known as Federal District.

3. Methodology
First we need to download the database of the Hydrologic Observatory of the National University. This database has several stations and each stations has its own data. Unfortunately there is no API for this database. The data has the following columns: Intensity (mm/h), Accumulative (mm), Reflectivity (dB), Visibility (m), Number of drops, kinetic energy (KJ). The main building of the City Water Office is in the Historic Centre Neighbourhood. There is also a pluviometric station in that building, so I downloaded the data from that station.





For this project we only need the intensity. The data was measured every minute and we need to sum every minute of each day to get the daily amount of rain. The daily amount of rain is a fair measurement for this purpose since it requires the least amount of money to harvest the maximum amount of water. Since during the night rains most frequently and because the rain harvesting system is passive it will be collecting water while the people is sleeping. That's why the measurement starting point was changed from 12 am to 7 am in a 24 hour period.

The frequency is the most important part of this project, because one can reduce the cost of the water tank. I made some calculations with the frequency of the rain in Mexico City. In this histogram, we see the amount of rain each week per square meter near the center of the city. 



Another way to see this data is with the distribution of the liters per week. In the left side we see the number of days in which the amount of rain was zero.


In this histogram we see the distribution of the rain intensity without the days when there is zero rain.




In this other histogram we see the distribution of the property area of all the buildings in Mexico City. This is not the same as the roof area, but it is a fair approximation to that number.



In this histogram we see the distribution of the water consumption per block in Cuauhtemoc County which is the cpunty in the center of the city.



After that, using Foursquare I explored nearby the meteorological station the data was gathered looking for the venues in the Historical Centre borough. Several hotels and restaurants are there. Unfortunately, I was not able to measure the roof of each building. This information is needed to calculate the possible amount of rain they can harvest.







Plus, the amount of water each hotel and restaurant spend is needed to calculate the return of investment in rain harvesting technology. The data is not available for each venue, instead the government reports the amount of water each block consumes. I want to use this data but I think it would take far more time. The site in which the information is:  https://datos.cdmx.gob.mx/api/records/1.0/search/?dataset=consumo-agua&q=&facet=alcaldia&facet=colonia&facet=bimestre&facet=indice_des&refine.alcaldia=CUAUHTEMOC&refine.colonia=CENTRO 

In this map we see the amount of water each block consumes. We can do that interactively in the Notebook.




In this map we see in red the center of the city, in green we see the venues near the center and in blue we see the meteorologic station. We aslo see the polygons of each block on top of the map.






The final idea was to build a file with the data of the venue, the amount of rain in the city, the area of the roof of the venue, the amount of payment for the water supply and so on to train a machine learning model and try to predict if a venue would buy a rain harvesting technology. I just put the code in place to do it but I have not enough time to compile the archive with all the variables needed. Im going to work to complete this.



4. Results
This project was a little more difficult than I expected so I was not able to finish it, nonetheless I submit the partial code I have. I took the results of the weekly amount of rain to make a presentation to a Mexican plumbing parts company.

The amount of rain is in the range expected. The entire map will show the places where rains the most in the city. Also, with Foursquare we are going to be able to locate the most suitable venues to sell rain harvesting technology based on its water consumption and money spent.

The amount of rain is far more than a venue uses during the rein season. 

5. Discussion
It is possible to improve the data and use the API provided by the government, but I was not able to do it yet. Meanwhile, the data and the code to process the rain in the city is simple and ready.

I need more time to complete this project, but once I finish I will have the amount in liters and money of each venue spend.

6. Conclusion
The code is working fine so far, unfortunately I need more time to build the next steps towards a consistent model using machine learning tools to propose a better business model for the water supply in Mexico City.

7. References
[1] Mexico City climate. Taken from https://en.wikipedia.org/wiki/Mexico_City#Climate

[2] Kimmelman, M. (February 17th, 2017). Mexico City, Parched and Sinking, Faces a Water Crisis. Mexico City. The New York Times. Taken from https://www.nytimes.com/interactive/2017/02/17/world/americas/mexico-city-sinking.html

[3] Izazola, Haydea. Agua y sustentabilidad en la Ciudad de México. Estudios Demográficos y Urbanos, núm. 47, mayo-agosto, 2001, pp. 285-320. El Colegio de México, A.C. Distrito Federal, México. (In Spanish)

[4] Zambrano, Luis. (26 de mayo de 2015). 171 tinacos. Ciudad de México, Nexos. Taken from http://labrujula.nexos.com.mx/?p=344 (In Spanish)

[5] Cohen, J., Hagerman, L. (Directores). 2014. H2Omx (documental). Cactus Film México. Taken from http://www.h2o.mx/ (In Spanish)

[6] Reporte de factibilidad hídrica, Sistema de aguas de la Ciudad de México. Taken from http://www.sacmex.cdmx.gob.mx/sacmex/index.php/atencion-a-usuarios/factibilidad-hidrica (In Spanish)

[7] Foley, J. Fundamentals of energy use in water pumping. Department of industry and Science. Australian Government. Mayo 2015. Taken from http://www.cottoninfo.com.au/sites/default/files/documents/Fundamentals%20EnergyFS_A_3a.pdf

[8] Isla Urbana A.C. (2016). Taken from http://islaurbana.org/sistemas-de-ciudad/ (In Spanish)

Code references [9] https://www.python.org/

[10] https://stackoverflow.com/

[11] https://jupyter.org/

[12] https://www.anaconda.com/
