# Vanta Ecomm 🛍️

<p align="center">
  <img src="assets/vanta-ecomm.png" alt="Nexa AI" width="100%">
</p>

A modern full-stack fashion e-commerce platform for discovering and purchasing curated fashion and accessories across Dresses, Tops, Bags, Footwear, and Jewelry.

Vanta Ecomm is built with a React frontend and Node.js/Express backend, using MongoDB for persistent data, JWT-based authentication, Cloudinary for product media, and Razorpay for online payments.

---

## ✨ Features

### 🛍️ Customer Features

- User registration and login
- JWT-based authentication
- Product browsing
- Product search
- Product filtering and sorting
- Category-based collections
- Product detail pages
- Shopping cart
- Wishlist
- Recently viewed products
- Checkout
- Razorpay payment integration
- Order placement
- Order history
- Order details
- Saved customer addresses
- Product reviews
- Responsive design
- Light/Dark theme

### 👨‍💼 Admin Features

- Admin authentication and protected routes
- Admin dashboard
- Product management
- Product creation and editing
- Product image uploads
- Category management
- Order management
- Order details
- Order status management
- Sales/analytics dashboard

---

## 🛠️ Tech Stack

### Frontend

- React
- Vite
- Tailwind CSS
- React Router
- Zustand
- Axios
- React Hook Form
- Recharts
- Lucide React
- React Hot Toast

### Backend

- Node.js
- Express
- MongoDB
- Mongoose
- JWT
- bcryptjs
- Zod

### Third-Party Services

- Cloudinary - Image/media storage
- Razorpay - Payment processing

### Testing & Development

- Vitest
- Supertest
- Nodemon
- ESLint

---

## 🏗️ Architecture

```text
                    ┌─────────────────────┐
                    │      Vanta ecomm    │
                    │     React Client    │
                    └──────────┬──────────┘
                               │
                               │ REST API
                               ▼
                    ┌─────────────────────┐
                    │   Express Backend   │
                    │   Node.js + Express │
                    └──────────┬──────────┘
                               │
                 ┌─────────────┼─────────────┐
                 │             │             │
                 ▼             ▼             ▼
          ┌────────────┐ ┌───────────┐ ┌────────────┐
          │  MongoDB   │ │ Cloudinary│ │  Razorpay  │
          │  Database  │ │   Images  │ │  Payments  │
          └────────────┘ └───────────┘ └────────────┘
