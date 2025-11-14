### Telegram MiniApp integration for MoonShine

## Requirements

- MoonShine 3+
- Laravel 10+
- PHP 8.2+

#### Installation

```shell
composer require moonshine/telegram-mini-app
```

```shell
php artisan vendor:publish --provider="MoonShine\TlgMiniApp\Providers\TlgMiniAppServiceProvider"
```

```dotenv
TELEGRAM_BOT_TOKEN=<TOKEN_HERE>
```
Using the plugin requires the telegram_id field to be present in the table used to store users. If the default table (moonshine_users) is used, then simply running migrations is sufficient. 
```shell
php artisan migrate
```
If you are using a non-standard table, you need to find the migration [2025_10_31_144332_add_telegram_id_to_moonshine_users.php](database/migrations/2025_10_31_144332_add_telegram_id_to_moonshine_users.php) and replace the name of the moonshine_users table with the one you are using.
#### Usage

#### Set MiniApp url

<YOUR_HOST>/<MOONSHINE_ROUTE_PREFIX>/telegram-startapp
