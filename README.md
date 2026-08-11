# LostFound+ – Lost and Found Management Platform

Full-stack MERN hackathon project with:
- JWT authentication and role-based access (user/moderator/admin)
- Lost/found item CRUD
- Image uploads (local by default; optional Cloudinary)
- Advanced search and filtering
- Smart matching score using category/location/date/description
- Ownership claims with verification answers
- Admin moderation dashboard
- Trust score
- MongoDB aggregation statistics

## Requirements
- Node.js 20+
- MongoDB 6+ (local or Atlas)

## Run
1. `cd server && npm install`
2. Copy `.env.example` to `.env` and set `MONGO_URI` and `JWT_SECRET`.
3. `npm run dev`
4. In another terminal: `cd client && npm install && npm run dev`
5. Open the URL shown by Vite (normally http://localhost:5173).

The server serves uploaded local images from `/uploads`. Cloudinary is optional; set all Cloudinary variables to enable it.

## Demo accounts
Run `cd server && npm run seed` after configuring MongoDB.
- Admin: admin@lostfound.local / Admin@123
- User: user@lostfound.local / User@123

## API
Base URL: `http://localhost:5000/api`
- POST `/auth/register`
- POST `/auth/login`
- GET `/items`
- POST `/items`
- GET `/items/:id`
- PATCH `/items/:id`
- DELETE `/items/:id`
- GET `/items/:id/matches`
- POST `/claims`
- GET `/claims/mine`
- PATCH `/claims/:id/review` (moderator/admin)
- GET `/admin/stats` (admin/moderator)
- GET `/admin/items/pending` (admin/moderator)
- PATCH `/admin/items/:id/status` (admin/moderator)

