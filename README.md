# KNEX Finance Management System

A comprehensive finance management system for KNEX with features for booking requests, invoice management, and financial tracking.

## Features

- **Booking Requests Management**
  - Manager review and approval system
  - Automatic conversion to invoice requests
  - Print/Download booking forms as PDF with all images

- **Invoice Management**
  - Invoice request creation and tracking
  - Status workflow (Draft → Submitted → In Progress → Verified → Completed)
  - Automatic invoice generation

- **Collections & Payments**
  - Payment tracking and remittances
  - QR code payment system
  - Delivery assignments

- **Dashboard & Reports**
  - Department-specific dashboards
  - Performance metrics
  - Audit reports

## Tech Stack

### Frontend
- Next.js 15
- React 18
- TypeScript
- Tailwind CSS
- Radix UI components

### Backend
- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT Authentication

## Project Structure

```
Finance/
├── Frontend/          # Next.js frontend application
├── Backend/           # Express.js backend API
└── docs/             # Documentation files
```

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- MongoDB database
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Finance
```

2. Install Frontend dependencies:
```bash
cd Frontend
npm install
```

3. Install Backend dependencies:
```bash
cd ../Backend
npm install
```

4. Configure environment variables:
   - Create `Backend/.env` with MongoDB connection string and JWT secret
   - Create `Frontend/.env.local` with API URL

5. Run the development servers:
```bash
# Backend (from Backend directory)
npm run dev

# Frontend (from Frontend directory)
npm run dev
```

## Environment Variables

### Backend (.env)
```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=5000
FRONTEND_URL=http://localhost:9002
```

### Frontend (.env.local)
```
NEXT_PUBLIC_API_URL=http://localhost:5000/api
```

## Key Features Implemented

### Booking Requests
- Managers can review booking requests
- View customer details, receiver information, and verification images
- Review ID front/back images and face scans
- View client face images
- Display items list
- Automatic conversion to invoice requests after review
- Print/Download booking forms as PDF

### Invoice Requests
- Sales team creates invoice requests
- Operations team verifies and adds weight
- Finance team generates invoices
- Status tracking throughout workflow

## Database Collections

- `users` - User authentication
- `employees` - Employee information
- `departments` - Department data
- `clients` - Client information
- `bookings` - Booking requests
- `invoiceRequests` - Invoice requests
- `invoices` - Generated invoices
- `collections` - Payment collections

## API Endpoints

### Bookings
- `GET /api/bookings` - Get all bookings
- `GET /api/bookings/status/:reviewStatus` - Get bookings by status
- `GET /api/bookings/:id` - Get booking by ID
- `POST /api/bookings/:id/review` - Review and approve booking

### Invoice Requests
- `GET /api/invoice-requests` - Get all invoice requests
- `POST /api/invoice-requests` - Create invoice request
- `PUT /api/invoice-requests/:id` - Update invoice request

## License

Proprietary - All rights reserved

## Contact

For questions or support, please contact the development team.

