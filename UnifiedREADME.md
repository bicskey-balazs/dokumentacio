# Vizsgaremek: Skillstree

## Leírás:
Az elkészült termék egy kurzuskezelő/e-learning felület, a bejelentkezett felhasználó tud tanulni kurzusokban, illetve létrehozni saját kurzusokat.
Lehetőség van a leckékhez és a kurzusokhoz kép- és videófeltöltésre is, a szöveges tartalmakon felül.

## Használati módok:

### Távoli elérés
A projekt elérhető a jcloud kubernetes szerveren, a következő címen:
[http://skillstree-vizsgaremek-frontend.jcloud.jedlik.cloud](http://skillstree-vizsgaremek-frontend.jcloud.jedlik.cloud)

### Lokális futtatás:
A projekt lokális futtatásához a következő technológiák szükségesek:
1. Frontend:
    - [Node 20+](https://nodejs.org/en/download)
2. Backend(Konténerizált)
    - [Docker](https://docs.docker.com/desktop/setup/install/windows-install/)
3. Backend(Lokális)
    - [PostgresSQL](https://www.postgresql.org/download/linux/ubuntu/)
    - [Laravel 12+](https://laravel.com/docs/12.x/installation)
    - [Ubuntu alapú linux disztribúcíó](https://ubuntu.com/)

## Lokális project indítása:
1. Frontend indítása:
    - npm run dev
2. Backend(Docker):
    - docker mappában -> "docker compose up" parancs kiadása
    - docker-setup.bat futtatása
    - alábbi két parancs kiadása a terminálban(amiben a docker-setup.bat futtott):
        chown -R www-data:www-data storage bootstrap/cache
        chmod -R 775 storage bootstrap/cache
3. Backend(Lokális):
    - Amennyiben szükség van a generált adatokra: php artisan migrate:fresh --seed
    - php artisan serve

## Demo fiókok:

1. Adminisztrátor fiók (Rendszergazda) Teljes hozzáférés.
    -	E-mail cím: ad@m.in
    -	Jelszó: admin123
2. Általános Teszt Felhasználó (Tanuló / Oktató)Normális felhasználói élmény.
    -	E-mail cím: us@e.r
    -   Jelszó: useruser

## Készítők:

  - [Anda Kristóf](https://github.com/anda-kristof/)
  - [Bicskey Balázs](https://github.com/bicskey-balazs)
  - [Borbély Dominik Péter](https://github.com/borbely-dominik-peter)
