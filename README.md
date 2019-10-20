# Hawa
# The Challenge:
"The challenge is to integrate NASA data, ground-based air quality data, and citizen science data to create an air quality surface that displays the most accurate data for a location and time. Create algorithms that select or weight the  best data from several sources for a specific time and location, and display that information" [*1]

--------------------------------------------------------------------------------------------------------
# Hawa
Hawa is one of the NASA challenges for 2019. It is an algorithm that integrates the most accurate data that indicates more efficiency about the Air quality for a specific location and time:


-----------------------------------------------------------------------------------------------------------
# Quesitions to answer:
1. [As long as we deal with an existed data? who is the resource of the input data? Who is going to benefit from our output?]
>>>


2.[ Why air quality? Why the world care about the air quality? what is the core value of this algorithm?]
>>>---------------------
"Air pollution is associated with almost 5 million annual deaths worldwide as well as harm to countless others through negative health impacts from asthma and diabetes to cardiovascular disease an cancer. The World Bank estimates that air pollutio cosets the global economy $225 billion in lost labor income and $5 trillion in welfare losses annually" [*2] [**]



3. [Those who will use Hawa algorithm, what are the addressed problem in real world that they want to solve using Hawa Algorithm?]
>>>



4. [How is Hawa algorithm going to be different form the existed methodologies> Can we address what companies, organizations, or existed industries and agencies that have a strong technology that similar or better than Hawa algorithm in any way? ]
*note: this question indicates the energy and passion that push us to keep Hawa uniqueness, success, cooperation, and partnership     
>>>



5. [From a scientific stand point, what are the main factors that the air quality relying on?]
>>> 


----------------------------------------------------------------------------------------------
# Resources:
[*1] Sustainability at the U.S. Department of state:
https://www.state.gov/communications-outreach-and-partnerships/#space-apps
> "more than 100 U.S. experts from municipal, state, and Federal governments and universities have been paired with embassies and consulates to help Fellows have helped build capacity and understanding about how to understand air quality data, both within the embassy community and with host governments."

[*2] https://2019.spaceappschallenge.org/challenges/living-our-world/surface-air-quality-mission/details

-----------------------------------------------------------------------------------------------------
# information for the presentation:
Air pollution is associated with almost 5 million annual deaths worldwide as well as harm to countless others through negative health impacts from asthma and diabetes to cardiovascular disease an cancer. The World Bank estimates that air pollutio cosets the global economy $225 billion in lost labor income and $5 trillion in welfare losses annually" [*2] 
Yet real-time, realiable air quality data are not avaliable in most of the world, leaving people with a significant and harmful knowledge gap. 



