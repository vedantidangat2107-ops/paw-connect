# 🐾 Paw Connect

A comprehensive pet adoption platform connecting adopters with their perfect companions.

## Features

- **For Adopters:**
  - Browse available pets
  - Filter by breed, age, size
  - Submit adoption applications
  - Track application status
  - Create favorites list
  - View pet details and images

- **For Admins:**
  - Add/edit/delete pets
  - Manage adoption applications
  - Approve/reject applications
  - View user profiles
  - Generate reports

## Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript
- **Backend:** Node.js, Express.js
- **Database:** MySQL
- **Authentication:** JWT (JSON Web Tokens)

## Installation

### Prerequisites
- Node.js (v14+)
- MySQL (v5.7+)

### Setup

1. Clone the repository
```bash
git clone https://github.com/vedantidangat2107-ops/paw-connect.git
cd paw-connect
```

2. Install dependencies
```bash
npm install
```

3. Create `.env` file
```
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=paw_connect
JWT_SECRET=your_secret_key
PORT=3000
```

4. Create database
```bash
mysql -u root -p < database/schema.sql
```

5. Start server
```bash
npm start
```

6. Open browser
```
http://localhost:3000
```

## API Endpoints

### Auth
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user

### Pets
- `GET /api/pets` - Get all pets
- `GET /api/pets/:id` - Get pet details
- `POST /api/pets` - Add new pet (Admin)
- `PUT /api/pets/:id` - Update pet (Admin)
- `DELETE /api/pets/:id` - Delete pet (Admin)

### Adoptions
- `GET /api/adoptions` - Get user's applications
- `POST /api/adoptions` - Submit application
- `GET /api/adoptions/:id` - Get application details
- `PUT /api/adoptions/:id` - Update application status (Admin)

### Admin
- `GET /api/admin/dashboard` - Admin dashboard data
- `GET /api/admin/users` - Get all users
- `GET /api/admin/stats` - Get statistics

## License

MIT License
