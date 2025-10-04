# MERN-BOOK-REVIEW-PLATFORM

## Setup

### Backend
cd backend
cp .env.example .env
# fill .env (MONGO_URI, JWT_SECRET)
npm install
npm run dev

### Frontend
cd frontend
npm install
npm start

## API
Base: /api
- POST /api/auth/signup {name,email,password}
- POST /api/auth/login {email,password} => returns { token, user }
- GET /api/books?page=1&limit=5
- POST /api/books (auth) => add book
- GET /api/books/:id => details + reviews
- PUT /api/books/:id (auth, owner)
- DELETE /api/books/:id (auth, owner)
- POST /api/reviews (auth) { bookId, rating, reviewText }
- DELETE /api/reviews/:id (auth)

## Notes
- Pagination: 5 books per page by default.
- Only the user who added a book can edit/delete it.
