# Edoc--Hospital-appointment-system
## 🚀 Step-by-Step Installation & Setup Guide

This guide explains how to set up and run the **Open Source Doctor Appointment Booking System (eDoc)** on your local machine.

---

### 1️⃣ Prerequisites

Ensure the following are installed on your system:

* **XAMPP / WAMP / MAMP** (Apache + PHP + MySQL)
* **PHP 7.4 or above**
* **MySQL 5.7+**
* **Web Browser** (Chrome / Edge / Firefox)
* **Git** (optional, for cloning the repository)

---

### 2️⃣ Download the Project

**Option A: Clone from GitHub**

```bash
git clone https://github.com/your-username/edoc.git
```

**Option B: Download ZIP**

* Download the ZIP file from GitHub
* Extract it into your server root directory:

  * XAMPP → `htdocs/`
  * WAMP → `www/`

Final path example:

```
htdocs/edoc/
```

---

### 3️⃣ Start the Server

* Open **XAMPP Control Panel**
* Start **Apache** and **MySQL** services

---

### 4️⃣ Create the Database

1. Open browser and go to:

   ```
   http://localhost/phpmyadmin
   ```
2. Click **New** → Create a database
3. Database name (recommended):

   ```
   edoc
   ```
4. Click **Create**

---

### 5️⃣ Import Database Tables

1. Select the `edoc` database
2. Go to **Import** tab
3. Upload the provided SQL file (if included)
4. Click **Go**

> ⚠️ If no SQL file is provided, ensure required tables are created manually as per the project schema.

---

### 6️⃣ Configure Database Connection

1. Open the file:

   ```
   edoc/connection.php
   ```
2. Update database credentials:

```php
$database = "edoc";
$username = "root";
$password = "";
$host = "localhost";
```

Save the file.

---

### 7️⃣ Configure Payment Gateway (Razorpay)

1. Navigate to:

   ```
   edoc/razorpay/
   ```
2. Open configuration files and add:

   * Razorpay **Key ID**
   * Razorpay **Secret Key**
3. Ensure `verify.php` and `success.php` are properly configured

> 🔐 Use Razorpay **Test Mode** for development.

---

### 8️⃣ Run the Application

Open your browser and visit:

```
http://localhost/edoc/
```

---

### 9️⃣ Default User Roles & Access

#### 👨‍⚕️ Admin Panel

```
http://localhost/edoc/admin/
```

Admin can:

* Manage doctors
* Manage schedules
* View patients
* Handle appointments
* View payments

#### 👤 Patient Panel

```
http://localhost/edoc/login.php
```

Patients can:

* Register & login
* Book appointments
* View schedules
* Make payments

---

### 🔟 Screenshots

Screenshots of the application UI are available in:

```
edoc/Screenshots/
```

---

### 🔒 Security Notes

* Update default credentials before deployment
* Never expose database credentials publicly
* Use HTTPS for production

---

### 🛠️ Troubleshooting

* **Blank page** → Check PHP version
* **Database error** → Verify credentials in `connection.php`
* **Payment issues** → Verify Razorpay keys

---

### 📌 Future Enhancements

* Email notifications
* Role-based authentication
* Doctor availability calendar
* Admin analytics dashboard

---

### 📄 License

This project is open-source and free to use for educational purposes.

---

✅ Your Doctor Appointment Booking System is now ready to use!
