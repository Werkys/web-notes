# web-notes

## Založení codeigniteru

Při zakládání nového projektu pak od příkazového řádku napíšeme následující kod:

> composer create-project codeigniter4/appstarter project-root


1) Ze složky public vytáhnu všechny čtyři soubory do složky projektu.
2) Otevřu si soubor index.php (původně byl ve složce public, takže nyní je ve složce projektu) a upravím jeho kód
> FCPATH . '../app/Config/Paths.php';

**umažu dvě tečky a lomítko** (protože jsme soubor přesunul o složku nahoru)

3) Nastavím soubor env:
jednak ho přejmenuju na .env
otevřu jej a odkomentuju proměnnou CI_Enviroment (umazáním hashtagu) a hodnotu nastavím na development (díky tomu mně bude CodeIgniter napovídat s případnými chybami)

musíme si taky nastavit base url. půjdeme do app/Config soubor App.php kde base url nastavíme. 
> public string $baseURL = 'http://localhost:8080/'; <br>
  ⬇️ <br>
> public string $baseURL = 'http://localhost/jancik/projektobce/';


❓ projekt obce je v tomto případě název projektu

## Tvoření controllerů

do terminalů napíšeme:

> php spark make:controller

po enteru se nám dá možnost pojmenovat controller ➡️ enter ➡️ controller existuje

❓většinou si první controller pojmenujem Main

Ve vytvořeném controlleru Main si do metody index napíšeme echo view ("index");

>public function index() <br>
    { <br>
        echo view ("index"); <br >
    } <br>

## Tvoření Routes

najdeme si soubor routes App/config soubor Routes.php

zde si u index Route předěláme Home na Main (pokud se tak jmenuje náš controller)

>$routes->get('/', 'Home::index'); <br>
>⬇️<br>
>$routes->get('/', 'Main::index');<br>


## Tvoření stránek
Ve Views si založíme nový soubor index.php. Za předpokladu že jsme udělali všechny ostatní kroky správně, by nám už teď měla fungovat po refreshnutí "stránka".
