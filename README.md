# Library Management System

> A comprehensive automated system for efficiently managing a public library. Empowering librarians with an interactive admin panel for seamless control and administration.

## Table of Contents
- [Development](#development)
- [Contribute](#contribute)
- [Setup](#setup)
- [Features](#features)
- [Screenshots](meta/README.md)

## Development
The backend of this system is developed using the robust **[Laravel 4.2 PHP MVC Framework](http://laravel.com/)**, which requires PHP 5.6 along with the essential MCrypt extension. The frontend is crafted using the **[Edmin Responsive Bootstrap Admin Template](http://egrappler.com/responsive-bootstrap-admin-template-edmin/)**, built upon [Bootstrap v2.2.2](http://bootstrapdocs.com/v2.2.2/docs/) and enriched with [jQuery](https://blog.jquery.com/2013/02/04/jquery-1-9-1-released/) and [Underscore-Dot-JS](http://underscorejs.org/).

## Contribute
- To report bugs related to incorrect file processing, please open a new issue.
- We warmly welcome Pull Requests (PRs) to enhance the existing system.

## Setup

### Prerequisite: MySQL Installation (for Linux)

If you don't have the MySQL Database Server installed, follow these steps:

1. Refer to Oracle's comprehensive guide on ["Installing MySQL on Linux"](https://dev.mysql.com/doc/refman/8.0/en/linux-installation.html) for detailed instructions.
2. Alternatively, you can install a compatible MySQL server for this project by running:

```bash
apt-get update && apt-get install mysql-server
```

3. During the installation, you may be prompted to set a root password for MySQL.

4. Create a MySQL user and database for this project and grant the necessary permissions. Configuration instructions are provided below.

### Unix / Linux / Mac Setup

Please ensure that PHP 5.6, the PHP mcrypt extension, and MySQL are installed for this project:

```bash
apt-get update
apt-get install php5.6 php5.6-mcrypt
git clone https://github.com/prabhakar267/library-management-system
cd library-management-system
[sudo] chmod -R 755 app/storage
composer install
```

Edit the [mysql.config.php.sample](app/config/mysql.config.php.sample) file to match your MySQL configurations and save it as `mysql.config.php` in the same directory.

```bash
php artisan migrate
php artisan serve
```

### Windows Setup

**MySQL Setup:**

- Download [MySQL Workbench](https://dev.mysql.com/downloads/workbench/).

- Choose the appropriate Windows version from the download page.

- Follow the installation instructions.

**PHP Setup:**

- For PHP 7+, obtaining the `mcrypt` extension is non-trivial, so consider using PHP 5.6 with XAMPP for this project. Download a compatible version of [XAMPP](https://www.apachefriends.org/xampp-files/5.6.33/xampp-win32-5.6.33-0-VC11-installer.exe) and use it to run the application.

For Windows setup, follow these steps:

```bash
cd C:/path/to/xampp/htdocs
git clone https://github.com/prabhakar267/library-management-system
cd library-management-system
composer update

# If your PHP version is not compatible with mcrypt:
C:/path/to/xampp5.6.33/php/php.exe artisan clear-compiled
C:/path/to/xampp5.6.33/php/php.exe artisan cache:clear

# Create a table for the app via phpMyAdmin or your preferred method.
# Edit app/config/mysql.config.php.sample to match your MySQL configurations and save it as mysql.config.php in the same directory.
php artisan migrate

# If your PHP version is not compatible with mcrypt:
C:/path/to/xampp5.6.33/php/php.exe artisan serve
```

## Features
- Empowers librarians with authorized login IDs and passwords for secure system access.
- Students have access to limited features, such as book searching and student registration.
- Librarians can efficiently search for specific books, book issues, and students from the home panel.
- The system automates book entry by generating Issue IDs based on the number of issues entered by librarians.
- Librarians can approve students, keeping a record of their actions.
- The system facilitates book issuance and return, providing an overview of outstanding logs.

![screencapture-library-local-1450375427449](https://github.com/RedisMadani/library-management-system/assets/136177376/85cb86df-cc7b-4023-9d2b-28f705d20a1c)
