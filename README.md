# ✈️ Online Flight Booking Management System

A web-based flight booking platform built with **PHP** and **MySQL**, allowing users to search, browse, and book flights online, with a full-featured **admin panel** to manage flights, airlines, airports, users, and bookings.

---

## 📌 Overview

The Online Flight Booking Management System simulates a real-world airline booking portal. Visitors can register, log in, search for flights between airports, and book seats. Administrators get a separate dashboard to add and manage flight schedules, airline and airport records, monitor bookings, and configure site-wide settings.

---

## 🚀 Features

### User Side
- User registration and login (session-based authentication)
- Search flights by departure and arrival airport
- View flight listings with airline, schedule, and seat availability
- Book flights for one or more passengers with real-time seat validation
- Dynamic "About Us" and home page content pulled from site settings

### Admin Panel
- Secure admin login
- **Flights** — add, edit, delete flight schedules
- **Airlines** — manage airline records
- **Airports** — manage airport/location records
- **Bookings** — view and manage all customer bookings
- **Users** — manage registered user accounts
- **Site Settings** — update site name, cover image, and about content
- DataTables-powered listing pages (search, sort, pagination)

---

## 🛠️ Tech Stack

| Layer          | Technology                                   |
|----------------|-----------------------------------------------|
| Backend        | PHP (procedural, mysqli)                      |
| Database       | MySQL                                         |
| Frontend       | HTML5, CSS3, Bootstrap, jQuery                |
| Tables/UI      | DataTables, Font Awesome                      |
| Architecture   | Multi-page PHP app with a dedicated `/admin` panel |

---

## 📂 Project Structure

```
Online_Flight_Booking_Management_System/
├── admin/                  # Admin panel
│   ├── db_connect.php      # Database connection
│   ├── flights.php         # Flight management
│   ├── airlines.php        # Airline management
│   ├── airport.php         # Airport management
│   ├── booked.php          # Booking records
│   ├── users.php           # User management
│   ├── site_settings.php   # Site configuration
│   ├── ajax.php            # AJAX request handler
│   └── assets/             # Admin static assets (DataTables, icons, uploads)
├── assets/                 # Public static assets (images)
├── css/                    # Stylesheets
├── js/                     # Client-side scripts
├── database/
│   └── flight_booking_db.sql   # Database schema & seed data
├── index.php                # Main entry point / router
├── home.php                  # Landing page + flight search
├── flights.php                # Flight listing page
├── book_flight.php            # Booking form
├── get_fields.php             # AJAX passenger fields
├── login.php / signup.php     # User authentication
├── about.php                  # About page
├── header.php / footer.php    # Shared layout
└── readme.txt                 # Original setup notes
```

---

## 🗄️ Database Schema

The system uses the `flight_booking_db` database with the following tables:

- **`users`** — registered user accounts
- **`airlines_list`** — airline records
- **`airport_list`** — airport/location records
- **`flight_list`** — flight schedules (airline, route, timing, seats)
- **`booked_flight`** — passenger bookings linked to flights and users
- **`system_settings`** — site-wide configuration (name, about content, cover image)

---

## ⚙️ Installation & Setup

1. **Install prerequisites**
   - [XAMPP](https://www.apachefriends.org/) (or any Apache + PHP + MySQL stack)
   - A code editor (VS Code / Sublime Text / Notepad++)

2. **Clone or download this repository**
   ```bash
   git clone https://github.com/<your-username>/online-flight-booking-management-system.git
   ```

3. **Deploy the project**
   - Copy the project folder into your server's document root, e.g. `C:/xampp/htdocs/`

4. **Create the database**
   - Start Apache and MySQL from the XAMPP control panel
   - Open [phpMyAdmin](http://localhost/phpmyadmin)
   - Create a new database named `flight_booking_db`
   - Import the schema from `database/flight_booking_db.sql`

5. **Configure the database connection**
   - Check `admin/db_connect.php` and update credentials if needed (default: host `localhost`, user `root`, no password)

6. **Run the application**
   - Visit `http://localhost/Online_Flight_Booking_Management_System`

---

## 🔑 Default Admin Login

| Field    | Value      |
|----------|------------|
| Username | `admin`    |
| Password | `admin123` |

> ⚠️ Change the default admin credentials before deploying this project anywhere public.

---

## 📸 Screenshots

*(Add screenshots of the home page, flight search results, booking form, and admin dashboard here.)*

---

## 📄 License

This project is intended for educational and academic purposes (e.g. mini/major project submissions). Feel free to fork and customize it for learning.

---

## 🙋 Author

Maintained by **Thejomurthi** — B.E. Electronics and Communication Engineering graduate, currently training in Java Full Stack Development.
