# 🛒 ShopNow — E-Commerce Frontend

> A modern, responsive e-commerce web application built with React.js featuring product browsing, cart management, user authentication, and Stripe payment integration.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Project Structure](#project-structure)
- [Application Flow](#application-flow)
- [Pages & Components](#pages--components)
- [Getting Started](#getting-started)
- [API Integration](#api-integration)
- [Screenshots](#screenshots)

---

## 📖 Overview

ShopNow Frontend is a React.js based e-commerce web application that connects with the ShopNow Spring Boot backend. It provides a complete shopping experience — from browsing products to placing orders with payment.

**Live App:** `http://localhost:5173`  
**Backend API:** `http://localhost:8080`

---

## 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| React.js 18 | Frontend Framework |
| Vite | Build Tool & Dev Server |
| React Router | Client Side Routing |
| Redux Toolkit | State Management |
| Axios | HTTP Client for API calls |
| TailwindCSS | Utility-first CSS Styling |
| Stripe.js | Payment Integration |
| React Hot Toast | Notifications |

---

## ✨ Features

- **Product Listing** — Browse all products with search and filter
- **Category Filter** — Filter products by category
- **Sort Products** — Sort by price, name etc.
- **Product Detail** — Detailed product view
- **User Authentication** — Register and Login
- **Shopping Cart** — Add, update, remove items
- **Checkout Flow** — Complete order placement
- **Stripe Payment** — Secure payment processing
- **Order Tracking** — Track order status
- **Admin Panel** — Manage products, categories, orders, sellers
- **Responsive Design** — Works on all screen sizes

---

## 📁 Project Structure

```
shopnow-frontend/
│
├── public/                          # Static assets
│   └── vite.svg
│
├── src/
│   ├── assets/                      # Images and static files
│   │
│   ├── components/                  # Reusable UI Components
│   │   ├── Navbar.jsx               # Top navigation bar
│   │   ├── Footer.jsx               # Footer component
│   │   ├── ProductCard.jsx          # Individual product card
│   │   ├── CartItem.jsx             # Cart item component
│   │   ├── Pagination.jsx           # Pagination component
│   │   └── Loader.jsx               # Loading spinner
│   │
│   ├── pages/                       # Page Components
│   │   ├── Home.jsx                 # Landing/Home page
│   │   ├── Products.jsx             # All products listing
│   │   ├── ProductDetail.jsx        # Single product detail
│   │   ├── Cart.jsx                 # Shopping cart page
│   │   ├── Checkout.jsx             # Checkout page
│   │   ├── Login.jsx                # Login page
│   │   ├── Register.jsx             # Registration page
│   │   ├── Orders.jsx               # User orders page
│   │   ├── About.jsx                # About page
│   │   └── Contact.jsx              # Contact page
│   │
│   ├── admin/                       # Admin Panel Pages
│   │   ├── Dashboard.jsx            # Admin dashboard
│   │   ├── AdminProducts.jsx        # Manage products
│   │   ├── AdminCategories.jsx      # Manage categories
│   │   ├── AdminOrders.jsx          # Manage orders
│   │   └── AdminSellers.jsx         # Manage sellers
│   │
│   ├── store/                       # Redux Store
│   │   ├── store.js                 # Redux store config
│   │   └── slices/
│   │       ├── authSlice.js         # Auth state
│   │       ├── cartSlice.js         # Cart state
│   │       └── productSlice.js      # Products state
│   │
│   ├── api/                         # API service files
│   │   └── axiosInstance.js         # Axios configuration
│   │
│   ├── App.jsx                      # Root component with routes
│   ├── main.jsx                     # Entry point
│   └── index.css                    # Global styles
│
├── index.html                       # HTML entry point
├── vite.config.js                   # Vite configuration
├── package.json                     # Dependencies
├── tailwind.config.js               # Tailwind configuration
└── README.md
```

---

## 🔄 Application Flow

```
┌─────────────────────────────────────────────────────────┐
│                    USER JOURNEY                         │
└─────────────────────────────────────────────────────────┘

  [Home Page]
       │
       ▼
  [Browse Products] ──── Search/Filter/Sort
       │
       ▼
  [Product Detail]
       │
       ▼
  [Add to Cart] ──── [Login Required?] ──▶ [Login/Register]
       │                                           │
       │◀─────────────────────────────────────────┘
       ▼
  [Cart Page] ──── Update Qty / Remove Items
       │
       ▼
  [Checkout Page]
       │
       ├──▶ [Enter Address]
       │
       ├──▶ [Select Payment Method]
       │
       └──▶ [Stripe Payment]
                  │
                  ▼
           [Order Placed ✅]
                  │
                  ▼
           [Order Tracking]


┌─────────────────────────────────────────────────────────┐
│                   ADMIN JOURNEY                         │
└─────────────────────────────────────────────────────────┘

  [Admin Login]
       │
       ▼
  [Admin Dashboard]
       │
       ├──▶ [Manage Categories] ── Add / Edit / Delete
       │
       ├──▶ [Manage Products] ── Add / Edit / Delete / Image
       │
       ├──▶ [Manage Orders] ── View / Update Status
       │
       └──▶ [Manage Sellers] ── View all sellers
```

---

## 📱 Pages & Components

### Public Pages
| Page | Route | Description |
|------|-------|-------------|
| Home | `/` | Landing page with hero slider and featured products |
| Products | `/products` | All products with search, filter, sort |
| Product Detail | `/products/:id` | Single product with details and add to cart |
| About | `/about` | About the platform |
| Contact | `/contact` | Contact information |
| Login | `/login` | User login form |
| Register | `/register` | New user registration |

### Protected Pages (Login Required)
| Page | Route | Description |
|------|-------|-------------|
| Cart | `/cart` | Shopping cart management |
| Checkout | `/checkout` | Order placement and payment |
| Orders | `/orders` | User order history |
| Profile | `/profile` | User profile management |

### Admin Pages (Admin Role Required)
| Page | Route | Description |
|------|-------|-------------|
| Dashboard | `/admin` | Admin overview |
| Categories | `/admin/categories` | Category management |
| Products | `/admin/products` | Product management |
| Orders | `/admin/orders` | Order management |
| Sellers | `/admin/sellers` | Seller management |

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn
- ShopNow Backend running on port 8080

### Step 1 — Clone the Repository
```bash
git clone https://github.com/Sushrut-Kadate/shopnow-frontend.git
cd shopnow-frontend
```

### Step 2 — Install Dependencies
```bash
npm install
```

### Step 3 — Run Development Server
```bash
npm run dev
```

### Step 4 — Open in Browser
```
http://localhost:5173
```

> ⚠️ Make sure ShopNow Backend is running on port 8080 before starting frontend!

---

## 🔗 API Integration

Frontend connects to backend via Axios. Base URL is configured as:

```javascript
const axiosInstance = axios.create({
  baseURL: 'http://localhost:8080',
  withCredentials: true  // Important for JWT cookie
});
```

### Key API Calls:

```javascript
// Get all products
GET http://localhost:8080/api/public/products

// Login
POST http://localhost:8080/api/auth/signin

// Add to cart
POST http://localhost:8080/api/carts/products/{productId}/quantity/{qty}

// Place order
POST http://localhost:8080/api/order/users/payments/{paymentMethod}
```

---

## ⚙️ Build for Production

```bash
npm run build
```

Build output will be in the `dist/` folder.

---

## 🔧 Environment Notes

- Frontend runs on: **http://localhost:5173**
- Backend API: **http://localhost:8080**
- JWT stored in HTTP Cookie named `springBootEcom`
- CORS configured to allow `http://localhost:5173`

---

## 👨‍💻 Author

**Sushrut Kadate**
- GitHub: [@Sushrut-Kadate](https://github.com/Sushrut-Kadate)

---

## 📄 License

This project is for educational purposes.
