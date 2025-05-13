
# 🍽️ **CityBites – Product Backlog**

---

## 🧩 EPIC 1: Restaurant Discovery (Core Search & Browse)

---

### **User Story 1.1: Search by City or Location**

**As a** user
**I want** to search for restaurants by city or use my current location
**So that** I can find restaurants relevant to where I am or where I’m going

**Acceptance Criteria:**

* User can type in a city name
* User can allow GPS-based location
* Restaurant list updates accordingly

---

### **User Story 1.2: Filter Restaurants**

**As a** user
**I want** to filter restaurants by cuisine, price, rating, and dietary tags
**So that** I can narrow results to match my preferences

**Acceptance Criteria:**

* Filter by cuisine type (multi-select)
* Filter by price range (\$–\$\$\$\$)
* Filter by minimum rating
* Filter by tags: vegan, gluten-free, etc.

---

### **User Story 1.3: View Restaurant List**

**As a** user
**I want** to view a scrollable list of restaurants
**So that** I can compare multiple places at a glance

**Acceptance Criteria:**

* Show name, image, rating, cuisine, location snippet
* Infinite scroll or pagination
* Sort options: rating, distance, popularity

---

### **User Story 1.4: View Restaurant Detail Page**

**As a** user
**I want** to see detailed info about a restaurant
**So that** I can decide whether I want to eat there

**Acceptance Criteria:**

* Photos, menu (PDF or embedded), full address/map
* Ratings breakdown and reviews
* Hours, website, and contact info

---

## 📝 EPIC 2: User Accounts & Profiles

---

### **User Story 2.1: User Registration and Login**

**As a** new user
**I want** to sign up with email or Google
**So that** I can save favorites and write reviews

**Acceptance Criteria:**

* Email/password signup or OAuth login
* JWT token authentication
* Password reset functionality

---

### **User Story 2.2: View/Edit Profile**

**As a** user
**I want** to update my profile
**So that** I can personalize my presence

**Acceptance Criteria:**

* View profile page with bio, photo, lists
* Edit profile settings

---

## ⭐ EPIC 3: Reviews and Ratings

---

### **User Story 3.1: Submit Review**

**As a** user
**I want** to rate and review a restaurant
**So that** I can share my experience with others

**Acceptance Criteria:**

* 1–5 star rating input
* Optional detailed ratings (food, service, ambiance)
* Write text review and upload photos

---

### **User Story 3.2: View Reviews**

**As a** user
**I want** to read other people’s reviews
**So that** I can make informed choices

**Acceptance Criteria:**

* Display reviews in chronological or helpfulness order
* Show reviewer name, avatar, and date

---

### **User Story 3.3: Upvote Reviews**

**As a** user
**I want** to mark helpful reviews
**So that** the best ones rise to the top

**Acceptance Criteria:**

* Show vote count
* Upvote only once per review

---

## 📚 EPIC 4: Lists and Favorites

---

### **User Story 4.1: Save to Favorites**

**As a** user
**I want** to favorite restaurants
**So that** I can remember them for later

**Acceptance Criteria:**

* Add/remove from favorites on list or detail page
* View all favorites in user profile

---

### **User Story 4.2: Create Custom Lists**

**As a** user
**I want** to make lists of restaurants (e.g., "Best Tacos")
**So that** I can organize places my way

**Acceptance Criteria:**

* Title and description fields
* Add restaurants to lists from detail page
* Shareable public/private list setting

---

## 🔍 EPIC 5: Smart Recommendations

---

### **User Story 5.1: Personalized Suggestions**

**As a** returning user
**I want** to get recommendations
**So that** I can discover new places I’ll likely enjoy

**Acceptance Criteria:**

* Based on previous reviews, favorites, cuisine preferences
* Display "Recommended For You" section on homepage

---

### **User Story 5.2: Top 10 & Hidden Gems**

**As a** user
**I want** to see city-specific lists
**So that** I can find the best or underrated spots

**Acceptance Criteria:**

* Static or AI-generated "Top 10" and "Hidden Gems"
* Updated periodically or based on user engagement

---

## 💬 EPIC 6: Social & Community

---

### **User Story 6.1: Follow Users**

**As a** user
**I want** to follow other users or influencers
**So that** I can discover places through people I trust

**Acceptance Criteria:**

* Follow/unfollow button
* See their public lists and reviews

---

### **User Story 6.2: See Where Friends Have Been**

**As a** user
**I want** to see which places my friends reviewed
**So that** I can get trusted recommendations

**Acceptance Criteria:**

* Show recent friend check-ins or reviews
* “Friend favorites” section on restaurant pages

---

## 🔒 EPIC 7: Admin & Moderation

---

### **User Story 7.1: Admin Dashboard**

**As an** admin
**I want** to view and manage restaurant data and reports
**So that** I can keep the platform clean and accurate

**Acceptance Criteria:**

* List all restaurants, reviews, and users
* Edit/delete reviews or flag inappropriate content

---

### **User Story 7.2: Restaurant Verification**

**As an** admin
**I want** to verify legitimate restaurant pages
**So that** users can trust the info

**Acceptance Criteria:**

* Toggle `is_verified` status
* Upload logos, menus, or correct hours

---

## 🚀 EPIC 8: Infrastructure & DevOps

---

### **User Story 8.1: Deployment Pipeline**

**As a** dev
**I want** CI/CD for frontend and backend
**So that** changes can be tested and deployed efficiently

**Acceptance Criteria:**

* GitHub Actions or Vercel/Netlify for frontend
* Dockerized backend + DB migrations

---

### **User Story 8.2: API Rate Limiting & Caching**

**As a** backend engineer
**I want** to cache frequent queries and limit abuse
**So that** the app scales reliably

**Acceptance Criteria:**

* Use Redis for caching
* Apply rate limits on API endpoints

---

## 🧪 EPIC 9: Testing

---

### **User Story 9.1: Unit and Integration Tests**

**As a** developer
**I want** automated tests
**So that** I can prevent regressions

**Acceptance Criteria:**

* Jest (frontend), Mocha/Chai or Supertest (backend)
* API endpoint coverage > 80%

---

### **User Story 9.2: Manual QA Testing**

**As a** QA tester
**I want** to manually test the full flow
**So that** we ensure a smooth user experience

**Acceptance Criteria:**

* Clickthrough test cases for signup, search, filters, reviews
* Bug report checklist

---

### ✅ MVP Tag Summary

To build the MVP, **prioritize:**

* Epics: 1, 2, 3, 4
* User Stories: 1.1 → 1.4, 2.1, 3.1 → 3.2, 4.1

---
