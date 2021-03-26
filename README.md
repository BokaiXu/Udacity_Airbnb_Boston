Libraries Used:
Pandas, Numpy, Scikit-learn, Matplotlib, Seaborn, Tensorflow

Motivation:
This project analyze the airbnb house price on Boston(https://www.kaggle.com/airbnb/boston) and use the data to make a model to predict the price of house rental around the Boston area.

Files:
calendar.csv: data with the house price.
listings.csv: detailed info about each house.
reviews.csv: reviews about each house.
Boston_Airbnb_Open_Data.ipynb: Jupyter notebook with the exploratory data analysis of the data sets and the neural net work used to predict the price of house rental in Boston area.

Summary of results: This analysis shows September is the most popular month to visit Boston while February is the worst. Also the price of house rental in Boston was influenced by a lot of factors such as neighbourhood, number of bedrooms, etc. A model was build based on the info of the listings data set and used to predict the price of house rental around Boston area.
Business Understanding:
This data set contains the airbnb info in Boston. The listings table includes ~4000 info of houses in the Boston area. It contians the location, house type, price,etc.
This data could be used to build the model to predict the price of house rental around Boston.

Data Understanding:
The listings table contains 94 columns. ('id', 'listing_url', 'scrape_id', 'last_scraped', 'name', 'summary',
       'space', 'description', 'experiences_offered', 'neighborhood_overview',
       'notes', 'transit', 'access', 'interaction', 'house_rules',
       'thumbnail_url', 'medium_url', 'picture_url', 'xl_picture_url',
       'host_id', 'host_url', 'host_name', 'host_since', 'host_location',
       'host_about', 'host_response_time', 'host_response_rate',
       'host_acceptance_rate', 'host_is_superhost', 'host_thumbnail_url',
       'host_picture_url', 'host_neighbourhood', 'host_listings_count',
       'host_total_listings_count', 'host_verifications',
       'host_has_profile_pic', 'host_identity_verified', 'street',
       'neighbourhood', 'neighbourhood_cleansed',
       'neighbourhood_group_cleansed', 'city', 'state', 'zipcode', 'market',
       'smart_location', 'country_code', 'country', 'latitude', 'longitude',
       'is_location_exact', 'property_type', 'room_type', 'accommodates',
       'bathrooms', 'bedrooms', 'beds', 'bed_type', 'amenities', 'square_feet',
       'price', 'weekly_price', 'monthly_price', 'security_deposit',
       'cleaning_fee', 'guests_included', 'extra_people', 'minimum_nights',
       'maximum_nights', 'calendar_updated', 'has_availability',
       'availability_30', 'availability_60', 'availability_90',
       'availability_365', 'calendar_last_scraped', 'number_of_reviews',
       'first_review', 'last_review', 'review_scores_rating',
       'review_scores_accuracy', 'review_scores_cleanliness',
       'review_scores_checkin', 'review_scores_communication',
       'review_scores_location', 'review_scores_value', 'requires_license',
       'license', 'jurisdiction_names', 'instant_bookable',
       'cancellation_policy', 'require_guest_profile_picture',
       'require_guest_phone_verification', 'calculated_host_listings_count',
       'reviews_per_month')
Most of the columns are not easy to be understood and are difficult to used in modeling. Also missing values need to be fixed.

Prepare Data:
Columns unrelated or not directly related with price was dropped. Category variables were converted to dummy varialbes. Rows with missing values were dropped.

Data Modeling:
A simple dense neural network was built based on the cleaned data of listings. ~67% of the data was used to build the model and the rest of the data was used to calculate the MSE.

Evaluate the Results:
MSE(mean suqare error) was used to evaluate the model. The MSE is 4443, the RMSE(root mean square error) is 67. This is a very large value since the range of price is in between 0 to 600.
Maybe we should use a Linear regression or try to assemble more data to fit the neural network.
