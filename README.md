# PHP Flight Management System

A comprehensive flight management web application with REST API built using PHP, MySQL, Bootstrap, and jQuery. Features user authentication, airline/city/country management, and admin dashboard.

## Features
- User Authentication & Management
- Country, City & Airline CRUD Operations
- Admin Dashboard & Settings
- RESTful API with JSON responses
- Responsive Bootstrap UI

## Technologies
- PHP 7.4+ | MySQL/MariaDB | Apache | PDO
- Bootstrap 4 | jQuery | Font Awesome
- XAMPP Development Environment

---

## Quick Start (5 Minutes)

### 1. Install & Start XAMPP

**macOS:**
```bash
sudo /Applications/XAMPP/xamppfiles/xampp start
```

**Windows:**
- Open XAMPP Control Panel
- Start Apache & MySQL (both should show green)

### 2. Copy Project to htdocs

**macOS:** `/Applications/XAMPP/xamppfiles/htdocs/IBL-FLIGHT-LAB-Complete-lab-submission`
**Windows:** `C:\xampp\htdocs\IBL-FLIGHT-LAB-Complete-lab-submission`

### 3. Create Database

1. Open http://localhost/phpmyadmin
2. Create database: `expediaflightbooking`
3. Collation: `utf8mb4_general_ci`
4. Import your SQL file (if provided)

### 4. Configure Database Connection

Edit `database/db.php`:
```php
$this->servername = "localhost";
$this->databasename = "expediaflightbooking";
$this->username = "root";
$this->password = "";  // Empty for XAMPP
```

### 5. Access Application

- **Web App:** http://localhost/IBL-FLIGHT-LAB-Complete-lab-submission/
- **Dashboard:** http://localhost/IBL-FLIGHT-LAB-Complete-lab-submission/dashboard.php
- **REST API:** http://localhost/IBL-FLIGHT-LAB-Complete-lab-submission/api/airlines

---

## Project Structure

```
IBL-FLIGHT-LAB-Complete-lab-submission/
├── database/db.php          # Database connection
├── models/                  # Data models (Users, Cities, Countries, Airlines)
├── controllers/             # Business logic & CRUD operations
├── css/                     # Bootstrap, Font Awesome, custom styles
├── js/                      # jQuery, Bootstrap, app logic
├── webfonts/                # Font files
├── index.php                # Login page
├── dashboard.php            # Main dashboard
├── settings.php             # Settings page
├── city.html                # City management
├── country.html             # Country management
└── usersmanager.html        # User management
```

---

## Troubleshooting

### Apache Won't Start
```bash
# Check port 80
sudo lsof -i :80
# Kill process or change Apache port to 8080
```

### MySQL Won't Start
```bash
# Check port 3306
sudo lsof -i :3306
# Or restart XAMPP completely
```

### Database Connection Failed
- Ensure MySQL is running (green in XAMPP)
- Verify database name: `expediaflightbooking`
- Check credentials in `database/db.php`

### 404 Errors
- Verify project in htdocs folder
- Use correct URL: `http://localhost/IBL-FLIGHT-LAB-4-AND-5/`

### Blank Page
```php
// Add to top of index.php to see errors
ini_set('display_errors', 1);
error_reporting(E_ALL);
```

### Missing Stored Procedures
```sql
-- Check if procedures exist
SHOW PROCEDURE STATUS WHERE Db = 'expediaflightbooking';
-- Import complete SQL file with stored procedures
```

---

## API Usage

**Get all airlines:**
```bash
GET http://localhost/IBL-FLIGHT-LAB-4-AND-5/api/airlines
```

**Create airline:**
```bash
POST http://localhost/IBL-FLIGHT-LAB-4-AND-5/api/airlines
Content-Type: application/json
{"airline_name": "Emirates", "logo": "logo.png"}
```

---

## XAMPP Commands

**macOS:**
```bash
sudo /Applications/XAMPP/xamppfiles/xampp start|stop|restart
```

**Windows:** Use XAMPP Control Panel GUI

---

**Version:** 1.0.0
**Status:** Complete & Functional
**Last Updated:** December 2025
