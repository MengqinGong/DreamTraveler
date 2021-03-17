

## Analysis on San Francisco Airbnb Open Data
#### What's in this folder?
- **sf**: contains data files: listings.csv, neighbourhoods.csv and neighbourhoods.geojson
- **Capstone_Project_1_Report.pdf**: final report
- **Capstone_Project_1_slides.pdf**: slides
- **Data_Story.ipynb**: code of exploratory data analysis (EDA) visualization part
- **Data_Wrangling.ipynb**: code of data cleaning and wrangling part
- **Inferential_Statistics.ipynb**: code of EDA inferential statistics part
- **Deep_Analysis.ipynb**: code of modeling part
- **listing_count_map.html**: map of San Francisco with listing counts in each neighbourhood
- **listings_clean.csv**: cleaned data after data cleaning and wrangling
- **median_price_map.html**: map of San Francisco with median listing price in each neighbourhood

### About This Project
#### Problem

Thanks to Airbnb, people now have more choices of accommodation when they travel to another city or a foreign country. Airbnb provides travellers with the opportunity to stay in a unique home and to deeply experience the local life. This analysis focuses on one of the most important aspects of an Airbnb listing - the price. I’m going to build a model that can predict the price of a listing in San Francisco based on its location, amenities, reviews and any other information that may apply.

Travellers who are planning a trip to San Francisco and Airbnb hosts in San Francisco will be interested in this analysis. Possible application of this analysis can be: finding the best price of a listing in a neighborhood and setting price based on the details of the listing.

#### Data

The data I used is from [insideairbnb.com](http://insideairbnb.com/get-the-data.html). The dataset ‘listings’ contains the detailed information of 7151 listings in San Francisco area on Airbnb, including location, host info, amenities, property type etc. (7151 records with 106 columns in total).

#### Conclusion

The number of new Airbnb listings in the SF market might depends on the home price in that area. A booming market of Airbnb may associated with a recession in home market.

Superhosts earn more than regular hosts because they have more bookings instead of higher price!

Listing features play an important role in deciding the price. The location/neighborhood, size, property type, and room type are all factors that have effects. Cleaning fee is excluded from nightly price, but is positively correlated with list price, so be prepared to pay high cleaning fee for an expensive stay!

Review score is positively correlated with price and number of reviews is negatively correlated with price. That means, people are more likely to book low price listings but they may have more fun with a higher priced listing.

A Random Forest Regressor was selected as the best predictive model for this dataset, the following graph shows the feature importance and the corresponding standard deviation of the Random Forest model:

![](https://lh4.googleusercontent.com/2-2HMUliWw0grtK3WYlShuKIuH9TdZjUj9C70YEXynJWjv7qBupvUIAfr1zOv4OKj2SfzseUwsIbRj6tsjVlFebNMOgZBJkobR4l9bdoDz2eUaedTTmm575LcInks7ZPXNPMwrPr)

The top 5 features are number of bedrooms, number of people the listing can accommodate, number of bathrooms, number of beds, and type of the room. So we can conclude that the size and capacity of a listing play the most important role in pricing, other features such as number of reviews, number of listings a host has (may be an indicator of if the host is experienced) and number of guests included also contribute to the price of a listing.

