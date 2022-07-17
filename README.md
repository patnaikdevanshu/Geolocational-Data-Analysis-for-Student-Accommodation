# Geolocational-Data-Analysis-for-Student-Accommodation
Exploratory Analysis of Geolocational Data
This project involves the use of K-Means Clustering to find the best accommodation for students in KIIT University by classifying accommodation for incoming students on the basis of their preferences on amenities, budget and proximity to the location.
## Workflow
![image](https://user-images.githubusercontent.com/71730642/179419251-5948ee9c-0189-4fdc-be30-fee7975613b9.png)

- The food_choices file from this link is used as data-set to differentiate among students.
- Suitable parameters are chosen to perform data cleaning. The cleaned data is visualized using Box-plots.
- K-Means clustering is applied on cleaned data for arbitrary values of K and best value of K is found.
![image](https://user-images.githubusercontent.com/71730642/179419167-bcaef46a-a976-48c7-b147-2301983b1622.png)

- **High income students:** In general they pay more on meal out, eat less fruits, mostly stay on campus, exercise more, cook less.
- **Low income students:** In general they pay less on meal out, eat more fruits, more likely to stay away from campus, exercise less, cook more often.
However the boundaries of these classifications are not very prominent.

-  Now we use real time data from REST API (HERE Geo coding API) for any college (KIIT University, Bhubaneshwar in this case) to find accommodation for students around the area.

Useful parameters are selected an data cleaning is performed on this data. This data is now clustered using optimal K
![image](https://user-images.githubusercontent.com/71730642/179419215-d8a14426-6ed8-4e56-9c3a-5d809eddb66a.png)

- Using Folium, the above clustered data is plotted on map
![image](https://user-images.githubusercontent.com/71730642/179419247-24c2b312-748e-4afa-86bc-8abd9f3944a9.png)

## By Observation
- **Cluster 0** (Green): has almost equal number of shops and restaurants but very few gyms
- **Cluster 1** (Blue):  has the minimum no. of shops, restaurants and gyms in  total
- **Cluster 2** (Orange): has the maximum no. of shops, restaurants and gyms in total
- **Cluster 3** (Red): has more shops and stores and comparitively lesser no. of restaurants and fewer gyms
