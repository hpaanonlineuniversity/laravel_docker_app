check .env file for database connection according to compose.yml

DB_CONNECTION=mysql
DB_HOST=mysql_db    # docker-compose.yml မှာပေးထားတဲ့ container_name နဲ့တူရမယ်
DB_PORT=3306
DB_DATABASE=laravel_db
DB_USERNAME=laravel_user
DB_PASSWORD=secret


docker compose up -d

docker compose exec app php artisan key:generate

docker compose exec app php artisan migrate

docker compose exec app php artisan storage:link

စမ်းသပ်ကြည့်ရန်

    Website: http://localhost:8000