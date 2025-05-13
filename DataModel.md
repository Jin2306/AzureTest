🗂️ Entity-Relationship Data Model
1. Users
Field Name	Type	Description
id	UUID (PK)	Unique user ID
name	VARCHAR	User's name
email	VARCHAR (Unique)	Login email
password_hash	TEXT	Encrypted password
profile_photo_url	TEXT	Link to profile image
bio	TEXT	Optional bio
role	ENUM	visitor / registered / influencer / admin
created_at	TIMESTAMP	Account creation date
updated_at	TIMESTAMP	Last profile update

2. Restaurants
Field Name	Type	Description
id	UUID (PK)	Unique restaurant ID
name	VARCHAR	Restaurant name
address	TEXT	Full address
city	VARCHAR	City name
state	VARCHAR	State or province
country	VARCHAR	Country
latitude	FLOAT	GPS coordinate
longitude	FLOAT	GPS coordinate
phone_number	VARCHAR	Contact number
website_url	TEXT	Restaurant's official site
price_range	INT	1–4 dollar signs
is_verified	BOOLEAN	Verified listing
created_at	TIMESTAMP	When added
updated_at	TIMESTAMP	Last updated

3. Reviews
Field Name	Type	Description
id	UUID (PK)	Unique review ID
user_id	UUID (FK → Users)	Who wrote the review
restaurant_id	UUID (FK → Restaurants)	Reviewed restaurant
rating	INT (1–5)	Overall rating
food_rating	INT (1–5)	Optional sub-ratings
service_rating	INT (1–5)	
ambiance_rating	INT (1–5)	
review_text	TEXT	User’s review content
review_photos	JSON[]	Array of image URLs
created_at	TIMESTAMP	When the review was made
updated_at	TIMESTAMP	Edit timestamp

4. Cuisine_Types
Field Name	Type	Description
id	UUID (PK)	Cuisine ID
name	VARCHAR	e.g., "Mexican", "Korean BBQ"

5. Restaurant_Cuisines (Many-to-Many)
Field Name	Type	Description
restaurant_id	UUID (FK → Restaurants)	
cuisine_id	UUID (FK → Cuisine_Types)	

6. Favorites
Field Name	Type	Description
user_id	UUID (FK → Users)	Who favorited
restaurant_id	UUID (FK → Restaurants)	Favorite restaurant
created_at	TIMESTAMP	When the favorite was added

7. Lists (User-created restaurant collections)
Field Name	Type	Description
id	UUID (PK)	Unique list ID
user_id	UUID (FK → Users)	List creator
title	VARCHAR	e.g., "Date Night Spots in SF"
is_public	BOOLEAN	Public or private list
created_at	TIMESTAMP	

8. List_Restaurants (Many-to-Many)
Field Name	Type	Description
list_id	UUID (FK → Lists)	
restaurant_id	UUID (FK → Restaurants)	

9. Photos
Field Name	Type	Description
id	UUID (PK)	Image ID
user_id	UUID (FK → Users)	Uploaded by
restaurant_id	UUID (FK → Restaurants)	Related restaurant
image_url	TEXT	S3 or CDN-hosted link
caption	TEXT	Optional caption
created_at	TIMESTAMP	When uploaded

10. Check-Ins (Optional gamification feature)
Field Name	Type	Description
id	UUID (PK)	Check-in ID
user_id	UUID (FK → Users)	Who checked in
restaurant_id	UUID (FK → Restaurants)	Checked-in restaurant
timestamp	TIMESTAMP	Date and time

11. Deals (Optional / Future Phase)
Field Name	Type	Description
id	UUID (PK)	Deal ID
restaurant_id	UUID (FK → Restaurants)	Restaurant with the deal
title	VARCHAR	e.g., “Free dessert with meal”
description	TEXT	Full terms
start_date	DATE	
end_date	DATE	

Indexes and Performance Notes
Indexes on restaurant_id, user_id, and city are essential for speed.

Consider full-text search indexing on restaurant name, city, and review text.

Store average_rating and review_count in the Restaurants table (denormalized) to reduce query time.
