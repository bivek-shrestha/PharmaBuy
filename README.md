# Laravel eCommerce Website Setup Guide : PharmaBuy

## Prerequisites

Ensure your system meets the following requirements:

-   **Operating System**: Ubuntu 16.04 LTS or higher / Windows 7 or higher (WAMP / XAMPP)
-   **Server**: Apache 2 or NGINX
-   **RAM**: 4 GB or higher
-   **PHP**: 7.4 or higher
-   **Database**:
    -   For MariaDB users: 10.2.7 or higher
    -   For MySQL users: 5.7.23 or higher
-   **Node.js**: 8.11.3 LTS or higher
-   **Composer**: 1.6.5 or higher

## Installation Steps

### 1. Install Composer

Download and install Composer from the [official website](https://getcomposer.org/).

### 2. Create a New Laravel Project

Open your terminal and run:

```bash
composer create-project --prefer-dist laravel/laravel PharmaBuy
```

This command will create a new Laravel project named `PharmaBuy`.

### 3. Set Up the Database

-   Create a new database for your application.
-   Configure the `.env` file in the root directory of your Laravel project with your database credentials:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_username
DB_PASSWORD=your_password
```


After installation, publish the assets and configurations:

```bash
php artisan vendor:publish --all
```

Run the migrations and seed the database:

```bash
php artisan migrate
php artisan db:seed
```

### 5. Configure Environment Settings

Update the following settings in your `.env` file:

```env
APP_URL=http://your-domain.com
ADMIN_EMAIL=admin@example.com
ADMIN_NAME=Admin
```

### 6. Set Up Storage Link

Create a symbolic link from `public/storage` to `storage/app/public`:

```bash
php artisan storage:link
```

### 7. Run the Application

Start the development server:

```bash
php artisan serve
```

Access your application at `http://localhost:8000`.

## Additional Features

-   **Multi-Vendor Marketplace**: Allow multiple sellers to register and sell their products on your platform.
-   **Point of Sale (POS)**: Manage both online and physical stores seamlessly.
-   **SaaS-Based eCommerce Solution**: Enable users to start and grow their online businesses with a scalable solution.
-   **Mobile App Integration**: Improve accessibility with a Flutter-based mobile app.

## Peak to the Project
