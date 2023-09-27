## About

**ByteCodeLearners** is a group of students working together with patience and enthusiasm to create something <kbd>ctrl</kbd> + <kbd>N</kbd>.

> **Note**
> Welcome to the backend repository for our server! This repository serves as the backbone of our application, supporting the existing backend infrastructure.

## Table of Contents

- [Requirements](#requirements)
- [Installation](#installation)

<a name="requirements"></a>

## Requirements

| Package                              | Version   |
| ------------------------------------ | --------- |
| [Node.js](https://nodejs.org/en/)    | V14.19.1+ |
| [npm](https://nodejs.org/en/)        | V6.14.16+ |
| [Composer](https://getcomposer.org/) | V2.2.6+   |
| [PHP](https://www.php.net/)          | V8.0.17+  |
| [MySQL](https://www.mysql.com/)      | V8.0.27+  |

<a name="installation"></a>

## Installation

> **Warning**
> Make sure to follow the requirements first.

Here is how you can run the project locally:

1. Clone this repo

   ```sh
   git clone https://github.com/ByteCodeLearners/BytecodeLearners_Backend.git
   ```

2. Go into the project root directory

   ```sh
   cd BytecodeLearners_Backend
   ```

3. Copy .env.example file to .env file
   ```sh
   cp .env.example .env
   ```
4. Create database `bytecodebackend` (you can change database name)

5. Go to `.env` file

   - set database credentials (`DB_DATABASE=bytecodebackend`, `DB_USERNAME=root`, `DB_PASSWORD=`)

6. Install PHP dependencies

   ```sh
   composer install
   ```

7. Generate key

   ```sh
   php artisan key:generate
   ```

8. Run migration

   ```
   php artisan migrate
   ```

9. Run server

   ```sh
   php artisan serve
   ```

10. Visit `localhost:8000` in your favorite browser.

    > Make sure to follow your Laravel local Development Environment.
