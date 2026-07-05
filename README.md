# FinMK - Advanced Personal Finance Tracker

## 🚀 Overview

FinMK is a state-of-the-art personal finance management application designed to help you track, analyze, and optimize your financial life. Built with a modern **React** frontend and a robust **Django** backend, it leverages AI and Machine Learning to provide deep insights into your spending habits.

### ✨ Key Features

-   **Dashboard & Analytics**: Interactive charts and graphs (Trends, Category Breakdown, Daily Spending) using **Recharts**.
-   **AI Financial Advisor**: Integrated Chatbot (FinMK Ai) powered by LLMs to answer queries about your finances.
-   **Voice Commands**: Add transactions effortlessly using natural language voice commands (e.g., *"Spent 200 on groceries"*).
-   **Smart Receipt OCR**: Scan receipts to automatically extract and log transaction details.
-   **Budgeting**: Set monthly budgets per category and get predictive alerts if you're pacing to overspend.
-   **Advanced Reporting**: Generate comprehensive PDF financial reports with a single click.
-   **Secure & Scalable**: Built on MongoDB for flexible data storage and Django REST Framework for secure API handling.

---

## 📂 Professional Showcase
For a high-level overview of the project's engineering, architecture, and AI capabilities (suitable for recruiters and portfolio review), please visit the **[showcase/](showcase/)** directory.

---

## 🛠️ Technology Stack

### Frontend
-   **Framework**: React (Vite)
-   **Styling**: Vanilla CSS / Tailwind (Utility Patterns)
-   **Icons**: Lucide React
-   **Charts**: Recharts
-   **Routing**: React Router DOM
-   **HTTP Client**: Axios

### Backend
-   **Framework**: Django & Django REST Framework (DRF)
-   **Database**: MongoDB (via Djongo/PyMongo)
-   **AI/ML**: Scikit-learn (Categorization), Hugging Face Transformers (Forecasting), SpaCy (NLP)
-   **OCR**: EasyOCR
-   **Voice**: Web Speech API (Frontend) + NLP Parsing (Backend)

---

## ⚙️ Prerequisites

Ensure you have the following installed on your system:
-   **Python 3.10+**
-   **Node.js 18+** & **npm**
-   **MongoDB** (Local or Atlas Connection String)

---

## 📥 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/FinMK.git
cd FinMK
```

### 2. Backend Setup
Navigate to the backend directory and set up the Python environment.

```bash
cd backend
python -m venv venv
# Activate Venv:
# Windows:
venv\Scripts\activate
# Mac/Linux:
# source venv/bin/activate

pip install -r requirements.txt
```

**Environment Variables (.env)**
Create a `.env` file in the `backend` folder with the following:
```env
DEBUG=True
SECRET_KEY=your_secret_key_here
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/finance
```

**Run Migrations**
```bash
python manage.py migrate
```

**Start Backend Server**
```bash
python manage.py runserver
```
*Backend runs on: `http://localhost:8000`*

### 3. Frontend Setup
Open a new terminal and navigate to the frontend directory.

```bash
cd frontend
npm install
npm run dev
```
*Frontend runs on: `http://localhost:5173`*

---

## 🎤 How to Use Voice Commands

1.  Navigate to the **Dashboard** or **Transactions** page.
2.  Click the floating **Microphone Icon** (bottom right).
3.  Speak your command naturally.
    -   *Example*: "Add 15 dollars for coffee"
    -   *Example*: "Received salary of 5000"
    -   *Example*: "Spent 50 on Uber"
4.  The system will parse the Merchant, Amount, and Category automatically.

## 🤖 FinMK Ai Chat Advisor

1.  Click the **"Ask AI"** button in the navigation or sidebar.
2.  Type questions like:
    -   *"How much did I spend on food this month?"*
    -   *"Am I over budget?"*
    -   *"Give me tips to save money."*
3.  You can also use the **Voice Button** in the chat input to dictate your questions.

---

## 📦 Deployment

### Exporting for Production/Github
Use the included `export.bat` script to create a clean export of your project (excluding `node_modules` and `venv`) ready for deployment or sharing.
1.  Double click `export.bat` in the root directory.
2.  Find the `export` folder in the project root.

### Render / Vercel
-   **Frontend**: Deploy the `frontend` folder to Vercel/Netlify. Build command: `npm run build`.
-   **Backend**: Deploy the `backend` folder to Render/Heroku. Start command: `gunicorn finance_tracker.wsgi:application`.

---

## 📄 License

This project is licensed under the MIT License.
