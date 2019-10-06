Rails6.0の環境を簡単に作りたかっただけ

1. Clone
```sh
git clone
```

2. Project Initialization
```
docker-compose run web rails new . --force --no-deps --database=mysql
```

3. Edit database.yml 
```src/config/database.yml
default: &default
  adapter: mysql2
  encoding: utf8mb4
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  username: root
  password: root
  host: db
```

4. Create src/config/webpacker.yml
https://raw.githubusercontent.com/rails/webpacker/master/lib/install/config/webpacker.yml


5. Run
```
docker-compose up
```
