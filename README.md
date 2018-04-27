My aim in this project is to gain some insight into patterns of urban blight, using open data sets published by the city of Detroit. Blight will be understood in terms of issues related to buildings: citations for offenses such as failure to maintain a building or its grounds, blight-related complaints to a city-run hotline, local crime rates, and indicatations that the building is or was likely to be demolished (demolition permits associated associated with the building and inclusion of the building in a list of completed demolitions).

In addition to the usual tasks of data cleaning, three fundamental challenges must be addressed before any predictive models are created. First, we construct a list buildings to be used in our models. This list will be based on the parcels of property on which the buildings stand. Essentially, the list of buildings will be a modified subset of all of the property parcels in Detroit: those that have or have had at least one building and satisfy a number of other constraints (perhaps including the constraint that there be only one building on the parcel). Second, we construct a set of labels---"blighted" or "not blighted"---to be assigned to each of the buildings. A building will be assigned one of these two labels on the basis of whether it is or was likely to be demolished. Third, we need an operational means of associating the various other blight-related aspects, such as crime rates and blight-related citations, with specific buildings. Although some of these associations will be made by means of parcel numbers, the primary means of association will be location (latitude and longitude) data, associated with the building by means of the `sf` (simple features) function `st_join`.

The project as it now stands (more or less):
https://stuartbarnum.github.io/Detroit-Demolitions/Detriot_Draft_2.html
