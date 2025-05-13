

## 🏁 1-Hour Sprint Plan: MVP Prototype (Read-Only Demo)

**🎯 Sprint Goal:**
Build a basic full-stack prototype that:

* Runs locally
* Displays a list of restaurants
* Pulls restaurant data from a backend API
* Is styled simply for demo purposes

---

### 📦 Deliverables

* A working React frontend that lists restaurants
* A simple Node.js/Express backend that serves static restaurant data via REST API
* JSON file or in-memory array as the mock database
* Basic styling (e.g., using Tailwind or inline CSS)

---

### 🧩 Breakdown (60 minutes total)

| Time          | Task                             | Description                                                                                                                                                |
| ------------- | -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **0–5 min**   | **Project Setup**                | - Create folder structure<br>- Initialize Git repo<br>- Create frontend and backend folders                                                                |
| **5–15 min**  | **Backend API (Node + Express)** | - Setup basic Express server<br>- Create endpoint `GET /api/restaurants`<br>- Return 5–10 sample restaurants as JSON                                       |
| **15–30 min** | **Frontend Setup (React)**       | - Create a basic React app (`Vite` recommended for speed)<br>- Install Axios or Fetch wrapper<br>- Build UI component to fetch and display restaurant list |
| **30–45 min** | **Connect Frontend to Backend**  | - Call API endpoint from React<br>- Render data: name, rating, cuisine, address                                                                            |
| **45–55 min** | **Style the Output**             | - Add basic styling (e.g., card format)<br>- Ensure it’s mobile-friendly and readable                                                                      |
| **55–60 min** | **Test & Polish**                | - Quick testing<br>- Fix any visible bugs<br>- Push to GitHub<br>- Write quick README if time allows                                                       |

---

### 🛠 Sample Tech Stack

* **Frontend:** React + Vite
* **Backend:** Node.js + Express
* **Data Source:** Local JSON array
* **Communication:** REST (Axios or Fetch)
* **Styling:** Tailwind CSS or simple CSS

---

### 📁 Folder Structure

```
/citybites-sprint
├── backend
│   ├── index.js (Express app)
│   └── data.js (mock restaurant data)
├── frontend
│   ├── src/
│   └── vite.config.js
└── README.md
```

---

### 💡 Mock Data Example (backend/data.js)

```js
module.exports = [
  {
    id: 1,
    name: "Pho Heaven",
    rating: 4.7,
    cuisine: "Vietnamese",
    address: "123 Elm St, San Francisco, CA"
  },
  {
    id: 2,
    name: "La Pasta",
    rating: 4.5,
    cuisine: "Italian",
    address: "45 Mission St, San Francisco, CA"
  }
];
```

---

### ✅ Success Criteria

* Server returns JSON on `localhost:3000/api/restaurants`
* Frontend on `localhost:5173` loads the restaurant list
* Page displays restaurant name, rating, cuisine, and address
* No critical errors in console

--
