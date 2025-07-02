
# 🤖 HealthAI – Intelligent Healthcare Assistant

HealthAI is a virtual healthcare assistant powered by IBM watsonx.ai (Granite 13B model). It enables users to ask health-related questions through a web interface and receive intelligent, AI-generated responses.

---

## 🚀 Features

- 🧠 Natural Language Interaction using Granite 13B (WatsonX) or GPT models  
- 🌐 Simple, mobile-friendly frontend using HTML/CSS  
- 🔁 Flask-based backend API for request/response handling  
- 🐳 Docker-ready for easy deployment  
- ☁️ Deployable on IBM Code Engine or any cloud container platform

---

## 🗂️ Project Structure

```
HealthAI-Assistant/
├── backend/
│   ├── app.py               # Flask backend
│   ├── requirements.txt     # Python dependencies
│   └── .env.example         # Sample environment variables
├── frontend/
│   └── index.html           # Frontend interface
├── deploy/
│   └── Dockerfile           # For containerization
├── .gitignore
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/HealthAI-Assistant.git
cd HealthAI-Assistant
```

### 2. Configure Environment

Copy the `.env.example` and fill in your values:

```bash
cp backend/.env.example backend/.env
```

Edit `backend/.env` with your actual credentials:
```env
API_KEY=your_ibm_or_openai_key
MODEL_ID=granite-13b-chat-v1
PROJECT_ID=your_project_id
REGION=us-south
ENDPOINT_URL=https://your-endpoint-url.com
```

### 3. Install Dependencies

```bash
cd backend
pip install -r requirements.txt
```

### 4. Run the Flask Server

```bash
python app.py
```

Visit: [http://localhost:5000](http://localhost:5000)

---

## 🐳 Docker Deployment

```bash
docker build -t healthai-assistant .
docker run -p 5000:5000 healthai-assistant
```

---

## ☁️ IBM Code Engine Deployment (Optional)

You can deploy the Docker image to IBM Code Engine. Make sure your `.env` values are also added to Code Engine's environment settings.

---

## 📌 Notes

- Do **not** commit your real `.env` file to GitHub.
- The current frontend connects to `http://localhost:5000/ask` — update this for production.
- HealthAI is not a replacement for real medical advice.

---

## 📄 License

MIT License – use freely, but credit the original author.

---

## 🙋‍♀️ Created By

**Chukkaluru Suchithra**  
👩‍💻 Powered by IBM watsonx.ai
