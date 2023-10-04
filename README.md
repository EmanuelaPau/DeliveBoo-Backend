# <img src="public/logodeliveboo.png" height="30" margin-right="20px"/> Deliveboo

Deliveboo is a food delivery web app based in Luxemburg that allows customers to order food from their favorite restaurant without registration, but entering only the data necessary for delivery (Credit card number, name, address). Restaurateurs can register in the platform and create, modify and delete dishes and see statistics based on their customers orders.

<br>

<p align="center">
    <span align="left">
        <img src="public/gif1.gif" height="300px"/>
    </span>
</p>

<hr>

## Setup
-   Make a braintree sandbox profile<br>
-   Start MAMP <br>
-   Create database <br>
-   Duplicate .env.example and rename it .env , insert info in .env (change your app name, database name, port, mailer, ...)<br>
-   Add to your .env file:<br>

```
FRONTEND URL=hhtp://localhost:3000
SANCTUM_STATEFUL_DOMAINS=localhost:3000
SESSION_DOMAINS=localhost

MAIL_MAILER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your email
MAIL_PASSWORD=your password
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=hello@example.com
MAIL_FROM_NAME="$(APP_NAME)"

BRAINTREE_ENVIRONMENT=sandbox
BRAINTREE_MERCHANT_ID=your braintree merchant id
BRAINTREE_PUBLIC_KEY=your braintree public key
BRAINTREE_PRIVATE_KEY= your braintree private key

```
<br>

```
composer install
npm install
php artisan key:generate
php artisan storage:link
php artisan cache:clear
php artisan config:cache
php artisan breeze:install api
php artisan migrate --seed
composer require braintree/braintree_php
composer require guzzlehttp/guzzle

```
<hr>

## Compiles and hot-reloads for development, run in server

```
npm run watch
php artisan serve

```

<hr>

## Screenshots 

<br>
<p align="center">
    <span align="left">
        <img src="public/DeliveBoo Homepage.png" height="400px"/>
    </span>
    <span align="right">
        <img src="public/DeliveBoo Restaurant Search.png" height="400px">
    </span>
</p>

<br><br>
<p align="center">
    <span align="left">
        <img src="public/DeliveBoo Restaurant Menu.png" height="400px"/>
    </span>
    <span align="right">
        <img src="DeliveBooAboutUs.png" height="400px">
    </span>
</p>
<hr>

## Contributors

<a href="https://github.com/EmanuelaPau">Emanuela Pau</a><br>
<a href="https://github.com/AlexTimoncini">Alex Timoncini</a><br>
<a href="https://github.com/vito-pizzulli">Vito Pizzulli</a><br>
<a href="https://github.com/MarioSantoro/MarioSantoro">Mario Santoro</a><br>

<hr>