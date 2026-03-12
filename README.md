# 🚀 MERN Stack Projects - All 8 Applications Built!

Welcome! This repository contains 8 complete web applications built with the MERN stack (MongoDB, Express, React, Node.js) + TypeScript.

---

## 🚀 Quick Start with Docker Compose

### Start All Applications
```bash
# Start all 8 apps + MongoDB + PostgreSQL
docker-compose up -d

# View logs
docker-compose logs -f

# Stop all
docker-compose down
```

### Start Individual App
Each app has its own `docker-compose.yml` file:
```bash
cd apps/todo-app
docker-compose up -d
```

---

## 📁 Projects Overview

| # | Project | Backend Port | Frontend Port | URL |
|---|---------|--------------|---------------|-----|
| 1 | **Blog Platform** | 5005 | 5173 | http://localhost:5173 |
| 2 | **Calendar App** | 5002 | 5174 | http://localhost:5174 |
| 3 | **Code Snippets** | 5003 | 5175 | http://localhost:5175 |
| 4 | **Music Playlist** | 5007 | 5176 | http://localhost:5176 |
| 5 | **News Aggregator** | 5001 | 5177 | http://localhost:5177 |
| 6 | **Real Estate** | 5006 | 5178 | http://localhost:5178 |
| 7 | **Todo App** | 5000 | 5179 | http://localhost:5179 |
| 8 | **Weather App** | 5004 | 5180 | http://localhost:5180 |

---

## 📖 Project Details

### 1. Blog Platform `/apps/blog-platform`
**Features**: Article CRUD, markdown support, comments, likes, tags, author profiles

**Run**: `cd apps/blog-platform && docker-compose up -d`
**Access**: http://localhost:5173

---

### 2. Calendar App `/apps/calendar-app`
**Features**: Monthly/weekly/daily views, event CRUD, single/multi-day events, reminders, color-coded categories

**Run**: `cd apps/calendar-app && docker-compose up -d`
**Access**: http://localhost:5174

---

### 3. Code Snippet Repository `/apps/code-snippets`
**Features**: Create/edit/delete code snippets, syntax highlighting, language filtering, rating system, fork snippets

**Run**: `cd apps/code-snippets && docker-compose up -d`
**Access**: http://localhost:5175

---

### 4. Music Playlist App `/apps/music-playlist`
**Features**: Create playlists, manage songs, music player controls, search functionality

**Run**: `cd apps/music-playlist && docker-compose up -d`
**Access**: http://localhost:5176

---

### 5. News Aggregator `/apps/news-aggregator`
**Features**: Real-time news, category filtering, search, bookmarks, saved searches

**Run**: `cd apps/news-aggregator && docker-compose up -d`
**Access**: http://localhost:5177

**Note**: Add `NEWS_API_KEY` to `.env` for real news (get free at https://newsapi.org/)

---

### 6. Real Estate Listings `/apps/real-estate`
**Features**: Property listings, add/edit/delete properties, advanced filtering, property details

**Run**: `cd apps/real-estate && docker-compose up -d`
**Access**: http://localhost:5178

---

### 7. Todo App `/apps/todo-app`
**Features**: Task CRUD, categories, subtasks, tags, smart lists, reminders, dark/light theme

**Run**: `cd apps/todo-app && docker-compose up -d`
**Access**: http://localhost:5179

---

### 8. Weather App `/apps/weather-app`
**Features**: Current weather, search by city, temperature, humidity, wind speed, modern UI

**Run**: `cd apps/weather-app && docker-compose up -d`
**Access**: http://localhost:5180

**Note**: Add `OPENWEATHER_API_KEY` to `.env` for live weather data (get free at https://openweathermap.org/)

---

## 🔧 Tech Stack

- **Frontend**: React 19, TypeScript, Vite, Tailwind CSS v4, Lucide React icons
- **Backend**: Node.js, Express, TypeScript, MongoDB with Mongoose
- **Authentication**: JWT with bcrypt (demo mode enabled)
- **API Design**: RESTful with consistent response format
- **DevOps**: Docker, Docker Compose

---

## 📦 Project Structure

```
/home/nobab/Documents/hbprojects/
├── apps/
│   ├── blog-platform/      ✅ Complete
│   ├── calendar-app/       ✅ Complete
│   ├── code-snippets/      ✅ Complete
│   ├── music-playlist/     ✅ Complete
│   ├── news-aggregator/    ✅ Complete
│   ├── real-estate/        ✅ Complete
│   ├── todo-app/           ✅ Complete
│   └── weather-app/        ✅ Complete
├── docker-compose.yml      (Run all apps)
└── README.md
```

---

## 🎯 Key Features

- ✅ **8 full-stack web applications** built from scratch
- ✅ **Docker Compose** for easy deployment
- ✅ **MongoDB + PostgreSQL** databases
- ✅ **RESTful APIs** with consistent response formats
- ✅ **TypeScript** for type safety
- ✅ **Responsive designs** with Tailwind CSS v4
- ✅ **Modern UI** with glassmorphism and gradients
- ✅ **Dark mode support**
- ✅ **Real-time features** (news, weather, calendar)

---

## 📝 Environment Variables

Create `.env` files in each app's server directory:

**News Aggregator**:
```
NEWS_API_KEY=your_key_here
MONGODB_URI=mongodb://mongodb:27017/news-aggregator
PORT=5001
```

**Weather App**:
```
OPENWEATHER_API_KEY=your_key_here
MONGODB_URI=mongodb://mongodb:27017/weather-app
PORT=5004
```

---

## 🚀 Quick Commands

```bash
# Start all apps
docker-compose up -d

# View logs for all apps
docker-compose logs -f

# View logs for specific app
docker-compose logs -f blog-app-client

# Stop all apps
docker-compose down

# Restart specific app
docker restart blog-app-client

# Check all running containers
docker ps
```

---

Built with ❤️ using MERN stack + TypeScript + Tailwind CSS + Docker
