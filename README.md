# 🧠 MERN ThinkBoard

A full-stack notes application built with the MERN stack. ThinkBoard lets users create, view, edit, and delete notes through a responsive React interface backed by an Express and MongoDB API.

<p align="center">
  <a href="https://mern-thinkboard-bwcb.onrender.com"><strong>🚀 Live Application</strong></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/SahilMujawar-19265/mern-thinkboard"><strong>💻 Source Code</strong></a>
</p>

## ✨ Features

- 📝 Create notes with a title and content
- 📚 View all notes on the home page
- ✏️ Open and edit individual notes
- 🗑️ Delete notes
- 📱 Responsive Tailwind CSS and daisyUI interface
- 🚦 Upstash Redis rate limiting
- 💾 MongoDB persistence with Mongoose
- 🌐 Production mode for serving the built frontend from Express

## 🛠️ Tech Stack

- 🎨 **Frontend:** React, Vite, React Router, Axios, Tailwind CSS, daisyUI
- ⚙️ **Backend:** Node.js, Express, Mongoose, MongoDB
- ☁️ **Additional Services:** Upstash Redis

## 📂 Project Structure

```text
mern-thinkboard/
├── backend/
│   ├── src/
│   │   ├── config/       # MongoDB and Upstash configuration
│   │   ├── controllers/  # Notes business logic
│   │   ├── middleware/   # Request rate limiting
│   │   ├── models/       # Mongoose models
│   │   ├── routes/       # Express routes
│   │   └── server.js     # Application entry point
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/   # Reusable React components
│   │   ├── lib/          # Frontend utilities
│   │   ├── pages/        # Application pages
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
└── package.json
```

## ✅ Prerequisites

- 📦 Node.js 18 or newer
- 📦 npm
- 🍃 A MongoDB database
- ⚡ An Upstash Redis database

## 🔐 Environment Variables

Create a `.env` file in `backend/` with:

```env
MONGODB_URI=your_mongodb_connection_string
UPSTASH_REDIS_REST_URL=your_upstash_redis_rest_url
UPSTASH_REDIS_REST_TOKEN=your_upstash_redis_rest_token
PORT=5001
NODE_ENV=development
```

The `PORT` and `NODE_ENV` variables are optional. The server uses port `5001` by default and enables CORS for `http://localhost:5173` outside production.

## 📥 Installation

Clone the repository:

```bash
git clone https://github.com/SahilMujawar-19265/mern-thinkboard.git
cd mern-thinkboard
```

Install dependencies for both applications:

```bash
npm install --prefix backend
npm install --prefix frontend
```

## ▶️ Running Locally

Start the backend:

```bash
npm run dev --prefix backend
```

In a separate terminal, start the frontend:

```bash
npm run dev --prefix frontend
```

Open `http://localhost:5173` in your browser. The API is available at `http://localhost:5001/api/notes`.

## 🔌 API Routes

All note routes are prefixed with `/api/notes`.

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/notes` | 📚 Get all notes |
| `GET` | `/api/notes/:id` | 🔎 Get a note by ID |
| `POST` | `/api/notes` | 📝 Create a note |
| `PUT` | `/api/notes/:id` | ✏️ Update a note |
| `DELETE` | `/api/notes/:id` | 🗑️ Delete a note |

## 🏗️ Production Build

From the repository root, build the frontend and start the application:

```bash
npm run build
npm start
```

Set `NODE_ENV=production` and ensure MongoDB and Upstash environment variables are configured. The Express server will serve the frontend from `frontend/dist`.

## 📜 Available Scripts

### Root

- 🏗️ `npm run build` - Install all dependencies and build the frontend
- ▶️ `npm start` - Start the backend server

### Backend

- 🔄 `npm run dev --prefix backend` - Start with Nodemon
- ▶️ `npm start --prefix backend` - Start the server with Node.js

### Frontend

- ⚡ `npm run dev --prefix frontend` - Start the Vite development server
- 🏗️ `npm run build --prefix frontend` - Build for production
- 🔍 `npm run lint --prefix frontend` - Run ESLint
- 👀 `npm run preview --prefix frontend` - Preview the production build

## 📄 License

ISC
