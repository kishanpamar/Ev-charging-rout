# Quick Start Guide - EV Smart (No MongoDB Required!)

## 🚀 Step-by-Step Setup

### Step 1: Install Backend Dependencies

Open a terminal in the project root and run:

```bash
cd backend
npm install
```

### Step 2: Start Backend Server

```bash
npm run dev
```

You should see:
- ✅ `In-memory database initialized`
- ✅ `Default admin user created: admin@evsmart.com / admin123`
- ✅ `In-memory database connected`
- ✅ `Server running on port 5000`

**Keep this terminal open!**

### Step 3: Install Frontend Dependencies

Open a **NEW** terminal window and run:

```bash
cd frontend
npm install
```

### Step 4: Start Frontend Development Server

```bash
npm run dev
```

You should see:
- ✅ Vite dev server running (usually on `http://localhost:3000`)

### Step 5: Open in Browser

Open your browser and navigate to the URL shown in the frontend terminal (usually `http://localhost:3000`)

## 🎯 Default Admin Login

- **Email**: `admin@evsmart.com`
- **Password**: `admin123`

## 📝 Creating Your First Account

1. Click "Register" on the landing page
2. Fill in your details
3. Choose a role: `user`, `owner`, or `admin`
4. Click "Register"
5. You'll be automatically logged in!

## ⚠️ Important Notes

- **No MongoDB needed!** Everything runs in memory
- Data is lost when you restart the backend server
- Perfect for development and testing
- Both servers must be running simultaneously

## 🛠️ Troubleshooting

**Backend won't start?**
- Make sure port 5000 is not in use
- Check that all dependencies are installed (`npm install` in backend folder)

**Frontend won't start?**
- Make sure port 3000 is not in use
- Check that all dependencies are installed (`npm install` in frontend folder)
- Make sure backend is running first

**Can't connect to API?**
- Ensure backend is running on port 5000
- Check the Vite proxy configuration in `frontend/vite.config.js`

## 🎉 You're All Set!

The application is now running with:
- ✅ React frontend with Vite
- ✅ Express backend
- ✅ In-memory storage (no database!)
- ✅ JWT authentication
- ✅ Role-based access control

