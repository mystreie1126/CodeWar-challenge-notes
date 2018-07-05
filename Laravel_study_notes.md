# Laravel-Basics

### 1.*Routes* ->just refers the URL in Address bar.

1.1 pass variable through routes
```
Route::get('/{id}/{name}',function($id,$name){ 
    return $id.$name;
});
```
1.2 naming the routes 
```
Route::get('/admin/aasda/1231ad/asdq12300', array('as'=>'some',function(){
	$url = route('some');
	return $url;
}));
```
1.3 [Routes in MVC](https://stackoverflow.com/questions/12430181/how-does-mvc-routing-work)



### 2.Controller

2.1

**php artisan make:controller controllerName** just create a empty controller class

**php artisan make:controller --resource controllerName** create a controller class with CRUD functions by default

2.2 **Route::resource('post','PostController')** blind the post URL to the PostController includes all the http methods

### 3.Migration

create the database table strucure 

*php artisan make:migration migration_class_name --create="table name"* create table migration 
*php artisan migrate* make migrate to all tables
*php artisan make:migration add_migration_to_a_table --table="target table"* add column to a table

**3.1 add a column to a exsist table**

Command:*php artisan make:migration add_migration_to_a_table --table="target table"* add column to a table

table class:
```
public function up(){
   Schema::table('posts', function (Blueprint $table) {
   	//column added
	$table->integer('is_admin')->unsigned();   
        });
}

public function down()
    {
        Schema::table('posts', function (Blueprint $table) {
	//column deleted: php artisan migrate:rollback
            $table->dropColumn('is_admin');
        });
    }
```

