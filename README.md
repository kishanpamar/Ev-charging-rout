# EV Smart Route & Charging Assistant

A full-stack web application for EV route planning and charging station management.

## Features

- **User Role**: Calculate route range, view charging stations
- **Owner Role**: Manage charging stations (CRUD operations)
- **Admin Role**: Approve/reject owner applications and stations

## Tech Stack

- **Frontend**: React + Vite + TailwindCSS
- **Backend**: Node.js + Express
- **Database**: In-memory storage (no database required!)
- **Authentication**: JWT

## Setup Instructions

### Prerequisites

- Node.js (v16 or higher)
- No database installation needed! Uses in-memory storage.

### Backend Setup

1. Navigate to backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file (optional, defaults are provided):
```env
PORT=5000
JWT_SECRET=your-super-secret-jwt-key
```

4. Start the server:
```bash
npm run dev
```

**Note**: A default admin user is automatically created:
- Email: `admin@evsmart.com`
- Password: `admin123`

### Frontend Setup

1. Navigate to frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. (Optional) Create `.env` file:
```env
VITE_API_URL=http://localhost:5000/api
```

4. Start the development server:
```bash
npm run dev
```

## Usage

1. **Register/Login**: Create an account with role (user, owner, or admin)
2. **User Dashboard**: 
   - Enter battery percentage and destination distance
   - View route calculation results
   - See charging stations on map
3. **Owner Dashboard**:
   - Apply for verification (if not verified)
   - Add, edit, delete your charging stations
4. **Admin Dashboard**:
   - Review and approve/reject owner applications
   - Monitor all stations
   - Approve pending stations

## API Endpoints

### Auth
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user

### Stations
- `GET /api/stations` - Get all verified stations
- `POST /api/stations` - Create station (Owner only)
- `PUT /api/stations/:id` - Update station (Owner only)
- `DELETE /api/stations/:id` - Delete station (Owner only)
- `GET /api/stations/my-stations` - Get owner's stations

### Owner
- `POST /api/owner/apply` - Apply for verification
- `GET /api/owner/status` - Get application status

### Admin
- `GET /api/admin/owners` - Get all owner applications
- `PUT /api/admin/owners/:id/approve` - Approve owner
- `PUT /api/admin/owners/:id/reject` - Reject owner
- `GET /api/admin/stations` - Get all stations
- `PUT /api/admin/stations/:id/approve` - Approve station

## Notes

- **In-memory storage**: All data is stored in memory and will be lost when the server restarts. Perfect for development and testing!
- Map view is a placeholder - integrate with Google Maps, Mapbox, or Leaflet for production
- AI-based smart routing is a placeholder for future implementation
- All stations require admin approval before appearing on public map
- Owners must be verified before they can add stations
- Default admin credentials: `admin@evsmart.com` / `admin123`