----------------------------------------------------------
# Sample Data for the Surface-to-Air Quality Mission:
( The following data has been compiled with satellite data, local meteorological data, and ground reference monitor data for the sites in three different location; they are:
a. Los Angeles, CA, USA
b. Delhi, India 
c. Addis Ababa, Ethiopia

  # Aerosol Otical Depth (AOD) Data:
  AOD is a unitless quaitity representing the opacity of the atmosphere form ground to dspace at the fiven location and time. Each measurement line includes the AOD form the 10km x 10 Km grid pint closest to the ground sites as wll as the average .
  Aerosol optical depth is a measure of the extinction of the solar beam by dust and haze. In other words, particles in the atmosphere (dust, smoke, pollution) can block sunlight by absorbing or by scattering light. ... An average aerosol optical depth for the U.S. is 0.1 to 0.15.https://www.esrl.noaa.gov/gmd/grad/surfrad/aod/
  
  https://www.state.gov/wp-content/uploads/2019/10/AOD_DATA.zip
  includes satellite derived Aerosol optical Depth produced from NASA MODIS instruments on the Terra(morning) and Aqua(afternoon) satellites using NASA'S Deep Blue and Dark target Algorithm. https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/20140012657.pdf
  
  ** What does the Terra satellite do?
In December 1999, NASA launched the Terra satellite as the flagship mission of the Earth Observing System to answer these questions. The Terra satellite carries five instruments that observe Earth's atmosphere, ocean, land, snow and ice, and energy budget https://www.nasa.gov/mission_pages/terra/spacecraft/index.html

  ** Aqua is an Earth Science satellite mission that collects information on our water systems. The satellite has six different Earth-observing instruments on board and streams approximately 89 gigabytes of data per day. https://www.nasa.gov/mission_pages/aqua/index.html
  
  For each location, there are two files: those ending with MOD04: ARE FROM THE MORNING satellite and those with MYD04 are fromthe afternoon satellite
  
  Tiny solid and liquid particles suspended in the atmosphere are called aerosols. Windblown dust, sea salts, volcanic ash, smoke from wildfires, and pollution from factories are all examples of aerosols. Depending upon their size, type, and location, aerosols can either cool the surface, or warm it. They can help clouds to form, or they can inhibit cloud formation. And if inhaled, some aerosols can be harmful to people's health.https://earthobservatory.nasa.gov/global-maps/MODAL2_M_AER_OD
  
  An optical thickness of less than 0.1 (palest yellow) indicates a crystal clear sky with maximum visibility, whereas a value of 1 (reddish brown) indicates very hazy conditions.
High aerosol amounts are linked to different process in different places and times of year. High aerosol amounts occur over South America from July through September. This pattern is due to land clearing and agricultural fires that are widespread across the Amazon Basin and Cerrado regions during the dry season.

Readme: (product name):
- MYD04: this represents MODIS-AQUA satellite (afternoon overpass)
-MOD04:  this represents MODIS-TERRA Satellite (morning overpass) 
data ordered in each file:
- YYYY, MM, DD, latitude, longitude , AOD1, AD3 STD3
where AOD1: Aerosal optical Depth at 550 nm for nearest gird to ground location 
AOD3:  Aeorsal optical depth at 55 nm

# Meteorological Data:
The file: https://www.state.gov/wp-content/uploads/2019/10/MERRA2.zip
this contains 365 meterological data files corresponding to each day of 2018. within each files are 24 hourly measurements for each of the 22 statioin locations. each hourly measurements includes locaiton, date, time, water vapor, temperature, wind speed, and trace gas concentrations. 
MERRA2 Data Columns

"""
**Station – Name of ground monitor for data row
Lat – Latitude (degrees north) of station
Lon – Longitude (degrees east) of station
SRadius – Search radius (km) for nearest MERRA grid point to station
MERRALat – Latitude (degrees north) of nearest MERRA grid point to station
MERRAlon – Longitude (degrees east) of nearest MERRA grid point to station
IDXi – I index of MERRA grid point
IDXj – J index of MERRA grid point
PS – Surface pressure (Pa)
QV10m – Specific humidity at 10 m above surface (kg/kg)   	(multiplied by 1000.0)
Q500 - Specific humidity at 500 mbar pressure (kg/kg) 		(multiplied by 1000.0)
Q850 – Specific humidity at 850 mbar pressure (kg/kg) 		(multiplied by 1000.0)
T10m – Temperature at 10 m above surface (Kelvin)
T500 – Temperature at 500 mbar pressure (Kelvin)
T850 – Temperature at 850 mbar pressure (Kelvin)
Wind – Surface wind speed (m/s)
BCSMASS – Black Carbon mass concentration at surface (μg/m3)
DUSMASS25 – Dust surface mass PM 2.5 concentration at surface (μg/m3)
OCSMASS – Organic carbon mass concentration at surface (μg/m3)
SO2SMASS – Sulphur dioxide mass concentration at surface (μg/m3)
SO4SMASS – Sulphate aerosol mass concentration at surface (μg/m3)
SSSMASS25 – Sea Salt surface mass concentration PM 2.5 (μg/m3)
TOTEXTTAU – Total aerosol extinction AOT @ 550 nm (unitless)
UTC_DATE – YearMonthDay (GMT date)
UTC_TIME – Time of sample (hours) (GMT time)
"""

These data were produced by NASA using satellite obervasions merged with atmosphered model forecasts in the reanalysis to provide the best estimates in the retorspective sense of atmospheric quantitie. these data are typically used to quantity and the near surfce particulate matter quantities such as PM2.5 And PM10

PM2.5 refers to atmospheric particulate matter (PM) that have a diameter of less than 2.5 micrometers, which is about 3% the diameter of a human hair.

# Refernce Ground Monitor Data:
https://www.state.gov/wp-content/uploads/2019/10/Reference_Monitor_Data.zip 
contains historical measurements of ground pollutants at each of the 22 locations for various time periods between 2016 and 2019. Each files contains mesuremennt of the PM2.5, P.M10, and trace gas pollutants for time periods and sampling intervals that vary by site.Not all sites have all data for the full period.. 

these data were obtained from the open AQ website.Other historical da
 

# How is Air Quality Measured?
- Air quality is measured with Air Quality index, or AQI. it works like thermometer that runs form 0 to 500 degress. However, instead of showing changes in the temperature, the AQI is a way of showing changes in the amount of pollution in the air.https://www.epa.gov/sites/production/files/2014-05/documents/zell-aqi.pdf

# PSI ( Pollutant standards index) 
https://www.haze.gov.sg/docs/default-source/faq/computation-of-the-pollutant-standards-index-(psi).pdf



