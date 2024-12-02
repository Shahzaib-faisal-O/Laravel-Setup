# Laravel Project Setup Guide

Follow these steps to create a new Laravel project:

## Prerequisites

- Ensure you have [Composer](https://getcomposer.org/) installed on your system.
- PHP 8.0 or later is required.
- Installing XAMPP will automatically install php as well mysql.

<!-- <hr> -->

## For Szabist university

- PHP and Composer is already installed.

## Steps to Create and Run Your Laravel Project

1. **Install Laravel Installer**

   ```bash
   composer global require laravel/installer
   ```

2. **Create a New Project**

   ```bash
   laravel new First-project
   ```

3. **Navigate to Your Project Directory**

   ```bash
   cd First-project
   ```

4. **Set Up the Database**

   - Laravel uses MySQL as the default database. Ensure you have MySQL installed and running.
   - If you encounter any errors, locate the `.env` file in your project directory and update the database settings:
     ```dotenv
     DB_CONNECTION=mysql
     DB_HOST=127.0.0.1
     DB_PORT=3306
     DB_DATABASE=laravel
     DB_USERNAME=root
     DB_PASSWORD=
     ```

5. **Run Database Migrations**

   - To create the required tables for your project, run:

     ```bash
     php artisan migrate
     ```

   - If you encounter any session-related issues, ensure the database is correctly configured in the `.env` file.

6. **Serve Your Project**

   - Start the Laravel development server:

     ```bash
     php artisan serve
     ```

   - Open your browser and visit `http://127.0.0.1:8000` to see your project in action.

## Troubleshooting

- If any issues arise, double-check your `.env` file for correct database configuration.
- Ensure Composer dependencies are up to date by running:
  ```bash
  composer install
  ```
- for session Problem
  `run:php artisan session:table`

- for cache clear
  `run:php artisan cache:clear`

Congratulations! Your Laravel project is now up and running.
