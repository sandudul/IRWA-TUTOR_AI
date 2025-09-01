# TUTOR_AI (Multi-Agent AI Tutoring System)

A sophisticated AI-powered tutoring platform featuring multiple intelligent agents working collaboratively to provide personalized learning experiences.

## 🚀 Features

### Multi-Agent Architecture
- **Content Generator Agent**: Creates educational content, explanations, and learning materials
- **Question Setter Agent**: Generates adaptive questions and assessments
- **Feedback Evaluator Agent**: Analyzes student responses and provides detailed feedback

### Core Technologies
- **Backend**: FastAPI with Python
- **Frontend**: React + Vite + TailwindCSS
- **Database**: SQLite (default) / PostgreSQL (optional)
- **AI**: Google Gemini AI for LLM explanations
- **Security**: JWT authentication, input sanitization, output filtering
- **Testing**: pytest for backend testing

### AI/ML Components
- Large Language Models (LLMs) - Google Gemini
- Natural Language Processing (NLP) - NER, Summarization
- Information Retrieval (IR) - Content search and retrieval
- Agent Communication Protocols - HTTP-based inter-agent communication

### Security Features
- JWT Authentication
- Input sanitization and validation
- Output filtering and content moderation
- Role-based access control
- Rate limiting

### Responsible AI Practices
- Content moderation and filtering
- Bias detection and mitigation
- Transparent AI decision-making
- User privacy protection
- Ethical AI guidelines implementation

## 🏗️ System Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   Database      │
│   (React)       │◄──►│   (FastAPI)     │◄──►│   (SQLite)      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
                              │
                              ▼
                    ┌─────────────────┐
                    │   AI Agents     │
                    │                 │
                    │ • Content Gen   │
                    │ • Question Set  │
                    │ • Feedback Eval │
                    └─────────────────┘
                              │
                              ▼
                    ┌─────────────────┐
                    │  Google Gemini  │
                    │      AI API     │
                    └─────────────────┘
```

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8+
- Node.js 16+
- Google Gemini API Key

### Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

### Environment Variables
Create `.env` files in both backend and frontend directories:

**Backend (.env)**
```
GEMINI_API_KEY=your_gemini_api_key_here
SECRET_KEY=your_secret_key_here
DATABASE_URL=sqlite:///./tutoring_system.db
```

**Frontend (.env)**
```
VITE_API_BASE_URL=http://localhost:8000
```

## 🧪 Testing

```bash
# Backend tests
cd backend
pytest

# Frontend tests
cd frontend
npm test
```

## 📊 Commercialization Plan

### Target Market
- Educational institutions (K-12, Higher Education)
- Corporate training departments
- Individual learners and tutors
- EdTech companies

### Pricing Model
1. **Freemium Tier**: Basic features, limited usage
2. **Professional Tier**: $29/month - Full access, priority support
3. **Enterprise Tier**: Custom pricing - White-label solutions, API access

### Revenue Streams
- Subscription fees
- API usage charges
- Custom integrations
- White-label licensing
- Content marketplace

## 🔒 Security & Compliance

- GDPR compliance
- FERPA compliance for educational data
- SOC 2 Type II certification
- Regular security audits
- Data encryption at rest and in transit

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## 📄 License

MIT License - see LICENSE file for details

## 🆘 Support

For support and questions, please contact:
- Email: support@tutoring-ai.com
- Documentation: https://docs.tutoring-ai.com
- Community: https://community.tutoring-ai.com
