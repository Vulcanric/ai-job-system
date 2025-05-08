# Real-Time Job Market Insight Agent
## 🔸Overview
An AI-powered web app that tracks job posting across major tech hiring platform (like LinkedIn, Indeed, Stack Overflow Jobs) in real time, analyzes trends, and provides insights.
## 💡Key Components
### 1. Frontend (User Interface)
- **Built with:** Streamlit
- **Features:**
  - Search by skill, location, company.
  - Interactive job trend visualization.
  - Real-time dashboard with insights.
### 2. Backend (API Layer)
- **Built with:** FastAPI
- **Responsibilities:**
    - Coordinates scraping via Bright Data MCP.
    - Queries and updates job data in the database.
    - Handles scheduled data pulls.
    - Sends summarized insight to frontend.
### 3. Data Layer
- **Storage:** PostgreSQL
- **Data / Data Structure:** Job title, company, salary (if available), location, date, skills, job description.
### 4. Scraping Layer
- **Powered by:** Bright Data MCP
- **Actions:**
    - **Discover:** Search job boards using keywords
    - **Access:** Handle JS-loaded or protected pages
    - **Extract:** Pull clean job listings data
    - **Interact:** Deal with forms, clicks, dynamic content
### 5. AI Layer
- **LLMs**: Ollama (Mistra, llama3)
- **Tasks:**
    - Keyword extraction (e.g., top skills per week)
    - Sentiment analysis (e.g., job market optimism)
    - Summarization (e.g., "Remote Python jobs up 20%")
