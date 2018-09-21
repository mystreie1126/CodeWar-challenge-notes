# Laravel-Basics

### 1.*secure_asset()* render the default css file from laravel

From the blade template 
```
<link rel="stylesheet" href="{{secure_asset('css/app.css')}}" type="text/css" /> 
```
renders the *localhost/public/css/app.css* file, *secure_asset* sending a https request 

1.3 [Routes in MVC](https://stackoverflow.com/questions/12430181/how-does-mvc-routing-work)



### 2.Controller

2.1

**php artisan make:controller controllerName** just create a empty controller class

**php artisan make:controller --resource controllerName** create a controller class with CRUD functions by default

2.2 **Route::resource('post','PostController')** blind the post URL to the PostController includes all the http methods


```

