# Car Rental Portal

A PHP/MySQL car rental web application with a public-facing site for browsing and booking vehicles, and an admin panel for managing vehicles, bookings, brands, pages, and users.

## Features

- Browse and search available cars, view vehicle details, and check availability
- User registration, login, and profile management
- Car booking with booking history (My Bookings)
- Testimonials (submit and view)
- Contact us form and newsletter subscription
- Admin panel: manage vehicles, brands, bookings (new/confirmed/canceled), contact queries, subscribers, pages, and testimonials

## Requirements

- PHP 5.6+ / 7.x with PDO MySQL extension
- MySQL/MariaDB
- Apache (e.g. via [XAMPP](https://www.apachefriends.org/))

## Setup

1. Clone the repo into your web root, e.g. `c:\xampp\htdocs\carrental`.
2. Create a MySQL database named `carrental` and import your schema/data (no schema dump is included in this repo — you'll need an existing `.sql` export or to recreate the tables used by the app, e.g. `tblusers`, `tblvehicles`, `tblbooking`, `tbltestimonial`, `tblcontactusinfo`, `tblcontactusquery`, `tblpages`, `tblsubscribers`).
3. Copy the sample config files and adjust credentials if needed:
   ```
   copy includes\config.sample.php includes\config.php
   copy admin\includes\config.sample.php admin\includes\config.php
   ```
   Default values match a fresh XAMPP install (`root` user, no password, host `localhost`).
4. Start Apache and MySQL (via XAMPP Control Panel).
5. Visit `http://localhost/carrental/` for the public site and `http://localhost/carrental/admin/` for the admin panel.

## Project Structure

- `/` — public site pages (home, car listing, search, booking, profile, testimonials, contact)
- `admin/` — admin dashboard and management pages
- `includes/` — shared PHP includes (header, footer, login, registration, DB config)
- `assets/` — public site CSS/JS/images
- `admin/css`, `admin/js`, `admin/img` — admin panel assets

## Notes

- `includes/config.php` and `admin/includes/config.php` hold DB credentials and are git-ignored; use the `.sample.php` versions as templates.
