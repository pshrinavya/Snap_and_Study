# 📸 Snap & Study 📚

Snap & Study is an AI-powered study assistant built with **Python, Streamlit, and Google Gemini**.

It allows students to upload an image of their study material, ask questions about it, and get simple explanations from an AI assistant. The generated study summary can also be sent directly to the user's email.

---

## ✨ Features

- 📸 Upload images of study material
- 🤖 AI-powered explanations using Google Gemini
- 💬 Chat with the AI about uploaded material
- 🧠 Get concepts explained in simple words
- 📧 Send study summaries directly to email
- 👤 Simple user onboarding
- 🔐 Secure API and email credentials using Streamlit secrets
- 💻 Simple and beginner-friendly interface

---

## 🛠️ Technologies Used

- **Python**
- **Streamlit**
- **Google Gemini API**
- **Gmail SMTP**
- **Git & GitHub**

### Python Libraries

- `streamlit`
- `google-genai`
- `smtplib`
- `email`

---

## 📂 Project Structure

```text
AI_Chatbot/
│
├── .streamlit/
│   └── secrets.toml
│
├── app.py
├── prompts.py
├── requirements.txt
├── .gitignore
└── README.md
```

> `venv/`, `__pycache__/`, and `secrets.toml` are excluded from GitHub for security and cleanliness.

---

## 🚀 How It Works

### 1. User Onboarding

The user enters:

- Name
- Email address

The application stores these details in Streamlit session state.

### 2. Upload Study Material

The user can upload an image of their study material through the chat interface.

Supported formats:

- JPG
- JPEG
- PNG

### 3. AI Analysis

The uploaded image is sent to Google Gemini.

The AI can:

- Understand the image
- Explain concepts
- Answer questions
- Summarize study material
- Explain difficult topics in simple language

### 4. Email Summary

The user can click **"Send to Email"**.

The application asks Gemini to generate a study summary and sends it to the email address provided during onboarding.

---

## 🔑 API & Secret Configuration

The project uses Streamlit secrets to keep sensitive credentials outside the source code.

Create:

```text
.streamlit/secrets.toml
```

and add:

```toml
GEMINI_API_KEY = "your_gemini_api_key"

GMAIL_ADDRESS = "your_gmail_address@gmail.com"

GMAIL_APP_PASSWORD = "your_gmail_app_password"
```

### ⚠️ Important

Never upload `secrets.toml` to GitHub.

It should be excluded through `.gitignore`.

---

## 📧 Gmail Setup

The email feature uses Gmail SMTP.

To use it:

1. Enable **2-Step Verification** on your Google account.
2. Create a **Google App Password**.
3. Put the generated App Password in `secrets.toml`.

The application uses:

```text
smtp.gmail.com
Port: 465
```

The actual Gmail password is never stored in the source code.

---

## 💻 Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

### 2. Open the project

```bash
cd AI_Chatbot
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the virtual environment

#### Windows PowerShell

```bash
.\venv\Scripts\Activate.ps1
```

If PowerShell blocks the activation script, activate the environment through VS Code or use:

```bash
venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Add your secrets

Create:

```text
.streamlit/secrets.toml
```

and add your Gemini and Gmail credentials.

### 7. Run the application

```bash
python -m streamlit run app.py
```

The application will open in your browser.

---

## 🔒 Security

Sensitive information is intentionally kept out of the repository.

The `.gitignore` file excludes:

```gitignore
.streamlit/secrets.toml
venv/
__pycache__/
*.pyc
```

Never commit:

- API keys
- Gmail passwords
- Gmail App Passwords
- Other private credentials

---

## 🎯 Future Improvements

Some possible improvements include:

- 📚 PDF and document support
- 🎤 Voice-based questions
- 🔊 AI-generated explanations using voice
- 📝 Automatic quiz generation
- 🧠 Flashcard generation
- 📊 Study progress tracking
- 🔖 Save important explanations
- 🌐 Support for multiple languages
- 📱 Improved mobile experience

---

## 👩‍💻 Author

Built as a learning project to explore:

- Generative AI
- Python
- Streamlit
- API integration
- Email automation
- Git & GitHub

---

## ⭐ If You Like the Project

Give the repository a ⭐ on GitHub!
