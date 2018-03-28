# Installation

- [Prerequisites](#prerequisites)
- [Install RvMenu](#install-rv-menu)
- [Requirements and browser support](#requirements-and-browser-support)

## Prerequisites

This guide assumes that you already know how to [install](http://laravel.com/docs/5.4/installation) and configure Laravel and have the latest version of [Composer](https://getcomposer.org/) installed.

## Install Laravel RvMenu

Extract the files from the archive you have downloaded from CodeCanyon into a `packages/menu` folder in your project root.

Edit your `composer.json` file and add a [local path](https://getcomposer.org/doc/05-repositories.md#path) repository:

```javascript
"repositories": [
    {
        "type": "path",
        "url": "./packages/menu"
    }
]
```

**You can change folder `packages/menu` to `your-folder-name\menu` but need to make sure to change repository URL in composer.json.**
** If you composer has configuration for `minimum-stability`, please make sure that it allows dev version.**
```bash
minimum-stability: dev,
prefer-stable: true
```


In your terminal run:

```bash
composer require botble/menu *@dev
```

Next, you must install the service provider:

```php
// config/app.php
'providers' => [
    ...
    Botble\Menu\Providers\MenuServiceProvider::class,
];
```

For Laravel 5.1 and 5.2 you have to publish the migrations with:

```bash
php artisan vendor:publish --provider="Botble\Menu\Providers\MenuServiceProvider" --tag=migrations
```

Run the migrate command to create the necessary tables:

```bash
php artisan migrate
```

Publish the assets files with:

```bash
php artisan vendor:publish --provider="Botble\Menu\Providers\MenuServiceProvider" --tag=assets
```

You can publish the config file with:

```bash
php artisan vendor:publish --provider="Botble\Menu\Providers\MenuServiceProvider" --tag=config
```

Create a symbolic link from "public/storage" to "storage/app/public"

```bash
php artisan storage:link
```

Head over to the [Usage](usage.md) section to get started.

### Requirements and Browser Support

Laravel RvMenu requires Laravel >= 5.1.9 and supports the following browsers (desktop and mobile): Chrome, Firefox, Opera, Safari, MS Edge and IE10+.

<style>.docs-content ol { padding-left: 20px; }</style>
