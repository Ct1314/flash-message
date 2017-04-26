# Laravel flash-message Help you quickly achieve message prompts
# Requirement
- PHP 5.6+
- toastr
- laravel 5.3+

# Features
- message prompt
- laravel flash session
- combined with toastr

# Install
`composer require yuanchang/laravel-flash`

# usage
## provider and alias
config/app.php
```php
providers=>[
    Flash\FlashServiceProvider::class,
]
alias=>[
    'Flash'=>Flash\FlashFacade::class,
]
```

## command
`php artisan vendor:publish --tag="flash-message"`

## resource 

```html
<link rel="stylesheet" href="/public/vendor/ly-message/toastr.css"></link>
<script src="/public/vendor/ly-message/toastr.js"></script>
```
## use
```php

use Flash;

Flash::success('success','success info');
Flash::info('info','info...');
Flash::warning('warning','warning info');
Flash::error('error','error info');

```

```php
you.blade.php

{!! Flash::render() !!}
```