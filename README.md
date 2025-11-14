
# 🏨 BookingHub - Next-Generation Hotel Reservation Platform

<div align="center">

![BookingHub Logo](https://img.shields.io/badge/BookingHub-Hotel%20Reservations-blue?style=for-the-badge&logo=hotel)

[![React](https://img.shields.io/badge/React-18.0.0-61DAFB?style=flat-square&logo=react)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-Express-339933?style=flat-square&logo=node.js)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?style=flat-square&logo=mongodb)](https://mongodb.com/)
[![Stripe](https://img.shields.io/badge/Stripe-Payments-008CDD?style=flat-square&logo=stripe)](https://stripe.com/)
[![JWT](https://img.shields.io/badge/JWT-Authentication-000000?style=flat-square&logo=jsonwebtokens)](https://jwt.io/)

*Revolutionizing hotel bookings with cutting-edge technology and seamless user experience*

[🚀 Live Demo](#) | [📖 Documentation](#features) | [🛠️ Installation](#installation) | [🤝 Contributing](#contributing)

</div>

---

## 🌟 Overview

BookingHub is a full-stack hotel reservation platform that combines modern web technologies to deliver an exceptional booking experience. Built with performance, security, and user experience at its core, this application showcases enterprise-level architecture and innovative features.

### ✨ What Makes BookingHub Special

- **🎯 Smart Search**: Advanced filtering and real-time availability checking
- **💳 Secure Payments**: Integrated Stripe payment processing with PCI compliance
- **🔐 Robust Authentication**: JWT-based security with bcrypt password hashing
- **📱 Responsive Design**: Mobile-first approach with modern UI components
- **⚡ Real-time Updates**: Dynamic content loading and state management
- **🌐 RESTful Architecture**: Clean API design following industry standards

---

## 🚀 Features

### 🏨 Core Functionality
- **Hotel Discovery**: Browse and search hotels by location, price, and amenities
- **Room Management**: Detailed room information with availability tracking
- **Booking System**: Complete reservation workflow with date selection
- **User Profiles**: Personalized accounts with booking history
- **Rating & Reviews**: Community-driven hotel ratings and feedback

### 💼 Advanced Features
- **Payment Integration**: Secure Stripe payment processing
- **Authentication System**: JWT tokens with refresh mechanism
- **Search Context**: Persistent search state across navigation
- **Featured Properties**: Curated hotel recommendations
- **Property Categories**: Hotels, apartments, resorts, villas, and more
- **Date Range Selection**: Intuitive calendar-based booking dates

### 🔧 Technical Excellence
- **Error Handling**: Comprehensive error management and user feedback
- **API Security**: Protected routes with token verification
- **Data Validation**: Input sanitization and validation
- **Performance Optimization**: Efficient data fetching and caching
- **Responsive Design**: Cross-device compatibility

---

## 🛠️ Technology Stack

### Frontend Arsenal
```javascript
{
  "framework": "React 18.0.0",
  "routing": "React Router DOM 6.3.0",
  "ui_library": "Ant Design 5.20.5 + Material-UI 6.1.0",
  "icons": "FontAwesome 6.6.0",
  "styling": "CSS3 + React Bootstrap 2.10.4",
  "date_picker": "React Date Range 1.4.0",
  "http_client": "Axios 1.7.5",
  "payments": "Stripe React 2.8.0"
}
```

### Backend Powerhouse
```javascript
{
  "runtime": "Node.js with Express 4.19.2",
  "database": "MongoDB with Mongoose 8.6.1",
  "authentication": "JWT 9.0.2 + bcrypt 5.1.1",
  "payments": "Stripe 16.9.0",
  "security": "CORS + Cookie Parser",
  "utilities": "UUID 10.0.0 + dotenv 16.4.5"
}
```

### Development Tools
```javascript
{
  "bundler": "React App Rewired",
  "dev_server": "Nodemon 3.1.4",
  "testing": "Jest + React Testing Library",
  "polyfills": "Crypto, Buffer, Stream browserify"
}
```

---

## 📁 Project Architecture

```
BookingHub/
├── 🎨 client/                    # React Frontend
│   ├── 📦 public/
│   └── 🔧 src/
│       ├── 🧩 components/        # Reusable UI Components
│       │   ├── featured/         # Featured hotels showcase
│       │   ├── header/           # Search header component
│       │   ├── navbar/           # Navigation bar
│       │   ├── propertyList/     # Property categories
│       │   └── reserve/          # Booking modal
│       ├── 🎯 context/           # State Management
│       │   ├── AuthContext.js    # User authentication
│       │   └── SearchContext.js  # Search persistence
│       ├── 🪝 hooks/             # Custom React Hooks
│       │   └── useFetch.js       # Data fetching hook
│       └── 📄 pages/             # Route Components
│           ├── home/             # Landing page
│           ├── hotel/            # Hotel details
│           ├── list/             # Search results
│           ├── login/            # Authentication
│           └── selectedBookings/ # User bookings
│
└── 🔧 api/                       # Node.js Backend
    ├── 🎮 controllers/           # Business Logic
    │   ├── auth.js               # Authentication logic
    │   ├── booking.js            # Booking management
    │   ├── hotel.js              # Hotel operations
    │   └── user.js               # User management
    ├── 📊 models/                # Database Schemas
    │   ├── Booking.js            # Booking model
    │   ├── Hotel.js              # Hotel model
    │   ├── Room.js               # Room model
    │   └── User.js               # User model
    ├── 🛣️ routes/                # API Endpoints
    └── 🔐 utils/                 # Utilities
        ├── error.js              # Error handling
        └── verifyToken.js        # JWT verification
```

---

## ⚡ Quick Start

### Prerequisites
```bash
Node.js >= 16.0.0
MongoDB >= 4.4
npm >= 8.0.0
```

### 🚀 Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/bookings-app.git
cd bookings-app
```

2. **Backend Setup**
```bash
cd api
npm install
```

3. **Frontend Setup**
```bash
cd ../client
npm install
```

4. **Environment Configuration**

Create `.env` files:

**API (.env)**
```env
MONGO=mongodb://localhost:27017/bookingdb
JWT_SECRET=your_super_secret_jwt_key
STRIPE_SECRET_KEY=sk_test_your_stripe_secret_key
PORT=8800
```

**Client (.env)**
```env
REACT_APP_API_URL=http://localhost:8800/api
REACT_APP_STRIPE_PUBLISHABLE_KEY=pk_test_your_stripe_publishable_key
```

5. **Launch the Application**

**Terminal 1 - Backend**
```bash
cd api
npm start
```

**Terminal 2 - Frontend**
```bash
cd client
npm start
```

🎉 **Access the application at `http://localhost:3000`**

---

## 🔌 API Endpoints

### Authentication
```http
POST   /api/auth/register     # User registration
POST   /api/auth/login        # User login
POST   /api/auth/logout       # User logout
```

### Hotels
```http
GET    /api/hotels            # Get all hotels
GET    /api/hotels/:id        # Get hotel by ID
GET    /api/hotels/find/:city # Find hotels by city
GET    /api/hotels/featured   # Get featured hotels
```

### Bookings
```http
POST   /api/bookings          # Create booking
GET    /api/bookings/user/:id # Get user bookings
PUT    /api/bookings/:id      # Update booking
DELETE /api/bookings/:id      # Cancel booking
```

### Rooms
```http
GET    /api/rooms/:hotelId    # Get hotel rooms
PUT    /api/rooms/availability/:id # Update room availability
```

---

## 🎨 UI Components Showcase

### 🏠 Homepage Features
- **Hero Search**: Dynamic search with location, dates, and guest count
- **Featured Properties**: Curated hotel highlights with ratings
- **Property Types**: Visual category browsing (Hotels, Apartments, Resorts)
- **Newsletter Signup**: Email subscription with validation

### 🔍 Search & Filtering
- **Advanced Filters**: Price range, ratings, amenities
- **Real-time Results**: Instant search result updates
- **Map Integration**: Visual hotel locations
- **Sort Options**: Price, rating, distance sorting

### 🏨 Hotel Details
- **Image Gallery**: High-resolution hotel photos
- **Room Selection**: Available rooms with pricing
- **Booking Calendar**: Date range picker with availability
- **Reviews Section**: User ratings and comments

---

## 🔐 Security Features

- **🛡️ JWT Authentication**: Secure token-based authentication
- **🔒 Password Hashing**: bcrypt encryption for user passwords
- **🚫 CORS Protection**: Cross-origin request security
- **✅ Input Validation**: Comprehensive data validation
- **🔐 Protected Routes**: Middleware-based route protection
- **🍪 Secure Cookies**: HTTP-only cookie implementation

---

## 💳 Payment Integration

BookingHub integrates with **Stripe** for secure payment processing:

- **Card Payments**: Credit/debit card processing
- **Payment Intent**: Secure payment confirmation
- **Webhook Support**: Real-time payment status updates
- **PCI Compliance**: Industry-standard security
- **Multiple Currencies**: International payment support

---

## 📱 Responsive Design

- **Mobile-First**: Optimized for mobile devices
- **Tablet Support**: Enhanced tablet experience
- **Desktop Excellence**: Full-featured desktop interface
- **Cross-Browser**: Compatible with all modern browsers
- **Accessibility**: WCAG 2.1 compliance

---

## 🚀 Performance Optimizations

- **Code Splitting**: Dynamic imports for faster loading
- **Image Optimization**: Lazy loading and compression
- **API Caching**: Efficient data fetching strategies
- **Bundle Optimization**: Minimized JavaScript bundles
- **CDN Ready**: Static asset optimization

---

## 🧪 Testing Strategy

```bash
# Run frontend tests
cd client && npm test

# Run backend tests
cd api && npm test

# Coverage report
npm run test:coverage
```

---

## 🚀 Deployment

### Production Build
```bash
# Build frontend
cd client && npm run build

# Start production server
cd api && npm start
```

### Netlify Deployment
```bash
# Build and deploy frontend to Netlify
cd client
npm run build
# Deploy dist folder to Netlify
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **React Team** for the amazing framework
- **MongoDB** for the flexible database solution
- **Stripe** for secure payment processing
- **FontAwesome** for beautiful icons
- **Ant Design & Material-UI** for UI components

---

## 📞 Support & Contact

- **Issues**: [GitHub Issues](https://github.com/yourusername/bookings-app/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/bookings-app/discussions)
- **Email**: support@bookinghub.com

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

Made with ❤️ by [Your Name](https://github.com/yourusername)

</div>
