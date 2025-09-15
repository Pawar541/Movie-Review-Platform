# Movie Review Platform

## Overview
This is a full-stack Movie Review Platform built with:
- **Backend:** Node.js, Express, MongoDB (Mongoose)
- **Frontend:** React (Vite), React Router, Axios

Features:
- Browse movies, read and write reviews, and rate films
- User authentication (login/register)
- Watchlist functionality
- Review system with star ratings and text

---

## Project Structure
```
movie-review-platform/
├── backend/         # Express + MongoDB API
│   └── src/
│       ├── routes/
│       ├── models/
│       ├── middleware/
│       └── index.js
├── frontend/        # React frontend
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── context/
│       ├── services/
│       ├── App.jsx
│       └── main.jsx
└── README.md
```

---

## Setup Instructions

### 1. Clone or extract the project
```bash
unzip movie-review-platform.zip
cd movie-review-platform
```

### 2. Setup Backend
```bash
cd backend
npm install
npm start
```
The backend will start at `http://localhost:5000`.

Make sure MongoDB is running locally (`mongodb://localhost:27017/movies` by default).

### 3. Setup Frontend
```bash
cd frontend
npm install
npm run dev
```
The frontend will start at `http://localhost:5173`.

---

## Environment Variables

Create a `.env` file inside the **backend** folder with the following:
```
PORT=5000
MONGO_URI=mongodb://localhost:27017/movies
JWT_SECRET=your_jwt_secret
```

---

## API Endpoints

- `GET /movies` → Retrieve all movies (with pagination/filtering)
- `GET /movies/:id` → Retrieve a specific movie with reviews
- `POST /movies` → Add a new movie (admin only)
- `GET /movies/:id/reviews` → Retrieve reviews for a movie
- `POST /movies/:id/reviews` → Submit a review
- `GET /users/:id` → Get user profile + reviews
- `PUT /users/:id` → Update user profile
- `GET /users/:id/watchlist` → Get user watchlist
- `POST /users/:id/watchlist` → Add to watchlist
- `DELETE /users/:id/watchlist/:movieId` → Remove from watchlist

---

## Notes
- Ensure MongoDB is running before starting backend.
- Adjust ports or DB URI in `.env` if needed.
- Use Postman or Insomnia to test backend routes.

---

## Future Improvements
- TMDB API integration for posters & trailers
- Recommendation system
- Admin dashboard
- Real-time notifications for new reviews
