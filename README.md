# fitra-nurakbar
Development Setup
Prerequisites
Pertama, pastikan kalian sudah punya PHP.
Kedua, mempunyai nodejs beserta Node Package Manager atau Yarn
Ketiga, jangan lupa kalian sudah terinstall juga Composer
Terakhir, pastikan kalian juga sudah punya database relasional seperti MySQL, PostgreSQL atau SQLite
Setting Up Project
Silahkan fork terlebih dahulu repository ini, kemudian clone repository yang udah kalian fork ya (Inget repository yang kalian fork, bukan repository ini). Bisa gunakan command berikut:

git clone git@github.com:{username github kalian}/laract9.git
# atau kalo kalian pake https (bukan ssh)
git clone https://github.com/{username github kalian}/laract9.git
Kemudian, buka terminal seperti bash, zsh, command prompt atau powershell dan nstall dependency composer dengan command berikut

composer install && composer update
Lanjut, copy file .env.example dengan nama .env sebagai berikut:

cp .env.example .env
Kemudian, silahkan ganti credentials database di file .env nya seperti

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=xxx
DB_USERNAME=root
DB_PASSWORD=
untuk panduan atau dokumentasi mengenai setup database pada file .env bisa kalian baca pada dokumentasi resmi laravelnya ya cui, klik disini.

Kemudian, silahkan migrate semua database di project ini dengan menggunakan artisan command:

php artisan migrate
Lanjut, generate aplikasi key untuk keamanan pada project laravel dengan menggunakan artisan command berikut:

php artisan key:generate
# atau 
php artisan key:generate --show
Install dependencies nodejs didalam folder node_modules menggunakan Npm atau Yarn:

npm install && npm run dev
# atau menggunakan Yarn
yarn && yarn dev
# atau menggunakan pnpm
pnpm i && pnpm dev
Langkah Terakhir, silahkan jalankan local development server Laravel dengan menggunakan artisan command sebagai berikut:

php artisan serve
Project ini akan berjalan di https://localhost:8080.
