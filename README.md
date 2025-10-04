# Supermarket Billing System (SBS)

A comprehensive Java-based supermarket billing and inventory management system with a graphical user interface built using Swing.

## 🚀 Features

### For Customers
- **User Authentication**: Secure login system for customers
- **Product Browsing**: Search and browse products by name or code
- **Shopping Cart**: Add items to cart with quantity selection
- **Real-time Updates**: View product availability and pricing
- **Billing**: Generate bills for purchased items

### For Administrators
- **Admin Dashboard**: Complete system management interface
- **Inventory Management**: Add, update, and manage product stock
- **User Management**: Manage customer accounts and admin accounts
- **Product Management**: Full CRUD operations for products
- **Sales Tracking**: Monitor and analyze sales data

## 🛠 Technology Stack

- **Language**: Java
- **GUI Framework**: Java Swing
- **Database**: MySQL
- **Development Environment**: IntelliJ IDEA

## 📋 Prerequisites

Before running this application, ensure you have the following installed:

- Java Development Kit (JDK) 8 or higher
- MySQL Server
- MySQL Connector/J (JDBC driver for MySQL)
- IntelliJ IDEA or any Java IDE

## ⚙️ Installation & Setup

### 1. Clone or Download the Project
```bash
# If using git
git clone <repository-url>
cd SBS2
```

### 2. Database Setup
1. Start your MySQL server
2. Create a new database named `supermarket_billing`
3. Run the SQL queries from `sql_queries.txt` to create tables and sample data:
   - `Products` table for inventory management
   - `c_login` table for customer accounts
   - `a_login` table for admin accounts

### 3. Configure Database Connection
Update the database connection details in `src/connection.java`:
```java
// Modify these parameters according to your MySQL setup
String url = "jdbc:mysql://localhost:3306/supermarket_billing";
String username = "your_mysql_username";
String password = "your_mysql_password";
```

### 4. Set Up Dependencies
Ensure MySQL Connector/J JAR is added to your project classpath:
- Download from: https://dev.mysql.com/downloads/connector/j/
- Add to project libraries in your IDE

## 🚀 Running the Application

### Option 1: Using IDE (Recommended)
1. Open the project in IntelliJ IDEA
2. Ensure all dependencies are properly configured
3. Run `src/Main.java`

### Option 2: Using Command Line
```bash
# Compile the Java files
javac -cp "path/to/mysql-connector.jar" src/*.java

# Run the main class
java -cp ".:path/to/mysql-connector.jar" Main
```

## 📱 How to Use

### Starting the Application
1. Run the application - you'll see the Dashboard
2. Choose between **Administrator** or **Customer** login

### For Customers:
1. Login with your credentials or sign up for a new account
2. Browse products using the search functionality
3. Add items to your cart
4. Proceed to checkout for billing

### For Administrators:
1. Login with admin credentials
2. Access the admin panel to manage inventory
3. Add new products, update stock, and manage users
4. View sales reports and system analytics

## 🗂 Project Structure

```
SBS2/
├── src/
│   ├── Main.java           # Application entry point
│   ├── Dashboard.java      # Main dashboard interface
│   ├── Login.java          # User authentication
│   ├── Signin.java         # User registration
│   ├── Customer.java       # Customer interface and functionality
│   ├── Admin.java          # Administrator interface
│   ├── Stock.java          # Inventory management
│   ├── Bill.java           # Billing system
│   ├── Cart.java           # Shopping cart functionality
│   ├── connection.java     # Database connection handler
│   ├── showTable.java      # Table display utilities
│   ├── sqlQuery.java       # Database query operations
│   └── ...                 # Other supporting classes
├── sql_queries.txt         # Database setup queries
├── .gitignore             # Git ignore file
└── README.md              # This file
```

## 🔧 Key Classes and Components

- **Main.java**: Application entry point that launches the Dashboard
- **Dashboard.java**: Main interface allowing users to choose between Admin and Customer modes
- **Customer.java**: Handles customer-side operations including product browsing and cart management
- **Admin.java**: Manages administrative functions like inventory control and user management
- **Stock.java**: Handles product inventory operations
- **Bill.java**: Manages billing and invoice generation
- **connection.java**: Establishes and manages database connections

## 🔒 Security Features

- Input validation for user registration and login
- Password protection for admin functions
- SQL injection prevention through parameterized queries
- Session management for user authentication

## 🚧 Troubleshooting

### Common Issues:

1. **Database Connection Error**:
   - Verify MySQL server is running
   - Check connection credentials in `connection.java`
   - Ensure database `supermarket_billing` exists

2. **JDBC Driver Not Found**:
   - Add MySQL Connector/J to classpath
   - Check JAR file path in project configuration

3. **Port Already in Use**:
   - Change the port in MySQL configuration
   - Update connection URL accordingly

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Authors

- **Parth Lad** - *Initial work and development*

## 🙏 Acknowledgments

- Thanks to the Java Swing team for the excellent GUI framework
- MySQL team for the robust database solution
- IntelliJ IDEA for the development environment

## 📞 Support

For support and questions, please contact:
- Email: parth@gmail.com
- Project Repository: [Repository Link]

---

**Note**: Make sure to update the database credentials and server configurations according to your local setup before running the application.
