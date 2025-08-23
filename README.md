# SPENDORA - Pandora Paradox × Emerald

> *Your Emerald Financial Guardian powered by mystical wisdom*

![SPENDORA Banner](https://img.shields.io/badge/SPENDORA-Pandora%20Paradox%20×%20Emerald-00C853?style=for-the-badge&logo=react)

## 🔮 Overview

SPENDORA is a mystical financial management web application that combines the power of Pandora's Paradox with emerald wisdom to help users manage their finances. Built with React and featuring a stunning dark theme with emerald accents, it provides comprehensive financial tracking, AI-powered coaching, and gamified feedback systems.

## ✨ Features

### 🏠 **Landing Experience**
- Animated emerald orb with mystical energy rings
- Hero banner with Pandora Paradox branding
- Feature showcase with glass card effects
- Responsive design for all devices

### 🔐 **Authentication System**
- Create Account with form validation
- Login with redirect flow
- Persistent user sessions
- Emerald-themed UI components

### 📊 **Financial Dashboard**
- Interactive charts (Pie, Line, Bar) using Recharts
- Budget progress tracking with color-coded warnings
- Category-based spending breakdown
- Recent transactions table
- Real-time budget alerts

### 📁 **Data Upload & Processing**
- Support for CSV, Excel (.xlsx, .xls), and PDF files
- Drag-and-drop file upload interface
- CSV parsing with PapaParse library
- Security warning modal for sensitive data
- Budget setting with validation

### 🤖 **AI Finance Coach**
- Interactive chatbot interface
- Contextual financial advice
- Auto-nudges when approaching budget limits
- Quick suggestion buttons
- Real-time spending analysis

### 💎 **Emerald Reward System**
- Feedback submission rewards
- Star rating system
- Animated emerald collection
- Gamified user engagement

### ⚠️ **Smart Budget Warnings**
- Automatic alerts at 80% budget usage
- Color-coded progress indicators
- Toast notifications
- Coach integration for overspending

## 🛠️ Technology Stack

- **Frontend**: React 18.2.0
- **Routing**: React Router DOM 6.3.0
- **Charts**: Recharts 2.5.0
- **CSV Processing**: PapaParse 5.4.1
- **Styling**: Custom CSS with CSS Variables
- **State Management**: React Context API
- **Build Tool**: Create React App

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd windsurf-project
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

### Build for Production
```bash
npm run build
```

## 📱 Usage Flow

### Complete Demo Journey
1. **Landing Page** → Create account or login
2. **Authentication** → Sign up with validation
3. **Upload Data** → Upload CSV/Excel file + set budget
4. **Security Modal** → Confirm sensitive data sharing
5. **Dashboard** → View charts, budget progress, transactions
6. **Budget Warning** → Automatic alerts when overspending
7. **AI Coach** → Get personalized financial advice
8. **Feedback** → Rate experience and earn emeralds

### Sample CSV Format
```csv
date,description,amount,category
2025-01-15,Grocery Store,85.50,Food
2025-01-14,Gas Station,45.00,Transportation
2025-01-13,Coffee Shop,12.75,Food
```

## 🎨 Design System

### Color Palette
- **Primary Background**: `#0D0F12` (Deep Black)
- **Secondary Background**: `#1A1D23` (Dark Gray)
- **Emerald Primary**: `#00C853` (Vibrant Green)
- **Emerald Secondary**: `#00E676` (Light Green)
- **Warning Red**: `#FF1744` (Alert Red)
- **Amber Warning**: `#FFC107` (Caution Yellow)

### Typography
- **Font Family**: Inter (Google Fonts)
- **Weights**: 300, 400, 500, 600, 700, 800, 900

### UI Components
- Glass card effects with backdrop blur
- Emerald glow buttons with hover animations
- Progress bars with color-coded states
- Modal dialogs with emerald borders
- Toast notifications with smooth animations

## 🏗️ Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── Header.js       # Navigation header
│   ├── Footer.js       # Footer with quick feedback
│   ├── Modal.js        # Modal dialog component
│   └── Toast.js        # Notification component
├── context/            # State management
│   └── AppContext.js   # Global app state
├── pages/              # Route components
│   ├── LandingPage.js  # Home page
│   ├── CreateAccount.js # Registration
│   ├── Login.js        # Authentication
│   ├── UploadBudget.js # File upload & budget
│   ├── Dashboard.js    # Main dashboard
│   ├── Coach.js        # AI chatbot
│   └── Feedback.js     # User feedback
├── App.js              # Main app component
├── App.css             # App-specific styles
├── index.js            # React entry point
└── index.css           # Global styles
```

## 🔧 Configuration

### Environment Variables
Create a `.env` file for production configurations:
```env
REACT_APP_API_URL=your_api_endpoint
REACT_APP_OPENAI_KEY=your_openai_key
```

### Customization
- Modify color variables in `src/index.css`
- Update branding in `src/components/Header.js`
- Customize chart themes in `src/pages/Dashboard.js`

## 🚀 Deployment

### Netlify Deployment
1. Build the project: `npm run build`
2. Deploy the `build` folder to Netlify
3. Configure redirects for React Router

### Vercel Deployment
1. Connect your GitHub repository
2. Vercel will auto-detect React and deploy
3. Configure environment variables in dashboard

## 🎯 Future Enhancements

### Planned Features
- [ ] Real OpenAI integration for coach
- [ ] Export dashboard as PNG/PDF
- [ ] Manual transaction recategorization
- [ ] Multiple budget periods (weekly, yearly)
- [ ] Bank account integration
- [ ] Mobile app version
- [ ] Advanced analytics and insights
- [ ] Social features and challenges

### Stretch Goals
- [ ] Cryptocurrency tracking
- [ ] Investment portfolio analysis
- [ ] Bill reminder system
- [ ] Savings goal tracking
- [ ] Multi-currency support

## 🤝 Contributing

### Team ParaX
Building the future of financial wellness through emerald wisdom.

### Contact
- **Email**: team@parax-spendora.com
- **Discord**: ParaX Community Server
- **GitHub**: github.com/parax/spendora

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by the mystical powers of Pandora's Paradox
- Built with the wisdom of emerald energy
- Powered by the React ecosystem
- Designed for financial enlightenment

---

**Made with 💎 by Team ParaX**

*"Unlock the mysteries of your finances with the power of Pandora's Paradox"*
