# QuickTask

Simple and fast task tracker

## Features

✨ **Beautiful UI** - Modern, responsive design with smooth animations  
🎯 **Task Management** - Create, update, and track tasks with ease  
📊 **Priority Levels** - Low, Medium, High priority indicators  
📅 **Due Dates** - Never miss a deadline  
🔄 **Status Tracking** - Todo → In Progress → Done workflow  
⚡ **Turso Database** - Fast, serverless SQLite at the edge  

## Setup

### 1. Install Dependencies

```bash
npm install
```

### 2. Set up Turso Database

```bash
# Install Turso CLI (if not already installed)
curl -sSfL https://get.tur.so/install.sh | bash

# Login to Turso
turso auth login

# Create database
turso db create quicktask

# Get connection details
turso db show quicktask --url
turso db tokens create quicktask
```

### 3. Initialize Database Schema

```bash
# Apply schema
turso db shell quicktask < SCHEMA.sql
```

### 4. Configure Environment

Copy `.env.local.example` to `.env.local` and add your Turso credentials:

```env
TURSO_DATABASE_URL=libsql://your-db.turso.io
TURSO_AUTH_TOKEN=your-token-here
```

### 5. Run Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see your app!

## Tech Stack

- **Next.js 16** - React framework
- **TypeScript** - Type safety
- **Turso** - Serverless SQLite database
- **Tailwind CSS** - Styling
- **Framer Motion** - Animations
- **Headless UI** - Accessible components
- **Heroicons** - Icons

## Pricing

$15/month

---

Built with ❤️ by LaunchKit 🚀

Powered by [Turso](https://turso.tech) - The edge database
