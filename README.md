## Building a Laravel 10 Auth Application with Vue 3

1.  create a new Laravel project via Composer:
```
composer create-project laravel/laravel l10-ui-vue3-auth
```
2.  Install the frontend scaffolding using the `laravel/ui` with `bootstrap 5.2` and `vue3`
```
composer require laravel/ui
php artisan ui vue --auth
npm install
npm run dev
```
3. Install the `vue-router` package and create simple SPA
```
npm install vue-router --dev
```
4.  SPA Auth using sanctum
