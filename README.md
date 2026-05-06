# Laravel Filament Boilerplate

Pre-configured Laravel 12 starter kit with Filament v5 admin panel, role-based access control, and modern developer tooling.

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0-blue" />
  <img src="https://img.shields.io/badge/PHP-8.2-777BB4" />
  <img src="https://img.shields.io/badge/Laravel-12-red" />
  <a href="LICENSE">
    <img alt="License" src="https://img.shields.io/badge/license-MIT-yellow" target="_blank" />
  </a>
</p>

## Compatibility
- PHP >= 8.2
- Laravel 12.x
- Node.js >= 18
- npm >= 9

## Description
Eliminates repetitive initial configuration for Laravel-based projects by providing a pre-integrated stack with enterprise-grade admin panel, access control, testing framework, and frontend tooling. Targeted at Laravel developers who need to skip boilerplate setup and start building business logic immediately.

## Features
- Laravel 12 framework with PHP 8.2+ support
- Filament v5 admin panel with pre-configured base resources
- Spatie Laravel Permission for granular role-based access control (RBAC)
- Filament Shield for automatic synchronization of admin panel permissions
- Pest PHP testing framework with pre-configured test suite and examples
- Tailwind CSS v4 for utility-first, responsive styling
- Vite for fast frontend asset compilation and hot module replacement (HMR)
- Pre-built User, Role, and Permission models with factories and seeders
- Streamlined Laravel 12 directory structure (deprecated Kernel.php removed)
- Artisan command auto-discovery for custom console commands

## Tech Stack
### Backend
- PHP 8.2
- Laravel 12
- Filament v5
- Livewire v4
- Spatie Laravel Permission
- Filament Shield

### Testing
- Pest v4
- PHPUnit v12

### Frontend
- Tailwind CSS v4
- Vite
- Alpine.js

### Tooling
- Composer
- Node.js
- npm

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Akselerasi-Prima-Digital/Laravel-Filament-Boilerplate.git
   cd Laravel-Filament-Boilerplate
   ```

2. Install PHP dependencies:
   ```bash
   composer install
   ```

3. Install Node.js dependencies:
   ```bash
   npm install
   ```

4. Copy environment configuration:
   ```bash
   cp .env.example .env
   ```

5. Generate application encryption key:
   ```bash
   php artisan key:generate
   ```

6. Configure database connection in `.env`:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=laravel_filament_boilerplate
   DB_USERNAME=root
   DB_PASSWORD=
   ```

7. Run database migrations and seeders:
   ```bash
   php artisan migrate --seed
   ```

8. Compile frontend assets for production:
   ```bash
   npm run build
   ```
   For development with HMR:
   ```bash
   npm run dev
   ```

9. Start the development server:
   ```bash
   php artisan serve
   ```

## Configuration
### Environment Variables
Key variables to configure in `.env`:
- `APP_NAME`: Application display name (default: `Laravel`)
- `APP_URL`: Base application URL (default: `http://localhost`)

### Package Configuration
- Spatie Permission: permission.php
- Filament Shield: filament-shield.php
- Filament Panel: filament.php

## Usage
### Admin Panel Access
After completing installation and seeding, access the Filament admin panel at:
```
http://localhost:8000/admin
```
Default admin credentials are defined in UserSeeder.php.

### Permission Management
Sync Filament admin permissions with Spatie Permission using Filament Shield:
```bash
php artisan shield:generate
```
Manage roles and permissions via the Filament admin panel at `/admin/shield/roles`.

### Running Tests
Execute the full test suite:
```bash
php artisan test
```

## Project Structure
```
app/
  Filament/       # Filament admin panel resources, pages, and widgets
  Http/           # Controllers and middleware
  Models/         # Eloquent models (User, Role, Permission)
  Policies/       # Model policies (RolePolicy)
  Providers/      # Service providers
bootstrap/        # Laravel 12 bootstrap files (app.php, providers.php)
config/           # All package and application configuration
database/         # Migrations, factories, seeders
public/           # Public assets and entry points
resources/        # Frontend assets (CSS, JS) and Blade views
routes/           # Web and console routes
tests/            # Pest PHP test suite (Feature, Unit)
```

## Scripts
### Node.js Scripts (package.json)
- `npm run dev`: Start Vite development server with HMR
- `npm run build`: Compile and minify frontend assets for production

### Artisan Commands
- `php artisan serve`: Start Laravel development server
- `php artisan migrate`: Run pending database migrations
- `php artisan shield:generate`: Sync Filament permissions
- `php artisan test`: Run Pest PHP test suite
- `php artisan make:filament-resource`: Generate new Filament resource

## Contributing
Contributions are welcome. Follow these steps:
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit changes: `git commit -m "Add: your feature description"`
4. Push to branch: `git push origin feature/your-feature`
5. Open a pull request

Ensure all tests pass before submitting:
```bash
php artisan test
```

## License
Distributed under the MIT License. See LICENSE for full text.

## Author
Akselerasi Prima Digital
