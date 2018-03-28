# Configuration

```php
<?php

return [
    'route' => [
        'prefix' => 'menu',
        'middleware' => ['web'],
    ],
    'cache' => [
        'enable' => false,
        'stored_keys' => storage_path('menu_cache_keys.json'),
    ],

    // assets libraries, you can remove if it's existed on your project
    'libraries' => [
        'stylesheets' => [
            'https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css',
            'vendor/menu/packages/nestable/jquery.nestable.min.css',
            'vendor/menu/packages/toastr/toastr.min.css',
            'vendor/menu/packages/fancybox/jquery.fancybox.min.css',
            'vendor/menu/packages/font-awesome/css/font-awesome.min.css',
            'vendor/menu/css/menu.css?v=' . env('RV_MENU_VERSION', time()),
        ],
        'javascript' => [
            'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js', // Comment it if your site has it already
            'vendor/menu/packages/nestable/jquery.nestable.min.js',
            'vendor/menu/packages/toastr/toastr.min.js',
            'vendor/menu/packages/fancybox/jquery.fancybox.min.js',
            'vendor/menu/js/main.js?v=' . env('RV_MENU_VERSION', time()),
            'vendor/menu/js/menu.js?v=' . env('RV_MENU_VERSION', time()),
        ],
    ],
];

```