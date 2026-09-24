AlumniConnect + HVS.Ai

A full-stack alumni networking platform with integrated AI-powered tools.

🔗 Live Demo: alumini-connect-hvs-ai.vercel.app 📦 Repository: github.com/Harshini-1811/helloalumini

Overview

AlumniConnect + HVS.Ai is a full-stack platform built to bring students and alumni onto a single network — mentorship, job referrals, events, and discussion — enhanced with a suite of Claude-powered AI tools for content generation, career prep, and communication. The project was built and led by a 4–5 member team, spanning 14 feature pages and 7 AI-powered tools.

Features
Core Platform (14 feature pages)
Mentorship Matching — connects students with alumni mentors using a custom matching algorithm
Messaging — direct communication between users
Jobs Board — alumni-posted job and referral listings
Events — alumni meetups, webinars, and networking events
Forum — open discussion space for the community
Quiz Module — skill-assessment / engagement quizzes
Analytics Dashboard — usage and engagement insights
AI-Powered Tools (7 tools, via Anthropic Claude API)
AI Chat Assistant — conversational support across the platform
Website Builder — AI-assisted website generation
Presentation Generator — automated slide-deck creation
Document Generator — automated document drafting
PDF Tools — AI-assisted PDF processing
Video Analyzer — AI-powered video content analysis
AI Interview Simulator — simulated interview practice with AI-generated questions and feedback
Mentor-Matching Algorithm

Uses normalized string comparison and keyword scoring to generate a 0–100% compatibility score between mentors and mentees, surfacing the most relevant matches for each user.

Tech Stack
Layer	Technology
Frontend	React 18, Vite
Backend	Python, FastAPI
Database	SQLite (9 normalized tables, 13 indexes)
AI	Anthropic Claude API (claude-sonnet-4)
Voice	Web Speech API
Deployment	Vercel
Architecture
Frontend: React 18 + Vite single-page application, communicating with the backend over REST APIs
Backend: FastAPI service exposing REST endpoints for auth, mentorship matching, messaging, jobs, events, forum, quizzes, analytics, and the AI tool suite
Database: SQLite, normalized across 9 tables with 13 indexes for query performance
AI Layer: Backend routes calls through the Anthropic Claude API for chat, content generation, and the AI Interview Simulator
Voice: Web Speech API integrated on the frontend for voice-based interactions
Getting Started
Prerequisites
Node.js (v18+) and npm
Python 3.10+
An Anthropic API key
Installation
bash
# Clone the repository
git clone https://github.com/Harshini-1811/helloalumini.git
cd helloalumini

# Frontend setup
cd frontend
npm install
npm run dev

# Backend setup (in a new terminal)
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
Environment Variables

Create a .env file in the backend directory:

ANTHROPIC_API_KEY=your_api_key_here
DATABASE_URL=sqlite:///./alumniconnect.db

Adjust paths, entry-point filenames, and env variable names above to match your actual project structure if they differ.

Project Structure
helloalumini/
├── frontend/          # React 18 + Vite application
├── backend/           # FastAPI application
│   ├── main.py
│   ├── models/        # Database models
│   ├── routes/        # API route handlers
│   └── ai/            # Claude API integration
└── README.md
Team

Built and led by Harshini Yaddlapalli (Team Lead) with a 4–5 member team.

License

This project is available for educational and portfolio purposes.

AUTHOR:Harshini Yaddlapalli
