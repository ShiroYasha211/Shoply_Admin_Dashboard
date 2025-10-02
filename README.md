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

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/shoply-admin-dashboard.git
cd shoply-admin-dashboard
```

2. **Install dependencies**
```bash
flutter pub get
```

3. **Configure Supabase**
   
   Update the Supabase configuration in `lib/app/core/constants/supabase_constants.dart`:
```dart
class SupabaseConstants {
  static const String supabaseUrl = 'YOUR_SUPABASE_URL';
  static const String supabaseAnonKey = 'YOUR_SUPABASE_ANON_KEY';
}
```

4. **Run the application**
```bash
flutter run -d chrome --web-renderer html
```

### Database Setup

The application expects the following Supabase tables:

#### Users Table (`profiles`)
```sql
CREATE TABLE profiles (
  id UUID REFERENCES auth.users ON DELETE CASCADE,
  email TEXT,
  name TEXT,
  role TEXT DEFAULT 'user',
  created_at TIMESTAMP DEFAULT NOW(),
  PRIMARY KEY (id)
);
```

#### Products Table
```sql
CREATE TABLE products (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  name TEXT NOT NULL,
  description TEXT,
  price DECIMAL(10,2) NOT NULL,
  stock INTEGER DEFAULT 0,
  category TEXT,
  image_url TEXT,
  created_at TIMESTAMP DEFAULT NOW()
);
```

#### Orders Table
```sql
CREATE TABLE orders (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  customer_id UUID REFERENCES profiles(id),
  total_amount DECIMAL(10,2) NOT NULL,
  status TEXT DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT NOW()
);
```

## 🔧 Configuration

### Environment Setup

1. Create a Supabase project at [supabase.com](https://supabase.com)
2. Copy your project URL and anon key
3. Update the constants file with your credentials
4. Set up the required database tables
5. Create an admin user with role 'admin'

### Admin User Setup

To create your first admin user:

1. Go to your Supabase project dashboard
2. Navigate to Authentication > Users
3. Create a new user or update an existing user
4. In the `profiles` table, set the `role` field to 'admin'

## 📸 Screenshots

> **Note:** Add screenshots of your dashboard here to showcase the UI

- Dashboard Overview
- Products Management
- User Management
- Order Processing
- Analytics Charts

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Development Workflow

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/shoply-admin-dashboard/issues) page
2. Create a new issue with detailed description
3. Contact the maintainers

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- Supabase for the powerful backend solution
- GetX community for state management
- All contributors and supporters

---

**Built with ❤️ using Flutter & Supabase**
