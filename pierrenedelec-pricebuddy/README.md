# PriceBuddy for Umbrel

Price tracking and monitoring solution for Umbrel.

## Features

- Track products from multiple online stores
- Price history and charts
- Price drop alerts
- Web scraping with SeleniumBase
- User-friendly dashboard

## Configuration

### Required Environment Variables

When installing this app on Umbrel, you'll need to configure the following environment variables:

- `DB_PASSWORD`: Database password for the MySQL user (required)
- `DB_ROOT_PASSWORD`: Root password for MySQL (required)
- `APP_USER_EMAIL`: Initial admin email (default: admin@example.com)
- `APP_USER_PASSWORD`: Initial admin password (default: admin)

**Security Note**: Make sure to change the default admin credentials after first login!

## Architecture

This app consists of 3 services:

1. **app**: PHP application (Laravel) serving on port 80
2. **database**: MySQL 8.2 database
3. **scraper**: SeleniumBase scraper for web scraping

## Data Persistence

The following directories are persisted:

- `${APP_DATA_DIR}/data/storage`: Application storage
- `${APP_DATA_DIR}/data/mysql`: MySQL database

## Original Project

Based on [PriceBuddy](https://github.com/jez500/pricebuddy) by Jez500.

For more information, visit: https://pricebuddy.jez.me/

