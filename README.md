# 🎯 AI Interview Performance Analyzer

<p align="center">
  <strong>AI-powered interview practice, speech analytics, and personalized performance feedback for placement preparation.</strong>
</p>


## 📌 Project Overview

**AI Interview Performance Analyzer** is a web-based placement preparation platform designed to help students practice technical, HR, and behavioral interviews.

The application captures spoken or typed responses and evaluates important communication and interview-performance indicators such as:

- Speaking duration
- Word count
- Words Per Minute (WPM)
- Filler-word usage
- Repeated words
- STAR-method structure
- Technical depth
- Response quality
- Overall interview readiness

The platform converts these signals into actionable feedback so students can identify weaknesses and improve their interview communication.

---

## ✨ Key Features

### 🎙️ Real-Time Interview Practice
Practice technical, HR, and behavioral questions using microphone-based responses or typed answers.

### 📊 Speech & Communication Analytics
Analyze:
- Speaking pace
- WPM/cadence
- Response duration
- Word count
- Filler words such as *um, uh, like, you know*
- Consecutive word repetition

### 🧠 Response Structure Analysis
Checks whether answers demonstrate the **STAR framework**:

**Situation → Task → Action → Result**

### 💡 Instant Coaching
Each response can be presented through practical coaching sections:

- **Here's What Came Through**
- **What Worked**
- **Tighten This**
- **Try This Next Time**

### 📄 Comprehensive Interview Report
View an overall readiness score, question-by-question analysis, performance breakdown, and printable report.

### 📈 Practice History
Track previous interview sessions and observe improvement over time.

### 🏫 Placement Cell Dashboard
An administrative interface allows placement coordinators to view aggregate readiness information, review transcripts, and manage question pools.

### 🔐 Authentication
Supports authenticated user workflows through Supabase and Google authentication integration.

---

## 🛠️ Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React 19 |
| Language | TypeScript |
| Build Tool | Vite |
| Styling | Tailwind CSS |
| UI Animation | Framer Motion |
| Icons | Lucide React |
| Routing | React Router |
| Database | Supabase PostgreSQL |
| Authentication | Supabase Auth / Google Auth |
| Speech | Web Speech API |
| Audio Analysis | Web Audio API |
| Backend | Vercel Serverless Functions |
| Deployment | Vercel |

---

## 🔄 Application Workflow

```text
User
  │
  ▼
Interview Setup
  │
  ▼
Select Interview Type
  │
  ▼
Interview Workstation
  │
  ├── 🎙️ Voice Response
  │       │
  │       ▼
  │   Speech-to-Text
  │
  └── ⌨️ Typed Response
          │
          ▼
   Response Analysis Engine
          │
          ├── WPM / Pace
          ├── Filler Words
          ├── Repetition
          ├── STAR Structure
          └── Technical Depth
                  │
                  ▼
          Personalized Feedback
                  │
                  ▼
           Interview Report
                  │
                  ▼
            Practice History
```

---

## 📁 Complete Project Structure

```text
AI-Interview-Performance-Analyzer/
│
├── api/
│   ├── admin-stats.js
│   ├── analyze-response.js
│   ├── db-client.js
│   ├── db-wake.js
│   ├── questions.js
│   ├── responses.js
│   └── sessions.js
│
├── public/
│   ├── favicon.svg
│   └── vite.svg
│
├── src/
│   ├── assets/
│   │   └── react.svg
│   │
│   ├── components/
│   │   ├── AudioVisualizer.tsx
│   │   ├── FeedbackCard.tsx
│   │   ├── FillerBadge.tsx
│   │   ├── Footer.tsx
│   │   ├── Header.tsx
│   │   ├── PacingGauge.tsx
│   │   └── PrintableReport.tsx
│   │
│   ├── contexts/
│   │   └── AuthContext.tsx
│   │
│   ├── lib/
│   │   ├── analyzer.ts
│   │   ├── googleAuth.ts
│   │   ├── soundEffects.ts
│   │   └── supabase.ts
│   │
│   ├── pages/
│   │   ├── AdminDashboard.tsx
│   │   ├── AuthPage.tsx
│   │   ├── InterviewReport.tsx
│   │   ├── InterviewSetup.tsx
│   │   ├── InterviewWorkstation.tsx
│   │   ├── LandingPage.tsx
│   │   └── PracticeHistory.tsx
│   │
│   ├── types/
│   │   └── interview.ts
│   │
│   ├── App.css
│   ├── App.tsx
│   ├── index.css
│   └── main.tsx
│
├── .env.example
├── .gitignore
├── .vite-source-tags.js
├── eslint.config.js
├── index.html
├── package.json
├── package-lock.json
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
├── vercel.json
├── vite.config.ts
└── README.md
```

