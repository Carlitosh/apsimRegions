apsimRegions
============

apsimRegions es una suite de herramientas de software diseñandas para entender el modelo de simulacion de cultivos Agricultural Production Systems sIMulator (APSIM) desde un punto a una escala espacial regional. Esta escrito en el lenguaje de programacion python y esta actualmente su compatibilidad en la version APSIM 7.4. ApsimRegions es esenc

ApsimRegions es esencialmente un framework  de modelado de cultivos que vincula datos meteorológicos en cuadrícula (lluvia, temperatura, radiación, etc.) con el modelo APSIM. Consulte http://www.apsim.info/Wiki para obtener más información sobre APSIM. Actualmente solo se ha probado con Python 2.7.3. Para comenzar con Python, pruebe Python (X, Y) que se puede descargar en https://python-xy.github.io. El IDE de Spyder incluido es muy similar a Matlab.

Se utiliza para crear y ejecutar archivos .apsim con muchos miles de simulaciones. Cada simulación puede representar una ubicación única o un escenario de gestión. La forma más sencilla de utilizar cada simulación para diferentes ubicaciones sería crear una tabla de búsqueda con un número de punto de cuadrícula y la latitud y la longitud asociadas. Cada simulación se nombraría desde el punto de la cuadrícula. Además, cree un archivo .met único para cada punto de la cuadrícula y haga referencia a ellos en cada simulación. Entonces es posible recorrer todos los puntos de la cuadrícula y crear simulaciones únicas (archivo .met, reglas de gestión, tipo de suelo, etc.) para cada punto de la cuadrícula.

- The apsimRegions directory contains code for creating the APSIM files (preprocess). Just move the package to your Python site-packages folder (ie C:\Python27\Lib\site-packages) and import the apsimRegions package by using in Python:

  import apsimRegions as ar

  Call all the funtions by using ar.{function}

- The scrips directory contains code for running APSIM. Copy both apsimRun.py and utils.py to your APSIM installation directory. Run them on Windows from the command line by using the command:

  C:\{data_directory}> "C:/Program Files (x86)/Apsim74-r2286/Model/ApsimRun.py"
  
  from the directory containing .apsim file(s) you wish to run. The associated .out and .sum files will be generated as the script runs, but will be removed after it is completed and the files are archived (*.tar.gz) and saved to a SQLite database. See the run.bat example in the examples folder.
  
  
  
