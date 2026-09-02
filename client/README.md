# Vanta Ecomm

> A modern full-stack fashion e-commerce platform for discovering and purchasing curated fashion and accessories across **Dresses, Tops, Bags, Footwear, and Jewelry**.

Vanta Ecomm is a production-style e-commerce frontend built with React and designed around a clean, premium shopping experience. It includes product discovery, category collections, search and filtering, authentication, wishlist and cart functionality, checkout, order management, customer accounts, and a dedicated admin dashboard.

The frontend communicates with a REST API backend for authentication, products, categories, orders, addresses, reviews, payments, and administration.

---

## ✨ Features

### 🛍️ Shopping Experience

* Browse products across multiple fashion categories
* Dedicated category collections
* Product detail pages
* Product search
* Filtering and sorting
* Pagination
* Wishlist
* Shopping cart
* Recently viewed products
* Responsive product grids
* Collection benefits and promotional sections
* Light and dark theme support

### 👤 Customer Account

* User registration and login
* Authentication state management
* Customer account dashboard
* Saved addresses
* Order history
* Individual order details
* Checkout flow
* Order confirmation
* Protected customer routes

### 💳 Checkout & Orders

* Address selection and management
* Contact information
* Order summary
* Payment selection
* Razorpay payment integration through the backend
* Order creation
* Order success page
* Order tracking/details

### 🔐 Authentication & Security

* JWT-based authentication
* Protected routes
* Customer/admin access separation
* Centralized authentication state
* Error handling
* API service abstraction

### 🛠️ Admin Dashboard

* Admin authentication and route protection
* Dashboard
* Product management
* Product creation and editing
* Product listing
* Order management
* Order details
* Administrative workflows

---

## 🧰 Tech Stack

### Frontend

| Technology          | Purpose                       |
| ------------------- | ----------------------------- |
| **React 19**        | UI development                |
| **Vite**            | Development and build tooling |
| **React Router**    | Client-side routing           |
| **Zustand**         | Application state management  |
| **Axios**           | REST API communication        |
| **React Hook Form** | Form management               |
| **Tailwind CSS**    | Styling and responsive UI     |
| **Recharts**        | Admin analytics               |
| **Lucide React**    | Interface icons               |
| **React Hot Toast** | Notifications                 |

### Backend Integration

The frontend consumes a REST API powered by:

* Node.js
* Express
* MongoDB
* Mongoose
* JWT
* Zod
* Razorpay
* Cloudinary

---

## 🏗️ Architecture

```text
┌───────────────────────────────┐
│          Vanta Ecomm          │
│        React Frontend         │
└───────────────┬───────────────┘
                │
                │ REST API
                ▼
┌───────────────────────────────┐
│        Node.js + Express      │
│          Backend API          │
└───────────────┬───────────────┘
                │
        ┌───────┴────────┐
        ▼                ▼
┌──────────────┐  ┌──────────────┐
│   MongoDB    │  │  Cloudinary  │
│  Data Store  │  │ Product Media│
└──────────────┘  └──────────────┘

                │
                ▼
        ┌──────────────┐
        │   Razorpay   │
        │   Payments   │
        └──────────────┘
```

---

## 📁 Project Structure

```text
src/
├── assets/
│   └── category/
│
├── components/
│   ├── admin/
│   ├── checkout/
│   ├── collection/
│   ├── navbar/
│   ├── products/
│   ├── AdminRoute.jsx
│   ├── AuthModal.jsx
│   ├── ErrorBoundary.jsx
│   ├── Footer.jsx
│   ├── Navbar.jsx
│   └── ToastProvider.jsx
│
├── constants/
│
├── context/
│
├── data/
│   ├── categoryHeroes.js
│   └── storeCategories.js
│
├── hooks/
│   ├── useCheckout.js
│   └── useProductCollection.js
│
├── layouts/
│   ├── AdminLayout.jsx
│   └── MainLayout.jsx
│
├── pages/
│   ├── admin/
│   ├── About.jsx
│   ├── Account.jsx
│   ├── Addresses.jsx
│   ├── Cart.jsx
│   ├── Category.jsx
│   ├── Checkout.jsx
│   ├── Home.jsx
│   ├── Login.jsx
│   ├── OrderDetails.jsx
│   ├── Orders.jsx
│   ├── OrderSuccess.jsx
│   ├── ProductDetails.jsx
│   ├── Products.jsx
│   ├── RecentlyViewed.jsx
│   └── Wishlist.jsx
│
├── services/
├── store/
├── styles/
├── utils/
│
├── App.jsx
├── index.css
└── main.jsx
```

---

## 🧭 Application Routes

### Storefront

| Route              | Description              |
| ------------------ | ------------------------ |
| `/`                | Homepage                 |
| `/products`        | Product collection       |
| `/products/:slug`  | Product details          |
| `/category`        | Category overview        |
| `/category/:slug`  | Category collection      |
| `/about`           | About Vanta Ecomm        |
| `/cart`            | Shopping cart            |
| `/wishlist`        | Wishlist                 |
| `/recently-viewed` | Recently viewed products |