---

## ⚙️ Local Installation

### 1. Clone the repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
cd AI-Interview-Performance-Analyzer
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file using `.env.example`:

```env
VITE_SUPABASE_URL=https://your-project.supabase.co
VITE_SUPABASE_ANON_KEY=your-anon-key

NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key

SUPABASE_SERVICE_ROLE_KEY=your-service-role-key
```

> Never commit real secret keys or service-role credentials to GitHub.

### 4. Start development server

```bash
npm run dev
```

Open the local Vite URL shown in the terminal.

### 5. Create production build

```bash
npm run build
```

### 6. Preview production build

```bash
npm run preview
```

---

## ☁️ Vercel Deployment

1. Push the project to GitHub.
2. Import the repository into Vercel.
3. Select the Vite/React project configuration.
4. Add the required environment variables in **Vercel → Project Settings → Environment Variables**.
5. Deploy the project.

The repository already includes:

```text
vercel.json
```

for deployment configuration and SPA routing.

---

## 🎓 College Project Value

This project demonstrates practical implementation of:

- Artificial Intelligence concepts
- Natural Language Processing
- Speech-to-Text interaction
- Web Audio processing
- Full-stack web development
- Authentication
- Database integration
- Serverless APIs
- Performance analytics
- Data visualization
- Cloud deployment

---

## 🧪 Suggested Demo Flow

For a college presentation:

1. Open the **Live Demo**.
2. Start an interview practice session.
3. Select an interview category.
4. Answer a sample question using the microphone.
5. Show real-time transcription.
6. Complete the response.
7. Demonstrate WPM and filler-word analysis.
8. Show STAR-structure feedback.
9. Open the final interview report.
10. Demonstrate practice history.
11. Show the placement/admin dashboard if configured.

---

## 🎯 Example Interview Questions

### HR
> Tell me about yourself.

### Behavioral
> Describe a challenging situation you faced in a project and how you solved it.

### Technical
> Explain the difference between a process and a thread.

### Project
> Explain your role and contribution in your final-year project.

---

## 🔒 Security Notes

- Store secrets in environment variables.
- Do not commit `.env` files.
- Use Supabase Row Level Security where applicable.
- Keep the Supabase service-role key server-side only.
- Configure authentication redirect URLs correctly for production.

---

## 📈 Future Enhancements

- AI-generated follow-up questions
- Resume-based personalized interviews
- Multilingual interview support
- Advanced sentiment and confidence analysis
- Facial-expression analysis with explicit user consent
- Interview benchmarking
- Placement-readiness dashboards
- Automated improvement plans
- Exportable PDF certificates/reports

---

## 👨‍💻 Project Type

**Domain:** Artificial Intelligence + Speech & Text Analysis + Web Technology

**Use Case:** Student Placement & Interview Preparation



**Architecture:** React SPA + Serverless API + Supabase



## ⭐ Project Highlights

> **Practice. Analyze. Improve. Get Interview Ready.**

AI Interview Performance Analyzer transforms ordinary interview practice into a measurable and feedback-driven learning experience.
