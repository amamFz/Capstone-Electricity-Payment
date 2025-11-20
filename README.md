# Capstone Electricity Payment System

A comprehensive electricity billing and payment management system built with Laravel. This application allows administrators to manage customers, track electricity usage, process payments, and generate receipts.

## Features

- **Customer Management (Pelanggan)**
  - Register and manage electricity customers
  - Customer categorization by type (Jenis Pelanggan)
  - Customer profile management

- **Tariff Management (Tarif)**
  - Configure electricity rates
  - Dynamic pricing based on customer type
  - Tariff history tracking

- **Usage Tracking (Pemakaian)**
  - Record monthly electricity consumption
  - Calculate charges based on usage and tariff
  - Usage history and analytics

- **Payment Processing (Pembayaran)**
  - Public payment search functionality
  - Payment entry and verification
  - Payment history tracking
  - PDF receipt generation

- **User Management**
  - Role-based access control
  - User authentication and authorization
  - Profile management

- **Dashboard & Analytics**
  - Overview of total users, customers, and consumption
  - Recent activity tracking
  - Statistical insights

## Technologies Used

- **Backend**: Laravel 11.x (PHP 8.2+)
- **Frontend**: 
  - Tailwind CSS
  - Alpine.js
  - Blade Templates
- **Database**: SQLite (default) / MySQL / PostgreSQL
- **PDF Generation**: DomPDF
- **Build Tools**: Vite
- **Authentication**: Laravel Breeze

## Requirements

- PHP 8.2 or higher
- Composer
- Node.js & NPM
- SQLite (or MySQL/PostgreSQL)

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/amamFz/Capstone-Electricity-Payment.git
   cd Capstone-Electricity-Payment
   ```

2. **Install PHP dependencies**
   ```bash
   composer install
   ```

3. **Install Node dependencies**
   ```bash
   npm install
   ```

4. **Environment setup**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. **Configure database**
   - Edit `.env` file with your database credentials
   - For SQLite (default), ensure the database file exists:
     ```bash
     touch database/database.sqlite
     ```

6. **Run migrations**
   ```bash
   php artisan migrate
   ```

7. **Seed database (optional)**
   ```bash
   php artisan db:seed
   ```

8. **Build frontend assets**
   ```bash
   npm run build
   ```

9. **Start the development server**
   ```bash
   php artisan serve
   ```

   Visit `http://localhost:8000` in your browser.

## Development

To run the development server with hot module replacement:

```bash
npm run dev
```

In a separate terminal:
```bash
php artisan serve
```

## Database Structure

The application uses the following main tables:

- **users**: System users and administrators
- **jenis_pelanggans**: Customer types/categories
- **tarifs**: Electricity tariff rates
- **pelanggans**: Customer information
- **pemakaians**: Monthly electricity usage records

## Usage

### Public Access
- View payment history at the home page
- Search for payments by customer ID or meter number

### Admin Access
1. Login to the dashboard
2. Manage customers, tariffs, and customer types
3. Record electricity usage
4. Process payments
5. Generate receipts

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
