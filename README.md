# classification_pyspark

### Multi-Class Text Classification with PySpark (kaggle Dataset)


In this project we will use Spark Machine Learning Library to solve a multi-class text classification problem, in particular, PySpark.

### Data:
We will base our calassification on San Francisco Crime Dataset, (878k rows) The data can be downloaded from [Kaggle](https://www.kaggle.com/c/sf-crime/data).

First Dataset overview : 


|              Dates|      Category|            Descript|DayOfWeek|PdDistrict|    Resolution|             Address|                  X|                 Y|
|-------------------|--------------|--------------------|---------|----------|--------------|--------------------|-------------------|------------------|
|2015-05-13 23:53:00|      WARRANTS|      WARRANT ARREST|Wednesday|  NORTHERN|ARREST, BOOKED|  OAK ST / LAGUNA ST|  -122.425891675136|  37.7745985956747|
|2015-05-13 23:53:00|OTHER OFFENSES|TRAFFIC VIOLATION...|Wednesday|  NORTHERN|ARREST, BOOKED|  OAK ST / LAGUNA ST|  -122.425891675136|  37.7745985956747|
|2015-05-13 23:33:00|OTHER OFFENSES|TRAFFIC VIOLATION...|Wednesday|  NORTHERN|ARREST, BOOKED|VANNESS AV / GREE...|   -122.42436302145|  37.8004143219856|
|2015-05-13 23:30:00| LARCENY/THEFT|GRAND THEFT FROM ...|Wednesday|  NORTHERN|          NONE|1500 Block of LOM...|-122.42699532676599| 37.80087263276921|
|2015-05-13 23:30:00| LARCENY/THEFT|GRAND THEFT FROM ...|Wednesday|      PARK|          NONE|100 Block of BROD...|  -122.438737622757|37.771541172057795|
|2015-05-13 23:30:00| LARCENY/THEFT|GRAND THEFT FROM ...|Wednesday| INGLESIDE|          NONE| 0 Block of TEDDY AV|-122.40325236121201|   37.713430704116|
|2015-05-13 23:30:00| VEHICLE THEFT|   STOLEN AUTOMOBILE|Wednesday| INGLESIDE|          NONE| AVALON AV / PERU AV|  -122.423326976668|  37.7251380403778|
|2015-05-13 23:30:00| VEHICLE THEFT|   STOLEN AUTOMOBILE|Wednesday|   BAYVIEW|          NONE|KIRKWOOD AV / DON...|  -122.371274317441|  37.7275640719518|
|2015-05-13 23:00:00| LARCENY/THEFT|GRAND THEFT FROM ...|Wednesday|  RICHMOND|          NONE|600 Block of 47TH AV|  -122.508194031117|37.776601260681204|
|2015-05-13 23:00:00| LARCENY/THEFT|GRAND THEFT FROM ...|Wednesday|   CENTRAL|          NONE|JEFFERSON ST / LE...|  -122.419087676747|  37.8078015516515|
|2015-05-13 22:58:00| LARCENY/THEFT|PETTY THEFT FROM ...|Wednesday|   CENTRAL|          NONE|JEFFERSON ST / LE...|  -122.419087676747|  37.8078015516515|
|2015-05-13 22:30:00|OTHER OFFENSES|MISCELLANEOUS INV...|Wednesday|   TARAVAL|          NONE|0 Block of ESCOLT...|  -122.487983072777|37.737666654332706|
|2015-05-13 22:30:00|     VANDALISM|MALICIOUS MISCHIE...|Wednesday|TENDERLOIN|          NONE|  TURK ST / JONES ST|-122.41241426358101|  37.7830037964534|
|2015-05-13 22:06:00| LARCENY/THEFT|GRAND THEFT FROM ...|Wednesday|  NORTHERN|          NONE|FILLMORE ST / GEA...|  -122.432914603494|  37.7843533426568|
|2015-05-13 22:00:00|  NON-CRIMINAL|      FOUND PROPERTY|Wednesday|   BAYVIEW|          NONE|200 Block of WILL...|  -122.397744427103|  37.7299346936044|
|2015-05-13 22:00:00|  NON-CRIMINAL|      FOUND PROPERTY|Wednesday|   BAYVIEW|          NONE|0 Block of MENDEL...|-122.38369150395901|  37.7431890419965|
|2015-05-13 22:00:00|       ROBBERY|ROBBERY, ARMED WI...|Wednesday|TENDERLOIN|          NONE|  EDDY ST / JONES ST|  -122.412597377187|37.783932027727296|
|2015-05-13 21:55:00|       ASSAULT|AGGRAVATED ASSAUL...|Wednesday| INGLESIDE|          NONE|GODEUS ST / MISSI...|  -122.421681531572|  37.7428222004845|
|2015-05-13 21:40:00|OTHER OFFENSES|   TRAFFIC VIOLATION|Wednesday|   BAYVIEW|ARREST, BOOKED|MENDELL ST / HUDS...|-122.38640086995301|   37.738983491072|
|2015-05-13 21:30:00|  NON-CRIMINAL|      FOUND PROPERTY|Wednesday|TENDERLOIN|          NONE|100 Block of JONE...|  -122.412249767634|   37.782556330202|

### Main Aim: 

For each a new crime description comes in, we want to assign it to one of 33 categories. The classifier makes the assumption that each new crime description is assigned to one and only one category. This is multi-class text classification problem.

    Input: Descript

Example: “ STOLEN AUTOMOBILE”

    Output: Category

Example: VEHICLE THEFT

### Code Part

You can see my Notebook in ./notbook/multi_classification.ipynb


