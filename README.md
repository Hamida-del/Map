# Map
Map
Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@Hamida-del 
Learn Git and GitHub without any code!
Using the Hello World guide, you’ll start a branch, write comments, and open a pull request.


Krysek
/
Coursera-Data-Science-Specialization-Developing-Data-Products-Week-2-Assignment
1
033
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
Coursera-Data-Science-Specialization-Developing-Data-Products-Week-2-Assignment/My First Leaflet Map.Rmd
@Krysek
Krysek Including link to GitHub.
Latest commit 09799b4 on 6 Jul 2017
 History
 1 contributor
36 lines (31 sloc)  1.3 KB
  
---
title: "My First Leaflet Map"
author: "Christian Frei"
date: "6 July 2017"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
The source code is available at [GitHub](https://github.com/Krysek/Coursera-Data-Science-Specialization-Developing-Data-Products-Week-2-Assignment). [Just click here!](https://github.com/Krysek/Coursera-Data-Science-Specialization-Developing-Data-Products-Week-2-Assignment)

## My First Leaflet Map
Create a leaflet map object.
```{r cars}
library(leaflet)
map <- leaflet() %>% addTiles()
```

Create a marker with a picture of Benrath Palace and a link to its homepage.
```{r}
benrathPalaceIcon <- makeIcon(
   iconUrl = "http://www.schloss-benrath.de/fileadmin/_processed_/csm_corps-de-logis-blumen_2e04b2b859.jpg",
   iconWidth = 30*408/255, iconHeight = 30,
   iconAnchorX = 30*408/255/2, iconAnchorY = 30/2
)
```

Add the marker to the map and display the map.
```{r}
benrathPalacePopup <- c("<a href= 'http://www.schloss-benrath.de/welcome/?L=1' >Benrath Palace<br><img src='http://www.schloss-benrath.de/fileadmin/_processed_/csm_corps-de-logis-blumen_2e04b2b859.jpg' width='210' height='132'  alt='Foto Corps de Logis' title='Foto Corps de Logi'></a>")
map %>%
   addTiles() %>%
   addMarkers(lat=51.161027, lng=6.870550, popup = benrathPalacePopup)
```
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
