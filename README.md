# 🛒 E-Commerce Backend API

A scalable and modular E-commerce backend built using Django, Django REST Framework (DRF), and PostgreSQL.

The system follows clean architecture principles with separate user and admin APIs, JWT authentication, pagination, business rule validations, and transaction-safe order processing.

---

## 🚀 Tech Stack

- Python
- Django
- Django REST Framework (DRF)
- PostgreSQL
- JWT Authentication
- DRF Pagination

---

## 🏗 Project Architecture

- Modular Django App Structure
- Separate `user_urls` and `admin_urls`
- RESTful API Design
- Role-based Access Control
- JWT-based Authentication
- Pagination for large datasets
- Transaction-safe Order Processing
- Business Rule Enforcement

---

## 📌 Modules & Features

### 🔐 Accounts Module
- User Registration & Login
- JWT Authentication
- Role-based Authorization (User / Admin)
- Secure Password Handling

---

### 🗂 Category Module
- Category CRUD Operations
- Category-based Product Filtering
- Admin Category Management

---

### 🛍 Products Module
- Product CRUD Operations
- Product Listing, Search & Filtering
- Paginated Product Listings
- Category Association
- Admin Product Control

---

### 🛒 Cart Module
- Add / Remove Products
- Quantity Management
- Persistent Cart Handling

---

### ❤️ Wishlist Module
- Add / Remove Wishlist Items
- User-specific Wishlist Storage

---

### ⭐ Reviews Module
- Users can add reviews only after order status is **Delivered**
- Rating System
- Review Validation
- Prevent duplicate reviews per user

---

### 💳 Payment Module
- Payment Integration
- Secure Transaction Handling
- Order-linked Payment Processing

---

### 📦 Orders Module
- Order Creation
- Order History
- Order Status Tracking:
  - Pending
  - Shipped
  - Delivered
- Controlled Order Lifecycle Flow
- Transaction-based Order Processing

---

## 🛠 Admin Module (Advanced Controls)

- Separate Admin APIs (`admin_views`)
- Revenue & Sales Analytics
- Active Users Monitoring
- Order Status Management (Pending → Shipped → Delivered)
- Business Rule Enforcement:
  - Users with pending orders cannot be blocked
  - Admin cannot block another Admin
- Role-based Access Control
- Dashboard Statistics APIs

---

## 📊 Admin Dashboard Capabilities

- Total Revenue Calculation (Django ORM Aggregation)
- Order Statistics
- Active Users Tracking
- Product Performance Insights

---

## 🛣 API Routing Structure

The project uses modular URL configuration for scalability and maintainability.

### Root URLs

- `/admin/` → Django Admin Panel
- `/api/accounts/` → Authentication & Account Management

---

### User APIs

- `/api/products/`
- `/api/cart/`
- `/api/wishlist/`
- `/api/orders/`
- `/api/payments/`
- `/api/reviews/`

---

### Admin APIs

- `/api/admin/products/`
- `/api/admin/orders/`
- `/api/admin/dashboard/`

Admin and User logic are separated using dedicated `user_urls` and `admin_urls`.

---

## 🗄 Database

- PostgreSQL
- Optimized queries using Django ORM
- Aggregations for revenue calculation
- Transaction handling for safe order processing

---

## 🔐 Authentication & Security

- JWT Authentication
- Role-based Permissions
- Protected Admin Routes
- Secure Order Transactions
- Business Logic Validations

---

## 📄 Pagination

- Implemented using DRF Pagination
- Optimized large dataset responses
- Page-based API responses for products & orders

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/sreenandpk/ecommerce-backend.git
cd ecommerce-backend
```
### 2️⃣ Create virtual environment
```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
```
### 3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```
### 4️⃣ Configure Environment Variables
Create a .env file and add:
```bash
SECRET_KEY=your_secret_key
DEBUG=True
DATABASE_NAME=your_db_name
DATABASE_USER=your_db_user
DATABASE_PASSWORD=your_db_password
DATABASE_HOST=localhost
DATABASE_PORT=5432
```
5️⃣ Run migrations
```bash
python manage.py makemigrations
python manage.py migrate
```
6️⃣ Run server
```bash
python manage.py runserver
```
👨‍💻 Author

Sreenand P K
Full-Stack Developer
Django | DRF | PostgreSQL | React | Redux
