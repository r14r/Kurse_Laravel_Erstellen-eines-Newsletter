#

## Install NodeJS

## Install PHP, Laravel und Composer

## Erstellen derBasis-Anwendung

```shell
laravel new App --jet --teams --stack livewire
```

```shell
composer require spatie/laravel-newsletter 
```

```shell
php artisan vendor:publish --provider="Spatie\Newsletter\NewsletterServiceProvider"
```

## Laravel Datenbank konfogirueren

```config
DB_CONNETION=sqlite
```

```shell
touch database/database.sqlite
php artisan migrate
```

## Laravel konfigurieren

```app/config/fortify.php```

```php
'features' => [
    Features::emailVerification(), 
```

```app/config/jetstream.php```

```php
'features' => [
    Features::termsAndPrivacyPolicy(),
    Features::profilePhotos(),
```

```app/Models/User.php```

```php
class User extends Authenticatable implements MustVerifyEmail
```
