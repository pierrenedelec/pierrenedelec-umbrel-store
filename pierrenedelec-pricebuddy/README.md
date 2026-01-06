# PriceBuddy for Umbrel

Price tracking and monitoring solution for Umbrel.

## Features

- Track products from multiple online stores
- Price history and charts
- Price drop alerts
- Web scraping with SeleniumBase
- User-friendly dashboard

## Configuration

### Environment Variables

This app comes with sensible defaults but should be configured for production use:

| Variable | Default | Description |
|----------|---------|-------------|
| `DB_PASSWORD` | `changeme123` | Database password for MySQL user |
| `DB_ROOT_PASSWORD` | `rootchangeme123` | Root password for MySQL |
| `APP_USER_EMAIL` | `admin@example.com` | Initial admin email |
| `APP_USER_PASSWORD` | `admin` | Initial admin password |

**⚠️ Security Note**: 
- Change these default passwords before deploying to production!
- Change the admin credentials after first login!
- The app will work out of the box with defaults for testing

## Architecture

This app consists of 3 services:

1. **app**: PHP application (Laravel) serving on port 80
2. **database**: MySQL 8.2 database
3. **scraper**: SeleniumBase scraper for web scraping

## Data Persistence

The following directories are persisted:

- `${APP_DATA_DIR}/data/storage`: Application storage (uploaded files, cache)
- `${APP_DATA_DIR}/data/bootstrap/cache`: Laravel framework cache
- `${APP_DATA_DIR}/data/mysql`: MySQL database

## Original Project

Based on [PriceBuddy](https://github.com/jez500/pricebuddy) by Jez500.

For more information, visit: https://pricebuddy.jez.me/

