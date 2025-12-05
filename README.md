# 🎨 AI Text-to-Image Generation Platform

A full-stack MERN application that transforms text prompts into stunning AI-generated images using the Clipdrop API. Features user authentication, credit-based system, and integrated payment processing.

## 🌟 Features

- **AI Image Generation** - Convert text descriptions into high-quality images using Clipdrop API
- **User Authentication** - Secure JWT-based registration and login system
- **Credit System** - 5 free credits for new users, 1 credit per image generation
- **Payment Integration** - Razorpay payment gateway with three pricing tiers
- **Responsive Design** - Mobile-friendly UI with smooth Framer Motion animations
- **Download Images** - Save generated images directly to your device
- **Protected Routes** - Secure middleware-protected API endpoints

## 🚀 Demo

[Live Demo Link](https://text-image-generation-ai-website-frontend.onrender.com/)

## 🛠️ Tech Stack

### Frontend
- **React.js** - UI library
- **Vite** - Build tool
- **Tailwind CSS** - Styling
- **Framer Motion** - Animations
- **Axios** - HTTP requests
- **React Router** - Navigation
- **Context API** - State management

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **JWT** - Authentication
- **Bcrypt.js** - Password hashing
- **Razorpay** - Payment gateway
- **Clipdrop API** - AI image generation

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js (v14 or higher)
- MongoDB installed and running
- Clipdrop API key
- Razorpay account (Key ID & Secret)

## ⚙️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/Harsha120903/Text-Image-Generation-AI-website.git
cd Text-Image-Generation-AI-website
```

### 2. Backend Setup
```bash
cd server
npm install
```

Create `.env` file in server directory:
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLIPDROP_API=your_clipdrop_api_key
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_secret
CURRENCY=INR
```

Start backend server:
```bash
npm start
```

### 3. Frontend Setup
```bash
cd client
npm install
```

Create `.env` file in client directory:
```env
VITE_BACKEND_URL=http://localhost:4000
VITE_RAZORPAY_KEY_ID=your_razorpay_key_id
```

Start frontend development server:
```bash
npm run dev
```

## 📁 Project Structure
```
Text-Image-Generation-AI-website/
├── server/
│   ├── config/
│   │   └── mongodb.js
│   ├── controllers/
│   │   ├── imageController.js
│   │   └── userController.js
│   ├── middlewares/
│   │   └── auth.js
│   ├── models/
│   │   ├── userModel.js
│   │   └── transactionModel.js
│   ├── routes/
│   │   ├── imageRoutes.js
│   │   └── userRoutes.js
│   └── server.js
│
├── client/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── Header.jsx
│   │   │   ├── Login.jsx
│   │   │   └── ...
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Result.jsx
│   │   │   └── BuyCredit.jsx
│   │   ├── context/
│   │   │   └── AppContext.jsx
│   │   └── App.jsx
│   └── package.json
│
└── README.md
```

## 🔑 API Endpoints

### User Routes
| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/api/user/register` | User registration | No |
| POST | `/api/user/login` | User login | No |
| GET | `/api/user/credits` | Get user credits | Yes |
| POST | `/api/user/pay-razor` | Initiate payment | Yes |
| POST | `/api/user/verify-razor` | Verify payment | Yes |

### Image Routes
| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/api/image/generate-image` | Generate AI image | Yes |

## 💳 Pricing Plans

| Plan | Credits | Price |
|------|---------|-------|
| Basic | 100 | $10 |
| Advanced | 500 | $50 |
| Business | 5000 | $250 |

## 🔐 Security Features

- **Password Hashing** - Bcrypt with salt rounds
- **JWT Authentication** - Secure token-based auth
- **Protected Routes** - Middleware validation
- **Payment Verification** - Server-side Razorpay verification
- **Environment Variables** - Secure API key storage

## 🎯 Key Functionalities

### User Flow
1. User registers/logs in
2. Receives 5 free credits
3. Enters text prompt for image generation
4. System deducts 1 credit and generates image
5. User can download the generated image
6. When credits run out, redirected to pricing page
7. Purchase credits via Razorpay
8. Credits automatically added after successful payment

### Payment Flow
1. User selects pricing plan
2. Backend creates transaction record
3. Razorpay order created
4. User completes payment
5. Backend verifies payment with Razorpay
6. Credits added to user account
7. Transaction marked as paid

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 👨‍💻 Author

**Harsha**
- GitHub: [@Harsha120903](https://github.com/Harsha120903)
- LinkedIn: [K Harshavardhan Reddy](https://www.linkedin.com/in/harsha1209/)

## 🙏 Acknowledgments

- [Clipdrop API](https://clipdrop.co/) for AI image generation
- [Razorpay](https://razorpay.com/) for payment processing
- [Framer Motion](https://www.framer.com/motion/) for animations
- [Tailwind CSS](https://tailwindcss.com/) for styling

## 📧 Contact

For any queries or support, please reach out:
- Email: kharsha122231@gmail.com
- Project Link: [https://github.com/Harsha120903/Text-Image-Generation-AI-website](https://github.com/Harsha120903/Text-Image-Generation-AI-website)

---

⭐ If you found this project helpful, please give it a star!
