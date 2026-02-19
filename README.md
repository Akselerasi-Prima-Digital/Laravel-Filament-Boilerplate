<p align="center">
  <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
</p>

<p align="center">
  <a href="https://github.com/laravel/framework/actions"><img src="https://img.shields.io/badge/Laravel-12.x-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel Version"></a>
  <a href="https://filamentphp.com/"><img src="https://img.shields.io/badge/Filament-5.x-FFAA00?style=for-the-badge&logo=laravel&logoColor=white" alt="Filament Version"></a>
  <a href="https://php.net"><img src="https://img.shields.io/badge/PHP-8.2+-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP Version"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License"></a>
</p>

# Laravel Filament Boilerplate

A modern boilerplate for building web applications with **Laravel** and **Filament Admin Panel**. Comes with authentication system, user management, and role-based access control (RBAC) out of the box.

## ✨ Key Features

### 🔐 Authentication & Security

- Email & password login
- Forgot password with email reset link
- Email verification for new users
- Session management

### 👥 User Management

- Intuitive CRUD interface for users
- Assign roles to users
- Direct permissions for users without roles
- Profile management

### 🛡️ Role & Permission (RBAC)

- Granular role management with permissions
- Role-based access control using [Filament Shield](https://github.com/bezhanSalleh/filament-shield)
- Guard support for multi-auth
- Super admin bypass for full access

### 🎨 Admin Panel

- Modern dashboard with [Filament 5.x](https://filamentphp.com/)
- Dark/Light mode
- Responsive design for mobile & desktop
- Ready-to-use widgets & charts

## 🛠️ Tech Stack

| Technology      | Version |
| --------------- | ------- |
| PHP             | ^8.2    |
| Laravel         | ^12.0   |
| Filament        | 5.0     |
| Filament Shield | ^4.1    |
| TailwindCSS     | 4.x     |

## 📦 Packages

### Production Dependencies

| Package                                                                         | Version | Description                               |
| ------------------------------------------------------------------------------- | ------- | ----------------------------------------- |
| [laravel/framework](https://laravel.com/)                                       | ^12.0   | The PHP Framework for Web Artisans        |
| [filament/filament](https://filamentphp.com/)                                   | 5.0     | Elegant TALL stack admin panel            |
| [bezhansalleh/filament-shield](https://github.com/bezhanSalleh/filament-shield) | ^4.1    | Role & Permission management for Filament |
| [laravel/tinker](https://github.com/laravel/tinker)                             | ^2.10.1 | REPL for Laravel                          |

### Development Dependencies

| Package                                         | Version | Description                    |
| ----------------------------------------------- | ------- | ------------------------------ |
| [pestphp/pest](https://pestphp.com/)            | ^4.3    | Testing framework              |
| [laravel/pint](https://laravel.com/docs/pint)   | ^1.24   | Code style fixer               |
| [laravel/sail](https://laravel.com/docs/sail)   | ^1.41   | Docker development environment |
| [laravel/pail](https://github.com/laravel/pail) | ^1.2.2  | Real-time log viewer           |

## 📋 Requirements

- PHP >= 8.2
- Composer
- Node.js & NPM
- MySQL / PostgreSQL / SQLite

## 🚀 Installation

### 1. Clone Repository

```bash
git clone https://github.com/Akselerasi-Prima-Digital/Laravel-Filament-Boilerplate.git
cd Laravel-Filament-Boilerplate
```

### 2. Install Dependencies

```bash
composer install
npm install
```

### 3. Environment Setup

```bash
cp .env.example .env
php artisan key:generate
```

### 4. Database Configuration

Edit the `.env` file and configure your database settings:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

### 5. Migration & Seeder

```bash
php artisan migrate --seed
```

### 6. Build Assets

```bash
npm run build
```

### 7. Run Server

```bash
php artisan serve
```

Or use the provided composer script:

```bash
composer dev
```

Access the application at: `http://localhost:8000/admin`

## 🔑 Default Credentials

| Email                | Password  | Role        |
| -------------------- | --------- | ----------- |
| superadmin@gmail.com | admin1234 | Super Admin |

> ⚠️ **Important:** Change the default password immediately after your first login!

## 📁 Folder Structure

```
├── app/
│   ├── Filament/           # Filament resources & pages
│   ├── Models/             # Eloquent models
│   ├── Policies/           # Authorization policies
│   └── Providers/          # Service providers
├── database/
│   ├── migrations/         # Database migrations
│   └── seeders/            # Database seeders
├── resources/
│   └── views/              # Blade views
└── routes/
    └── web.php             # Web routes
```

## 🧪 Testing

Run tests with Pest:

```bash
composer test
```

## 🤝 Contributing

Contributions are welcome! Please fork this repository and create a pull request for any improvements or bug fixes.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the [MIT License](LICENSE).

## 🙏 Credits

- [Laravel](https://laravel.com/) - The PHP Framework for Web Artisans
- [Filament](https://filamentphp.com/) - The elegant TALL stack admin panel
- [Filament Shield](https://github.com/bezhanSalleh/filament-shield) - Role & Permission management

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/Akselerasi-Prima-Digital">Akselerasi Prima Digital</a>
</p>
