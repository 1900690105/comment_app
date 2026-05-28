# 🚀 React + Supabase Realtime App

A fullstack React application built with **Supabase** featuring:

- 💬 Comments System
- ❤️ Realtime Like Feature
- 🔒 Row Level Security (RLS)
- ☁️ Live PostgreSQL Database
- ⚡ Realtime Updates using Supabase Realtime

---

## 📌 Features

### ✅ Comments System
Users can:
- Add comments
- View comments dynamically
- Store comments in Supabase database

### ✅ Realtime Like Feature
Users can:
- Like posts
- See likes update instantly
- Experience realtime synchronization across tabs

### ✅ Supabase Realtime
Realtime subscriptions allow instant UI updates without page refresh.

### ✅ Row Level Security (RLS)
Implemented production-level security:

- Public users can **read comments**
- Public users can **add comments**
- Restricted update/delete access

---

## 🛠️ Tech Stack

### Frontend
- React.js
- Tailwind CSS

### Backend / Database
- Supabase
- PostgreSQL

### Deployment
- Vercel

---

## 📂 Project Structure

```bash
src/
│── components/
│── App.js
│── supabase.js
│── index.css
│── index.js
⚙️ Environment Variables

Create a .env file in root folder.

For Create React App (CRA):

REACT_APP_SUPABASE_URL=your_supabase_url
REACT_APP_SUPABASE_KEY=your_supabase_anon_key
📦 Installation

Clone repository:

git clone YOUR_GITHUB_REPO_URL

Move to project folder:

cd project-name

Install dependencies:

npm install

Start development server:

npm start
🗄️ Database Setup
Create Posts Table
CREATE TABLE posts (
  id BIGINT GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
  title TEXT NOT NULL,
  likes INT DEFAULT 0,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);
Insert Sample Data
INSERT INTO posts (title, likes)
VALUES
('Supabase Realtime Tutorial', 0),
('React Learning Guide', 5),
('Modern Backend Development', 10);
Create Comments Table
CREATE TABLE comments (
  id BIGINT GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
  name TEXT NOT NULL,
  comment TEXT NOT NULL,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);
🔒 Row Level Security (RLS)

Enable RLS:

ALTER TABLE comments
ENABLE ROW LEVEL SECURITY;
Read Policy
CREATE POLICY "Anyone can read comments"
ON comments
FOR SELECT
TO public
USING (true);
Insert Policy
CREATE POLICY "Anyone can add comments"
ON comments
FOR INSERT
TO public
WITH CHECK (true);
🚀 Deployment
Deploy on Vercel
Push code to GitHub
Import repository in Vercel
Add environment variables
Deploy
📸 Demo Features
Add comments
Like posts
Realtime synchronization
Secure database policies
🎯 Learning Outcomes

By building this project, you will learn:

Supabase integration with React
PostgreSQL database basics
Realtime subscriptions
Row Level Security (RLS)
Production deployment
Environment variable management
👨‍💻 Author

Ram
Full Stack Developer

Built with ❤️ using React + Supabase


Save it as:

```text
README.md

Then commit:

git add .
git commit -m "add readme"
git push
