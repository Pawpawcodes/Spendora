# Firebase Setup for SPENDORA

## Step 1: Create Firebase Project
1. Go to https://console.firebase.google.com/
2. Click "Create a project"
3. Name it "spendora-app"
4. Enable Google Analytics (optional)
5. Create project

## Step 2: Enable Services
In Firebase Console:
1. **Authentication** → Get started → Enable Email/Password
2. **Firestore Database** → Create database → Start in test mode
3. **Storage** → Get started (for CSV file uploads)

## Step 3: Get Configuration
1. Project Settings → General → Your apps
2. Click "Web app" icon
3. Register app as "SPENDORA"
4. Copy the config object

## Step 4: Install Firebase SDK
```bash
npm install firebase
```

## Step 5: Add Environment Variables
Create `.env` file:
```env
REACT_APP_FIREBASE_API_KEY=your_api_key
REACT_APP_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
REACT_APP_FIREBASE_PROJECT_ID=your_project_id
REACT_APP_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
REACT_APP_FIREBASE_APP_ID=your_app_id
```

## Step 6: Database Structure
```
users/
  {userId}/
    profile: { name, email, createdAt }
    budget: { amount, period, createdAt }
    transactions/
      {transactionId}: { date, description, amount, category }
    categories/
      {categoryId}: { name, totalSpent, color }
```
