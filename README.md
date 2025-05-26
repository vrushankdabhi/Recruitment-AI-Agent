# 🤖 AI Recruitment System

An intelligent Streamlit application that automates the entire recruitment workflow using specialized AI agents. This system simulates a complete recruitment team with distinct roles - from technical resume analysis to interview scheduling - providing a comprehensive, automated hiring solution.

## ✨ Features

### 🎯 Specialized AI Agents
- **Resume Analyzer Agent**: Expert technical recruiter that evaluates skills, experience, and candidate fit
- **Email Communication Agent**: Professional HR coordinator handling all candidate correspondence
- **Interview Scheduler Agent**: Smart scheduling coordinator managing Zoom meetings and calendar coordination
- **Role-Based Evaluation**: Tailored assessment for AI/ML Engineers, Frontend Engineers, and Backend Engineers

### 🔄 Complete Recruitment Workflow
- **Automated Resume Screening**: AI-powered analysis with skill matching and experience verification
- **Intelligent Decision Making**: Lenient evaluation considering project experience and learning potential
- **Professional Communication**: Automated selection/rejection emails with constructive feedback
- **Smart Scheduling**: Automatic interview booking with timezone handling and email notifications
- **Real-time Processing**: Live PDF viewing, instant analysis, and immediate feedback

### 🛠️ Technical Capabilities
- **PDF Resume Processing**: Extract and analyze text from uploaded resumes
- **Multi-role Support**: Predefined skill requirements for different engineering positions
- **Timezone Intelligence**: IST-based scheduling with business hours enforcement
- **Email Integration**: Gmail SMTP with app password authentication
- **Zoom Integration**: Server-to-Server OAuth for meeting creation
- **Session Management**: Persistent state handling for smooth user experience

## 🚀 Prerequisites

Before running the application, complete these essential setup steps:

### 📧 Gmail Configuration
1. **Create or use a dedicated Gmail account** for recruitment purposes
2. **Enable 2-Step Verification** on the Gmail account
3. **Generate App Password**:
   - Visit [Google App Passwords](https://support.google.com/accounts/answer/185833?hl=en)
   - Follow the steps to create a 16-character app password
   - Format: `abcd efgh ijkl mnop` → Use as `abcdefghijklmnop` (no spaces)

### 🎥 Zoom API Setup
1. **Create/Use a Zoom account**
2. **Access Zoom App Marketplace**: [marketplace.zoom.us](https://marketplace.zoom.us)
3. **Create Server-to-Server OAuth App**:
   - Go to Developer Dashboard
   - Create new app → Select "Server-to-Server OAuth"
   - Obtain: Account ID, Client ID, Client Secret
4. **Configure Required Scopes**:

### 🔑 Google Cloud API
1. **Get Gemini API Key**:
   - Visit [Google Cloud Console](https://console.cloud.google.com/)
   - Enable Gemini API
   - Create API credentials

### Environment Setup
Configure the following in the Streamlit sidebar:
- **Gemini API Key**: Your Google Cloud API key
- **Zoom Credentials**: Account ID, Client ID, Client Secret
- **Email Settings**: Sender email and app password
- **Company Name**: For professional email signatures

## 🏃‍♂️ How to Run

```bash
streamlit run recruitment_team_agent.py
```

## 💼 Supported Roles

### 🤖 AI/ML Engineer
- Python, PyTorch/TensorFlow
- Machine Learning algorithms and frameworks
- Deep Learning and Neural Networks
- Data preprocessing and analysis
- MLOps and model deployment
- RAG, LLM, Finetuning and Prompt Engineering

### 🎨 Frontend Engineer
- React/Vue.js/Angular
- HTML5, CSS3, JavaScript/TypeScript
- Responsive design
- State management
- Frontend testing

### ⚙️ Backend Engineer
- Python/Java/Node.js
- REST APIs
- Database design and management
- System architecture
- Cloud services (AWS/GCP/Azure)
- Kubernetes, Docker, CI/CD

## 📋 How It Works

1. **Upload Resume**: Candidate uploads PDF resume
2. **Role Selection**: Choose from available engineering positions
3. **AI Analysis**: Resume analyzer evaluates skills against requirements
4. **Decision Making**: AI determines selection based on 70% skill match threshold
5. **Communication**: Automated email sent with decision and feedback
6. **Interview Scheduling**: For selected candidates, automatic Zoom meeting creation
7. **Confirmation**: Complete workflow with email notifications

## 🔒 Security Features

- **API Key Protection**: Secure input fields with password masking
- **Token Management**: Automatic OAuth token refresh for Zoom
- **Email Security**: App password authentication (no plain passwords)
- **Session Isolation**: User data contained within session state

## 🐛 Troubleshooting

### Common Issues
- **Email not sending**: Verify app password and 2FA setup
- **Zoom meeting creation fails**: Check OAuth scopes and credentials
- **PDF processing errors**: Ensure PDF is text-readable (not image-only)
- **API errors**: Verify all API keys and rate limits

### Debug Mode
Enable debug logging by adding print statements or using the built-in error handling in the application.

## 🔮 Future Enhancements

- **ATS Integration**: Connect with existing applicant tracking systems
- **Advanced Scoring**: Weighted skill assessment with customizable criteria
- **Video Interview Capability**: Automated video interview scheduling
- **Skills Assessment**: Integrated coding challenges and technical tests
- **Multi-language Support**: Resume analysis in multiple languages
