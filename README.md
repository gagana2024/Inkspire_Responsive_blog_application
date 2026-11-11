# Inkspire — Full-Stack Blog Application

Frontend: HTML, CSS, JavaScript. Backend: Node.js, Express.js, MongoDB, JWT.

## Run it
1. Install Node.js and MongoDB (or create a MongoDB Atlas database).
2. Open a terminal inside `backend`.
3. Run `npm install`.
4. Copy `.env.example` to `.env`. Set `MONGO_URI` and replace `JWT_SECRET` with a long random secret.
5. Run `npm run dev`. Wait for the MongoDB connection success message.
6. Open the project root in VS Code and start Live Server on `index.html`.

## REST API
| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/api/auth/register` | Register user |
| POST | `/api/auth/login` | Login and receive JWT |
| GET | `/api/blogs` | List published blogs |
| POST | `/api/blogs` | Create blog (JWT required) |

Passwords are hashed with bcryptjs. Blog creation requires `Authorization: Bearer <token>`.
See `backend/README.md` for details and example request bodies.
