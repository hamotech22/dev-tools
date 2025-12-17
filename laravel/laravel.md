# 🟥 Laravel Toolkit – أساسيات وأوامر مهمة

دليل عملي ومنظم لأساسيات **Laravel** والأوامر الأكثر استخدامًا، جاهز للرفع مباشرة على GitHub كملف **README.md**.

---

## 1️⃣ متطلبات التشغيل

- PHP >= 8.1
- Composer
- MySQL / PostgreSQL
- Node.js & npm (للـ frontend assets)

```bash
php -v
composer -V
```

---

## 2️⃣ إنشاء مشروع Laravel

```bash
composer create-project laravel/laravel my-project
cd my-project
php artisan serve
```

---

## 3️⃣ هيكلة المشروع الأساسية

```text
app/
 ├─ Http/
 │   ├─ Controllers/
 │   ├─ Middleware/
 ├─ Models/
 ├─ Providers/

routes/
 ├─ web.php
 ├─ api.php

resources/
 ├─ views/
 ├─ js/
 └─ css/

database/
 ├─ migrations/
 ├─ seeders/
 └─ factories/
```

---

## 4️⃣ Routes

### Web Routes
```php
Route::get('/', function () {
    return view('welcome');
});
```

### API Routes
```php
Route::get('/users', [UserController::class, 'index']);
```

---

## 5️⃣ Controllers

```bash
php artisan make:controller UserController
```

```php
class UserController extends Controller
{
    public function index() {
        return response()->json(User::all());
    }
}
```

---

## 6️⃣ Models & Migrations

```bash
php artisan make:model Product -m
```

```php
Schema::create('products', function (Blueprint $table) {
    $table->id();
    $table->string('name');
    $table->timestamps();
});
```

```bash
php artisan migrate
```

---

## 7️⃣ CRUD Example

```php
// Create
Product::create($request->all());

// Read
Product::all();

// Update
$product->update($request->all());

// Delete
$product->delete();
```

---

## 8️⃣ Validation

```php
$request->validate([
  'name' => 'required|min:3'
]);
```

---

## 9️⃣ Authentication

### Laravel Breeze
```bash
composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev
php artisan migrate
```

---

## 🔟 Middleware

```bash
php artisan make:middleware AdminMiddleware
```

```php
if (!auth()->user()->is_admin) {
   return redirect('/login');
}
```

---

## 1️⃣1️⃣ API Authentication (Sanctum)

```bash
composer require laravel/sanctum
php artisan migrate
```

---

## 1️⃣2️⃣ أوامر Artisan المهمة

```bash
php artisan serve
php artisan migrate
php artisan make:model ModelName
php artisan make:controller ControllerName
php artisan route:list
php artisan cache:clear
```

---

## 📌 Best Practices

- Logic في Controllers / Services
- استخدم Form Requests للـ Validation
- API في `api.php`
- Versioning للـ API

---

## 📂 جاهز للرفع على GitHub

- اسم الملف: `README.md`
- شرح فكرة المشروع
- API Endpoints
- Screenshots (إن وجد)

---

✨ **Laravel أفضل اختيار للـ Backend مع Angular أو React** 🚀

