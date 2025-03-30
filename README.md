# Symfony Framework Project

## 📌 Introduction
This project is built using the Symfony framework, a powerful and flexible PHP framework for web development. It follows the MVC (Model-View-Controller) architecture and provides robust features for rapid application development.

## 🚀 Getting Started

### 1️⃣ Prerequisites
Before setting up this project, ensure you have the following installed:
- PHP (>= 8.1)
- Composer
- Symfony CLI
- MariaDB (for database management)
- Node.js & npm (if using Webpack Encore)

### 2️⃣ Installation
Clone the repository and install dependencies:
```bash
# Clone the repository
git clone https://github.com/your-username/your-repo.git
cd your-repo

# Install PHP dependencies
composer install

# Create environment file
cp .env.example .env
```

### 3️⃣ Configuration
Update your `.env` file with database credentials:
```
DATABASE_URL="mysql://db_user:db_password@127.0.0.1:3306/db_name"
```
Since MariaDB is compatible with MySQL, the same connection string can be used.

Then, set up the database:
```bash
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
```

### 4️⃣ Running the Application
Start the Symfony local server:
```bash
symfony server:start
```
Access the application in your browser:
```
http://127.0.0.1:8000
```

## 🛠 Features
- ✅ MVC architecture
- ✅ Doctrine ORM for database interactions
- ✅ Twig templating engine
- ✅ Routing and controllers for handling requests
- ✅ Form handling & validation

## 📂 Project Structure
```
my_project/
├── src/               # Application source code
│   ├── Controller/    # Controllers
│   ├── Entity/        # Doctrine entities
│   ├── Form/          # Form classes
│   ├── Repository/    # Database repositories
├── templates/         # Twig templates
├── public/            # Web root directory
├── config/            # Configuration files
└── migrations/        # Database migrations
```

## 🔄 Running Migrations
To generate and apply database migrations:
```bash
php bin/console make:migration
php bin/console doctrine:migrations:migrate
```

## 📝 Testing
Run unit tests with PHPUnit:
```bash
php bin/phpunit
```

## 📜 License
This project is licensed under the MIT License - see the `LICENSE` file for details.

---
Feel free to contribute by submitting issues and pull requests! 🚀
