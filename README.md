# My Awesome Project
Check out the **live demo** https://saas-nine-delta.vercel.app/


# ClinicalNotes AI - Professional Medical Documentation Platform

A comprehensive AI-powered clinical documentation platform designed for healthcare professionals. Transform your consultation notes into professional medical summaries, actionable follow-up plans, and patient communications using advanced artificial intelligence.

## 🏥 Features

- **AI-Powered Clinical Summaries**: Generate comprehensive medical record summaries from consultation notes
- **Follow-up Action Planning**: Extract clear next steps and follow-up actions for every consultation
- **Patient Communication**: Automatically draft clear, patient-friendly email communications
- **Real-time Processing**: Stream AI responses for immediate feedback
- **HIPAA Compliant**: Enterprise-grade security and compliance
- **Professional Authentication**: Secure user management with Clerk

## 🚀 Technology Stack

### Frontend
- **Next.js 15** - React framework with App Router
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first styling
- **Clerk** - Authentication and user management
- **React Markdown** - Rich text rendering

### Backend
- **FastAPI** - High-performance Python web framework
- **OpenAI GPT-5** - Advanced AI language model
- **Server-Sent Events** - Real-time streaming responses
- **Clerk Authentication** - Secure API access

## 📋 Prerequisites

- Node.js 18+ and npm/yarn
- Python 3.8+
- OpenAI API key
- Clerk account and API keys

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd clinical-notes-ai
```

### 2. Frontend Setup
```bash
# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
```

Add the following to your `.env.local`:
```env
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
```

### 3. Backend Setup
```bash
# Install Python dependencies
pip install -r requirements.txt

# Set up environment variables
export OPENAI_API_KEY=your_openai_api_key
export CLERK_JWKS_URL=your_clerk_jwks_url
```

### 4. Development Server
```bash
# Start frontend (Terminal 1)
npm run dev

# Start backend (Terminal 2)
cd api
uvicorn index:clinical_app --reload --port 8000
```

## 🏗️ Project Structure

```
clinical-notes-ai/
├── pages/                 # Next.js pages
│   ├── _app.tsx         # App wrapper with authentication
│   ├── _document.tsx    # HTML document structure
│   ├── index.tsx        # Landing page
│   └── product.tsx      # Clinical dashboard
├── api/                 # Backend API
│   └── index.py         # FastAPI application
├── styles/              # Global styles
│   └── globals.css      # Tailwind and custom styles
├── public/              # Static assets
└── requirements.txt     # Python dependencies
```

## 🔧 Configuration

### Environment Variables

**Frontend (.env.local):**
- `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY` - Clerk public key
- `CLERK_SECRET_KEY` - Clerk secret key

**Backend:**
- `OPENAI_API_KEY` - OpenAI API key
- `CLERK_JWKS_URL` - Clerk JWKS endpoint

### Clerk Setup
1. Create a Clerk account at [clerk.com](https://clerk.com)
2. Set up authentication providers
3. Configure subscription plans for premium features
4. Add your domain to allowed origins

## 🚀 Deployment

### Frontend (Vercel)
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

### Backend (Railway/Heroku)
```bash
# Railway deployment
railway login
railway link
railway up
```

## 🔒 Security & Compliance

- **HIPAA Compliant**: Enterprise-grade security measures
- **Authentication**: Secure user authentication with Clerk
- **Data Protection**: Encrypted data transmission
- **Access Control**: Role-based access management

## 📊 API Documentation

### POST /api
Process clinical consultation data and generate AI documentation.

**Request Body:**
```json
{
  "patient_name": "John Doe",
  "date_of_visit": "2024-01-15",
  "notes": "Patient presents with..."
}
```

**Response:** Server-sent events stream with AI-generated content.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Contact: [support@clinicalnotes.ai](mailto:support@clinicalnotes.ai)

## 🔄 Version History

- **v1.0.0** - Initial release with core clinical documentation features
- Enhanced AI processing with streaming responses
- Professional authentication and subscription management
- HIPAA-compliant security implementation
