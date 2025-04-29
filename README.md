# 📬 Smart Email Assistant

Smart Email Assistant is an AI-powered tool that helps users manage and reply to emails faster and more efficiently. It includes a Spring Boot backend, a React frontend, and a Chrome extension that integrates directly into Gmail to generate smart, context-aware replies using GPT-based models.

---

## 🚀 Features

- ✉️ Seamless Gmail integration via Chrome Extension
- 🤖 AI-generated replies using OpenAI/GPT
- 🧠 Understands email thread context for accurate suggestions
- 🎯 Reply tone customization (formal, casual, concise, etc.)
- 📅 Reply scheduling and smart summaries
- 🔐 Privacy-respecting design and secure token handling

---

## 🛠️ Tech Stack

| Component     | Technology                   |
|---------------|------------------------------|
| Frontend      | React.js                     |
| Backend       | Spring Boot (Java)           |
| NLP/AI        | OpenAI API (GPT-4)           |
| Browser Ext.  | JavaScript, Gmail DOM APIs   |
| Email Access  | Gmail API / IMAP/SMTP        |


---

## 📂 Project Structure
Smart-Email-Assistant/

    ├── SmartEmailAssistantSpring/   # Spring Boot backend (email processing & AI integration)
    
    ├── SmartEmailAssistantReact/    # React frontend for dashboard and controls
    
    ├── SmartEmailAssistantExt/      # Chrome extension to modify Gmail UI
    
    ├── README.md                    # Project documentation
    
    └── .gitignore                   # Git ignore file



## 🧪 How to Run the Project Locally

This project has 3 main parts:
1. **Backend (Spring Boot)** – processes emails and generates AI replies.
2. **Frontend (React)** – dashboard/UI for managing settings.
3. **Browser Extension** – integrates AI replies into Gmail.



### ✅ Prerequisites

- **Java 17+** and **Maven** for the backend
- **Node.js** and **npm** for the frontend
- **Google Chrome** for the extension
- **Gmail account** (for testing the extension)
- **OpenAI API key** (for AI replies)



### ⚙️ Step-by-Step Setup

#### 1. Clone the Repository
    git clone https://github.com/Kumargaurav126/Smart-Email-Assistant.git
    
    cd Smart-Email-Assistant



#### 2. Run the Backend (Spring Boot)
Go to the backend folder and run the Spring Boot server:

    cd backend
    
    ./mvnw spring-boot:run
    
  The backend will start on http://localhost:8080.



#### 3. Run the Frontend (React)
In a new terminal window, navigate to the frontend folder, install dependencies, and start the React development server:

    cd SmartEmailAssistantReact
    npm install
    npm start

The frontend will be available at http://localhost:3000 and will communicate with the backend API.



#### 4. Load the Gmail Chrome Extension
i. Open Chrome and navigate to chrome://extensions/.

ii. Enable Developer Mode (top right).

iii. Click Load unpacked and select the folder gmail-extension/.



#### 5. Connect Gmail + AI
i. Open Gmail in Chrome.

ii. Open an email.

iii. The extension will read the email and call the backend (http://localhost:8080) to generate a reply using AI.

iv. The reply will appear inside Gmail, and you can edit or send it directly.



#### 6. Add Your Google Gemini API Key
If using Google Gemini for AI replies, you'll need to provide your Gemini API key and its url. Add it to your backend’s application.properties file like this:

    gemini.api.key = your-gemini-api-key
    gemini.api.url = https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent
