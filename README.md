# EcoTrack — PHP + MongoDB Starter

A beginner-friendly waste reporting and recycling tracker built with:
- PHP 8.1+
- MongoDB Community Server
- MongoDB PHP Library
- HTML, CSS and vanilla JavaScript

## Features
- Submit a waste issue report
- View recent reports
- Show total, submitted and resolved counts
- Update a report status (demo admin action)
- Input validation and basic error handling

## Requirements
1. PHP 8.1 or newer
2. MongoDB Community Server running locally, or a MongoDB Atlas connection string
3. Composer
4. PHP MongoDB extension (`mongodb`)

## Setup

### 1. Install the PHP MongoDB extension
Install/enable the `mongodb` PHP extension for your PHP version. Check:
```bash
php -m
```
You should see `mongodb` in the list.

### 2. Install dependencies
From the project root:
```bash
composer install
```

### 3. Configure MongoDB
Copy `.env.example` to `.env`, then edit `MONGODB_URI` if needed.
For local MongoDB, the default URI is:
`mongodb://127.0.0.1:27017`

### 4. Start the application
From the project root:
```bash
php -S 127.0.0.1:8000 -t public
```
Open `http://127.0.0.1:8000`.

## Notes
- MongoDB database: `ecotrack`
- Collection: `reports`
- This is a student prototype. It intentionally has no login system. Do not expose the status-update endpoint publicly without adding authentication and authorization.
- The app reads `.env` with a small custom loader; Composer installs the official MongoDB PHP library.

## Suggested next steps
1. Add login and role-based access for administrators.
2. Add report image uploads with file type and size validation.
3. Add a recycling-centre directory.
4. Add Chart.js charts for report categories and monthly trends.
5. Add map pins for reported locations.
6. Add tests and deployment documentation.
