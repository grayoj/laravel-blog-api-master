## Laravel Blog Rest API
This the blog rest API project as requested with the following blog features.
1.  Authentication (I included it)
2.  Article
3.  Author
4.  comment
5. Categories

## How to install ?

```
git clone <The Repo Link>
cd laravel-blog-api
composer install

```
## Configure the .env file

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel-blog-api
DB_USERNAME=db_root
DB_PASSWORD=

I did not set a password.

```

## STEPS TO TAKE 

Firstly, you must migrate.
```
php artisan migrate
```

Next step is to generate key for the application
```
php artisan key:generate
http://localhost:8000

```
## Components and features
Article Add/Update/Delete/Search/Article
Category Add/Update/Delete/Search
Comment Add/Update/Delete
The Author/User - Signup/Login/Logout

## API Authentication and Authorization
Category - authentication required for add/update/delete
Article - authentication required for add/update/delete
Author - authentication required for details/delete
Comment - authentication required for add/update/delete
    
## API Endpoints

I created API endpoints that could be tested via Postman, specifically Swagger as in the test task.

<b>Categories</b>
Add - /api/category/store 
Update - /api/category/{id}/update 
delete - /api/category/{id}/delete 
view - /api/category/{id}/view 
All - /api/categories
Search - /api/category/{keyword}/search
        
<b>For Articles</b>
Add - /api/article/store 
Update - /api/article/{id}/update 
Delete - /api/article/{id}/delete 
view - /api/article/{id}/view 
All - /api/articles
Search - /api/article/{keyword}/search

<b>For Comments</b> As requested
Add - /api/comment/store 
Update - /api/comment/{id}/update 
delete -> /api/comment/{id}/delete 
view -> /api/comment/{id}/view 
All -> /api/comment

<b>For User Auth</b>
signup -> /api/register 
Login -> /api/login
Logout -> /api/logout
        

Faker could be used to generate dummy data.
Use ``php artisan tinker``
```
factory(App\ModelName::class,number_of_column)->create()
```

To test this API project you can use swagger or postman.
For authentication, use:
```
‘headers’ => [
    ‘Accept’ => ‘application/json’,
    ‘Authorization’ => ‘Bearer ‘.$accessToken,
]
```

## Thank You, Hope I did well.

## Gerald Maduabuchi
