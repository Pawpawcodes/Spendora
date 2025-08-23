# Supabase Setup for SPENDORA (Alternative to Firebase)

## Step 1: Create Supabase Project
1. Go to https://supabase.com
2. Sign up and create new project
3. Choose region and set database password
4. Wait for project setup (2-3 minutes)

## Step 2: Install Supabase Client
```bash
npm install @supabase/supabase-js
```

## Step 3: Get API Keys
1. Go to Project Settings → API
2. Copy your Project URL and anon key

## Step 4: Environment Variables
```env
REACT_APP_SUPABASE_URL=your_project_url
REACT_APP_SUPABASE_ANON_KEY=your_anon_key
```

## Step 5: Database Schema
```sql
-- Users table
CREATE TABLE users (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  email VARCHAR UNIQUE NOT NULL,
  name VARCHAR NOT NULL,
  budget DECIMAL DEFAULT 0,
  created_at TIMESTAMP DEFAULT NOW()
);

-- Transactions table
CREATE TABLE transactions (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  date DATE NOT NULL,
  description VARCHAR NOT NULL,
  amount DECIMAL NOT NULL,
  category VARCHAR NOT NULL,
  created_at TIMESTAMP DEFAULT NOW()
);

-- Enable Row Level Security
ALTER TABLE users ENABLE ROW LEVEL SECURITY;
ALTER TABLE transactions ENABLE ROW LEVEL SECURITY;

-- Policies
CREATE POLICY "Users can view own data" ON users FOR SELECT USING (auth.uid() = id);
CREATE POLICY "Users can update own data" ON users FOR UPDATE USING (auth.uid() = id);
CREATE POLICY "Users can view own transactions" ON transactions FOR SELECT USING (auth.uid() = user_id);
CREATE POLICY "Users can insert own transactions" ON transactions FOR INSERT WITH CHECK (auth.uid() = user_id);
```

## Benefits of Supabase:
- Real SQL database (PostgreSQL)
- Built-in authentication
- Real-time subscriptions
- Row Level Security
- RESTful API auto-generated
