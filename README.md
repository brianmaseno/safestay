# Safe-Stay

A comprehensive apartment management system for landlords and tenants built with React and Node.js.

## Features

### For Landlords
- **Tenant Management**: View and manage tenant information
- **Bills Management**: Create, edit, and track monthly bills
- **Complaint Handling**: Receive and resolve tenant complaints
- **Rules Management**: Create and manage property rules
- **Real-time Chat**: Communicate with tenants instantly
- **PDF Generation**: Generate bills and receipts
- **Email Notifications**: Automated notifications for bills, complaints, and rules

### For Tenants
- **Dashboard**: Overview of bills, complaints, and apartment info
- **Bill Payments**: View and track rent payments
- **Complaint Submission**: Submit and track maintenance requests
- **Rules Viewing**: Access property rules and guidelines
- **Real-time Chat**: Communicate with landlord instantly
- **Receipt Download**: Download payment receipts

## Tech Stack

### Frontend
- **React 18** with Vite
- **Tailwind CSS** for styling
- **React Router** for navigation
- **Context API** for state management
- **Axios** for API calls

### Backend
- **Node.js** with Express
- **MongoDB** with Mongoose
- **JWT** for authentication
- **Socket.io** for real-time chat
- **PDFKit** for PDF generation
- **Nodemailer** for email notifications
- **bcrypt** for password hashing

## Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB database
- Gmail account for email notifications

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/brianmaseno/safestay.git
   cd safestay
   ```

2. **Install server dependencies**
   ```bash
   cd server
   npm install
   ```

3. **Install client dependencies**
   ```bash
   cd ../client
   npm install
   ```

4. **Environment Configuration**
   Create a `.env` file in the server directory:
   ```env
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   EMAIL_USER=your_gmail_address
   EMAIL_PASSWORD=your_gmail_app_password
   ```

5. **Start the application**
   
   **Start the server:**
   ```bash
   cd server
   npm start
   ```
   
   **Start the client (in a new terminal):**
   ```bash
   cd client
   npm run dev
   ```

6. **Access the application**
   - Frontend: `http://localhost:5173`
   - Backend API: `http://localhost:5000`

## Project Structure

```
safestay/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── contexts/       # Context providers
│   │   ├── pages/          # Application pages
│   │   └── services/       # API services
│   └── ...
├── server/                 # Node.js backend
│   ├── controllers/        # Business logic
│   ├── models/            # Database models
│   ├── routes/            # API routes
│   ├── middleware/        # Custom middleware
│   ├── services/          # Email and other services
│   └── utils/             # Utility functions
└── ...
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login

### Users
- `GET /api/users/profile` - Get user profile
- `GET /api/users/tenants` - Get all tenants (Landlord only)

### Bills
- `GET /api/bills` - Get bills
- `POST /api/bills` - Create new bill
- `PUT /api/bills/:id` - Update bill
- `POST /api/bills/:id/pay` - Pay bill

### Complaints
- `GET /api/complaints` - Get complaints
- `POST /api/complaints` - Create complaint
- `PUT /api/complaints/:id` - Update complaint status

### Rules
- `GET /api/rules` - Get property rules
- `POST /api/rules` - Create rules
- `PUT /api/rules/:id` - Update rules

### Chat
- `GET /api/chat/conversations` - Get conversations
- `POST /api/chat` - Create/send message
- `GET /api/chat/:partnerId` - Get conversation messages

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.

## Author

**Brian Maseno**
- GitHub: [@brianmaseno](https://github.com/brianmaseno)
- Email: brianmaseno@gmail.com

## Support

For support, please open an issue in the GitHub repository or contact the author directly.