### Customer

| Route                     | Description           |
| ------------------------- | --------------------- |
| `/login`                  | Customer login        |
| `/register`               | Customer registration |
| `/account`                | Account dashboard     |
| `/account/addresses`      | Saved addresses       |
| `/account/orders`         | Order history         |
| `/orders/:id`             | Order details         |
| `/checkout`               | Checkout              |
| `/order-success/:orderId` | Order confirmation    |

### Admin

| Route               | Description         |
| ------------------- | ------------------- |
| `/admin`            | Admin dashboard     |
| `/admin/products`   | Product management  |
| `/admin/orders`     | Order management    |
| `/admin/orders/:id` | Admin order details |

---

## 🎨 Design Philosophy

Vanta Ecomm is designed around a **premium fashion retail aesthetic** rather than a generic marketplace interface.

The frontend focuses on:

* Clean typography
* Editorial-style layouts
* Product-first presentation
* Responsive design
* Minimal interface elements
* Clear shopping flows
* Consistent spacing and visual hierarchy
* Light/dark theme support
* Mobile-friendly navigation

The goal is to create a shopping experience that feels closer to a curated fashion storefront than a traditional catalogue application.

---

## ⚙️ Getting Started

### Prerequisites

Make sure you have installed:

* Node.js 18+
* npm
* Git

The Vanta Ecomm backend must also be running for product, authentication, cart, order, and checkout functionality.

---

### 1. Clone the Repository

```bash
git clone https://github.com/sharmarujula123-gif/vanta-bags-ecomm.git

cd vanta-bags-ecomm
```

> Update the repository URL after renaming the GitHub repository to `vanta-ecomm`.

---

### 2. Install Dependencies

```bash
npm install
```

---

### 3. Configure Environment Variables

Create a `.env` file in the frontend root:

```env
VITE_API_URL=http://localhost:5000/api
```

Use the URL of your deployed backend when running the application in production.

---

### 4. Start Development Server

```bash
npm run dev
```

Vite will start the development server and provide the local application URL.

---

## 🏭 Production Build

Create an optimized production build:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

---

## 🧪 Code Quality

Run ESLint with:

```bash
npm run lint
```

The project uses ESLint to maintain consistent code quality and identify potential issues during development.

---

## 🔌 API Integration

Frontend API communication is separated into service modules rather than being tightly coupled to individual components.

The frontend uses Axios to communicate with the backend REST API.

Typical API areas include:

```text
Authentication
Products
Categories
Cart
Wishlist
Orders
Addresses
Reviews
Payments
Admin
```

This separation makes the frontend easier to maintain and allows backend services to evolve independently.

---

## 🔐 Authentication Flow

```text
User
 │
 ▼
Login / Register
 │
 ▼
Authentication API
 │
 ▼
JWT Authentication
 │
 ▼
Frontend Auth Store
 │
 ├── Customer Routes
 │
 └── Admin Routes
```

Protected routes are handled through authentication and admin route guards.

---

## 📱 Responsive Design

The interface is designed to work across:

* Desktop
* Laptop
* Tablet
* Mobile

Responsive layouts are implemented using Tailwind CSS and dedicated mobile navigation components.

---

## 🚀 Deployment

The frontend can be deployed to modern hosting platforms that support Vite applications.

Before deployment:

1. Configure the production `VITE_API_URL`
2. Verify the backend is publicly accessible
3. Test authentication
4. Test product loading
5. Test cart functionality
6. Test checkout and payment flow
7. Verify protected routes
8. Run the production build

```bash
npm run build
```

---

## 🔮 Future Improvements

Potential improvements for future versions include:

* Advanced product recommendations
* Product reviews and ratings UI improvements
* Coupon and promotional-code support
* Enhanced inventory indicators
* Advanced admin analytics
* Order status notifications
* Product comparison
* Improved accessibility
* SEO optimization
* Performance optimization
* Progressive Web App support

---

## 👨‍💻 Project Purpose

Vanta Ecomm was developed as a full-stack portfolio project to demonstrate practical experience with:

* Modern React development
* Component-based UI architecture
* REST API integration
* State management
* Authentication and protected routes
* E-commerce workflows
* Product discovery
* Shopping cart and wishlist systems
* Checkout and payment integration
* Customer account management
* Admin dashboards
* Responsive UI development
* Frontend/backend separation

---

## 📌 Project Highlights

**Application:** Vanta Ecomm
**Type:** Full-Stack Fashion E-commerce Platform
**Frontend:** React + Vite
**State Management:** Zustand
**Styling:** Tailwind CSS
**Backend:** Node.js + Express
**Database:** MongoDB
**Authentication:** JWT
**Payments:** Razorpay
**Media:** Cloudinary
**Validation:** Zod
**Testing:** Vitest + Supertest

---

## 📄 License

This project is currently intended as a portfolio and learning project.

License information can be added here when the project is released under a specific open-source license.
