<div align="center">
  <img src="../logo.png" alt="LifeOps Logo" width="150" />
  
  # AI LifeOps Assistant
  
  **"An AI-powered execution system that turns goals into daily actionable plans and adapts based on user progress"**
</div>

## 📖 Objective
Design and develop a modern AI-driven web application that helps users convert high-level goals into structured daily tasks, track execution, receive intelligent reminders, and stay motivated through analytics and gamification.

## 🎯 Target Users
- Students (learning, coding, ML, interview prep)
- Self-learners
- Early professionals

## ✨ Core Functionality
1. **Goal Input System:** Users define goals with title, description, deadline, daily time commitment, and difficulty level.
2. **AI Planning Engine:** Uses LLM APIs to break goals down into structured weekly milestones and actionable daily tasks.
3. **Daily Dashboard:** Features today’s actionable tasks, priority markers, estimated times, progress summaries, and smart adaptive suggestions.
4. **Task Tracking System:** Allows users to mark tasks as Completed or Missed and logs status history.
5. **Adaptive Scheduler:** Re-balances the workload by shifting missed tasks forward, reducing overload, and maintaining a realistic pace automatically.
6. **Progress Analytics:** Daily/weekly completion graphs, consistency scores, and streak tracking.
7. **Notifications & Reminders:** Daily task summaries, missed alerts, and streak warnings via Firebase or browser push.
8. **Gamification System:** Earn XP points per task, streak rewards, and goal completion badges. Level progression (Beginner → Consistent → Focused → Elite).
9. **User Authentication:** Email/password login and optional Google OAuth integration.

## 🎨 UI/UX Design
- **Design Style:** Clean, minimal, modern SaaS UI featuring dark/light modes, card-based layouts, and smooth micro-interactions.
- **Key Pages:** 
  1. Landing Page
  2. Goal Setup Page
  3. Dashboard
  4. Analytics Page
  5. Profile Page
- **Elements:** Custom task cards, visual progress rings, flame streak indicators, and animated badge popups.

## 🛠️ Tech Stack (Free Tier Optimized)
- **Frontend:** React + Tailwind CSS + Vite (Hosted on Vercel / Netlify)
- **Backend:** FastAPI (Python) (Hosted on Render / Railway)
- **Database:** Supabase (PostgreSQL + Auth) or Firebase
- **AI Solutions:** OpenRouter (free tier), local Ollama, or HuggingFace API integration
- **Notifications:** Firebase Cloud Messaging (FCM)

## 🗄️ Database Structure
- **Users**: `id`, `email`, `password`
- **Goals**: `id`, `user_id`, `title`, `deadline`, `difficulty`
- **Tasks**: `id`, `goal_id`, `date`, `description`, `status`
- **Progress**: `id`, `user_id`, `completion_rate`, `streak`
- **Badges**: `id`, `user_id`, `badge_type`

## 🔌 API Endpoints
- `POST /goal` - Creates a new user goal.
- `GET /tasks/today` - Fetches the generated tasks for the current day.
- `POST /task/update` - Updates a task's status (completed/missed).
- `GET /progress` - Retrieves streak and consistency information.
- `GET /analytics` - Polls completion rates to render the analytics dashboard.

## 🔄 Data Flow
`User` → `Goal Input` → `Backend` → `AI Planning Engine` → `Tasks Stored` → `Dashboard` → `User Updates Tasks` → `Adaptive Scheduler` → `Updated Plan` → `Notifications` → `User`

---

## 🏗️ Architecture & Diagram
![Architecture Diagram](../architecture.png)

*The system encompasses user interactions (Goal Input, Dashboard, Task Tracker) feeding into internal logic components (AI Planning Engine, Adaptive Scheduler, Progress Analytics, Notification Service) interfacing with external dependencies (LLM API, Database).*

---

## 📈 Success Metrics
- **Task completion rate (%)**
- **Daily active users (DAU)**
- **Streak retention metrics**
- **Goal completion rate**

## 🚧 Constraints
- Must be buildable in **3–4 weeks**.
- Focus heavily on execution functionality rather than feature overload.
- Keep the overall underlying architecture highly modular and scalable.

---

## 🤝 Contribute
We welcome community contributions! Whether you're fixing bugs, adding new features, or optimizing the AI models:

1. **Fork** the repository
2. **Create** your feature branch: `git checkout -b feature/AmazingFeature`
3. **Commit** your changes: `git commit -m 'Add some AmazingFeature'`
4. **Push** to the branch: `git push origin feature/AmazingFeature`
5. **Open a Pull Request** 

Ensure that you keep the architecture modular and adhere to the project's design guidelines.
