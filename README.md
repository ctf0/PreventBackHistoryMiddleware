# PreventBackHistoryMiddleware
http://way2php.com/prevent-browser-back-button-logout-laravel-5-3/

- save file to `app/Http/Middleware/PreventBackHistoryMiddleware.php`
- Then add this to the end of the ***web*** array in **app/Http/Kernel.php**

```php
\App\Http\Middleware\PreventBackHistoryMiddleware::class,
```

- and now group ur routes into

```php
Route::group(['middleware' => ['revalidate']], function () {
    // routes
});
```
