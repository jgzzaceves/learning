
# Introduction

Suppose you are the owner of a coffee shop franchise and are looking for a place to put a new place in Mexico. Among the options, you need to choose one of the three major cities in the country: Monterrey, CDMX, and Guadalajara. You focus on three aspects to make the best decision: density of coffee shops, per capita income and population density. So, you will pick the city that has the lowest number of coffee shops per capita around downtown.

# Data

I will obtain the location of coffee shops in these 3 mexican cities using Foursqaure API. The socioeconomic data I'll obtain from the following pages: https://es.wikipedia.org/wiki/Anexo:Entidades_federativas_de_M%C3%A9xico_por_superficie,_poblaci%C3%B3n_y_densidad and https://es.wikipedia.org/wiki/Anexo:Estados_de_M%C3%A9xico_por_PIB_per_c%C3%A1pita. I will calculate an weighted indicator taking into account all this info to make a decision.

# Methodology

I will call the Foursquare API to obtain the 100 closest coffe shops to the city's downtown (this limitation is due to the maximum queries allowd by the free tier Foursquare API). Then, I will aid myself with a map to visualize the density of venues in each city. The proxy I'll use for coffe shop density will be the mean distance to the downtown of all venues.

Then, I will scrape the wikipedia websites described in the data section so I can obtain the data of population density and per capita income for each of the cities. For this I will require the beautiful soup package. Because a higher income per capita is preferable, I'll get its inverse to obtain consistent indicator.

Finally, I'll normalize de data and get the mean of the three indicators, choosing the one with the lowest value.

# Results

Our original data frame is the following:

![Screen%20Shot%202020-04-26%20at%2012.47.06%20AM.png](attachment:Screen%20Shot%202020-04-26%20at%2012.47.06%20AM.png)

Our results indicate that Guadalajara is the best city to open a coffee shop. This is represented in the following table are:

![Screen%20Shot%202020-04-26%20at%2012.47.12%20AM.png](attachment:Screen%20Shot%202020-04-26%20at%2012.47.12%20AM.png)

Which can be partially sustained by the maps presented here (low density is desired):

Guadalajara:

![Screen%20Shot%202020-04-26%20at%2012.48.07%20AM.png](attachment:Screen%20Shot%202020-04-26%20at%2012.48.07%20AM.png)

Monterrey:

![Screen%20Shot%202020-04-26%20at%2012.50.02%20AM.png](attachment:Screen%20Shot%202020-04-26%20at%2012.50.02%20AM.png)

Mexico City:

<img src="<img src="learning/Screen%20Shot%202020-04-26%20at%2012.49.48%20AM.png">

# Discussion

Our conclusion is that the best place among the three cities presented to open a coffe shop is Guadalajara; followed by Monterrey and Mexico City.

On possible improvement would be to extend this same analysis to other cities in Mexico, which may be more or less better options depending on the variables taking into consideration.

Another aspect to work upon would be to explore the robustness of the statistics/indicator used in this project to asses the best city.

# Conclusion

This is just an example of the many possibilities that rapid location data reach can be used for. Combinig this with data found elsewhere online results in a array of possibilities that was just beginning to be considered in this work. Further research involving new cities or dimensions can be intereseting and enlightening.


```python

```
