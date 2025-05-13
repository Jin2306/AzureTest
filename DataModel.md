**Table: Users**

- id: UUID (Primary Key)
- name: VARCHAR
- email: VARCHAR (Unique)
- password_hash: TEXT
- profile_photo_url: TEXT (optional)
- bio: TEXT (optional)
- role: ENUM ('visitor', 'registered', 'influencer', 'admin')
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

**Table: Restaurants**

- id: UUID (Primary Key)
- name: VARCHAR
- address: TEXT
- city: VARCHAR
- state: VARCHAR
- country: VARCHAR
- latitude: FLOAT
- longitude: FLOAT
- phone_number: VARCHAR
- website_url: TEXT
- price_range: INT (1 to 4)
- is_verified: BOOLEAN
- created_at: TIMESTAMP
- updated_at: TIMESTAMP
- 
**Table: Reviews**

- id: UUID (Primary Key)
- user_id: UUID (Foreign Key → Users.id)
- restaurant_id: UUID (Foreign Key → Restaurants.id)
- rating: INT (1–5)
- food_rating: INT (1–5)
- service_rating: INT (1–5)
- ambiance_rating: INT (1–5)
- review_text: TEXT
- review_photos: JSON[] (Array of image URLs)
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

**Table: Cuisine_Types**

- id: UUID (Primary Key)
- name: VARCHAR (e.g., "Korean", "French")

**Table: Restaurant_Cuisines**  
(Many-to-Many relationship)

- restaurant_id: UUID (Foreign Key → Restaurants.id)
- cuisine_id: UUID (Foreign Key → Cuisine_Types.id)

**Table: Favorites**

- user_id: UUID (Foreign Key → Users.id)
- restaurant_id: UUID (Foreign Key → Restaurants.id)
- created_at: TIMESTAMP

**Table: Lists**  
(User-created collections of restaurants)

- id: UUID (Primary Key)
- user_id: UUID (Foreign Key → Users.id)
- title: VARCHAR
- is_public: BOOLEAN
- created_at: TIMESTAMP

- **Table: List_Restaurants**  
(Many-to-Many relationship)

- list_id: UUID (Foreign Key → Lists.id)
- restaurant_id: UUID (Foreign Key → Restaurants.id)

**Table: Photos**

- id: UUID (Primary Key)
- user_id: UUID (Foreign Key → Users.id)
- restaurant_id: UUID (Foreign Key → Restaurants.id)
- image_url: TEXT
- caption: TEXT
- created_at: TIMESTAMP

**Table: Check_Ins**

- id: UUID (Primary Key)
- user_id: UUID (Foreign Key → Users.id)
- restaurant_id: UUID (Foreign Key → Restaurants.id)
- timestamp: TIMESTAMP

**Table: Deals**

- id: UUID (Primary Key)
- restaurant_id: UUID (Foreign Key → Restaurants.id)
- title: VARCHAR
- description: TEXT
- start_date: DATE
- end_date: DATE



