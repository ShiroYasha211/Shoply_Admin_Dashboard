# Shoply Admin Dashboard 🛍️

A modern, responsive e-commerce admin dashboard built with Flutter Web and connected to Supabase backend. This dashboard provides comprehensive management tools for products, users, orders, and analytics.

![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)

## 🌟 Features

### 🔐 Authentication
- **Secure Admin Login**: Role-based authentication system
- **Session Management**: Persistent login sessions
- **Admin-only Access**: Protected routes with middleware

### 📊 Dashboard Overview
- **Real-time Analytics**: Key metrics and statistics
- **Sales Performance**: Revenue tracking and charts
- **Quick Actions**: Fast access to common tasks

### 👥 User Management
- **User Directory**: Complete user profiles and information
- **Registration Tracking**: Monitor new user registrations
- **User Analytics**: Activity and engagement metrics

### 🛍️ Product Management
- **Product Catalog**: Full product CRUD operations
- **Inventory Tracking**: Stock levels and management
- **Category Organization**: Product categorization system
- **Search & Filter**: Advanced product search capabilities

### 📦 Order Management
- **Order Processing**: Complete order lifecycle management
- **Status Tracking**: Real-time order status updates
- **Customer Communications**: Order notifications and updates

### 📈 Analytics & Reports
- **Sales Analytics**: Comprehensive sales reporting
- **Performance Metrics**: Business intelligence dashboards
- **Data Visualization**: Interactive charts and graphs

## 🚀 Demo

### Live Demo Access
**Admin Credentials:**
- **Email:** `mohammed211@gmail.com`
- **Password:** `123456`

> **Note:** These are demo credentials for testing purposes only.

## 🛠️ Technology Stack

- **Frontend Framework:** Flutter Web
- **State Management:** GetX
- **Backend:** Supabase (PostgreSQL)
- **Authentication:** Supabase Auth
- **Charts:** FL Chart
- **UI Components:** Custom responsive widgets
- **Architecture:** Clean Architecture with MVC pattern

## 📱 Responsive Design

The dashboard is fully responsive and works seamlessly across:
- 🖥️ Desktop (1200px+)
- 💻 Laptop (768px - 1199px)
- 📱 Tablet (576px - 767px)
- 📱 Mobile (< 576px)

## 🏗️ Project Structure

```
lib/
├── app/
│   ├── controllers/           # Global controllers
│   │   └── auth_controller.dart
│   ├── core/
│   │   ├── constants/         # App constants
│   │   ├── middleware/        # Route middleware
│   │   ├── services/          # Core services
│   │   └── values/           # Theme and styling
│   ├── data/
│   │   ├── models/           # Data models
│   │   └── services/         # Data services
│   ├── modules/              # Feature modules
│   │   ├── dashboard/        # Dashboard module
│   │   ├── products/         # Products module
│   │   ├── users/           # Users module
│   │   ├── orders/          # Orders module
│   │   └── login/           # Authentication module
│   ├── routes/              # App routing
│   └── widgets/             # Shared widgets
└── main.dart               # App entry point
```

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (^3.0.0)
- Dart SDK (^3.0.0)
- Web browser (Chrome recommended)
- Supabase account



## 📸 Screenshots



<img width="1920" height="870" alt="Screenshot 2025-10-02 212440" src="https://github.com/user-attachments/assets/032a690f-f757-4873-bb3a-e3cb1166e18b" />

- Dashboard Overview

  <img width="1920" height="867" alt="Screenshot 2025-10-02 205645" src="https://github.com/user-attachments/assets/1be112eb-bc81-4cc5-854d-d52c8a3bd0ad" />

- Products Management

  <img width="1920" height="866" alt="Screenshot 2025-10-02 205617" src="https://github.com/user-attachments/assets/55a691e6-a557-4680-a510-d228b7b73949" />

- User Management

<img width="1920" height="870" alt="Screenshot 2025-10-02 205711" src="https://github.com/user-attachments/assets/0e3f8e03-7823-413d-a779-2a509f054203" />

- Order Processing

<img width="1920" height="865" alt="Screenshot 2025-10-02 212500" src="https://github.com/user-attachments/assets/63548ed8-c499-430b-b029-2e5775e22101" />

- Analytics Char

<img width="1920" height="869" alt="Screenshot 2025-10-02 205737" src="https://github.com/user-attachments/assets/a6b57f56-3f64-496c-a9bb-88f0a5675d47" />

- Order Details

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Development Workflow

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
