# As potential Airbnb hosts, what factors should we look out for to maximise the chance of a higher review rating for the apartment?
![Singapore](singapore.png)

### Contributors:
* Yeo Boon Hao
* Teo Jun Wei
* Lim Zi Hao
</n>


Our project is based of the Singapore airbnb dataset found on [insideairbnb](http://insideairbnb.com/get-the-data)

## Motivation 
- When people shop online or look for a hotel to stay at, they will turn to the reviews section for reference.
  - Reviews made by past customers are usually deemed to be reliable, and a reflection of their satisfaction level.
  - As such, this guides their decision.
  
- Additionally, with the covid situation easing up
  - More travellers are able to visit Singapore
  - A good opportunity to start generating revenue through airbnb
 
 ## Dataset
 
|variable|dtype||variable|dtype|
|---|---|---|---|---|
|id|int||amenities|json|
|listing_url|string||price|string|
|scrape_id|string||minimum_nights|int|
|last_scraped|datetime||maximum_nights|int|
|name|string||minimum_minimum_nights|int|
|description|string||maximum_minimum_nights|int|
|neighborhood_overview|string||minimum_maximum_nights|int|
|picture_url|string||maximum_maximum_nights|int|
|host_id|int||minimum_nights_avg_ntm|int|
|host_url|string||maximum_nights_avg_ntm|int|
|host_since|date||calendar_updated|date|
|host_location|string||has_availability|boolean|
|host_about|string||availability_30|int|
|host_response_time|string||availability_60|int|
|host_response_rate|string||availability_90|int|
|host_acceptance_rate|string||availability_365|int|
|host_is_superhost|boolean||calendar_last_scraped|date|
|host_thumbnail_url|string||number_of_reviews|int|
|host_picture_url|string||number_of_reviews_ltm|int|
|host_neighbourhood|string||number_of_reviews_l30d|int|
|host_listings_count|string||first_review|date|
|host_total_listings_count|string||last_review|date|
|host_verifications|json||review_scores_rating|float|
|host_has_profile_pic|boolean||review_scores_accuracy|float|
|host_identity_verified|boolean||review_scores_cleanliness|float|
|neighbourhood|string||review_scores_checkin|float|
|neighbourhood_cleansed|string||review_scores_communication|float|
|latitude|float||review_scores_location|float|
|longitude|float||review_scores_value|float|
|property_type|string||license|string|
|room_type|string||instant_bookable|boolean|
|accommodates|int||calculated_host_listings_count|int|
|bathrooms|float||calculated_host_listings_count_entire_homes|int|
|bathrooms_text|string||calculated_host_listings_count_private_rooms|int|
|bedrooms|int||calculated_host_listings_count_shared_rooms|int|
|beds|int||reviews_per_month|float|

 ## Getting Started
 
 ### Installing required packages

```
pip install folium
pip install wordcloud
```

### Data cleaning

- Removed NaN Values
- Remove unwanted symbols like [ ] “” /  and converted the some unicode to ASCII
- Rounded the number to 1.dp to generalize the ratings 
- Removed the $ sign from the price string and converted to float
