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
1.3 Routes in MVC
