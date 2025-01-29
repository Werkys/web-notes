# web-notes

## Založení codeigniteru

Při zakládání nového projektu pak od příkazového řádku napíšeme následující kod:

> composer create-project codeigniter4/appstarter project-root


1) Ze složky public vytáhnu všechny čtyři soubory do složky projektu.
2) Otevřu si soubor index.php (původně byl ve složce public, takže nyní je ve složce projektu) a upravím jeho kód
> FCPATH . '../app/Config/Paths.php';

  umažu dvě tečky a lomítko (protože jsme soubor přesunul o složku nahoru)

3) Nastavím soubor env:
jednak ho přejmenuju na .env
otevřu jej a odkomentuju proměnnou CI_Enviroment (umazáním hashtagu) a hodnotu nastavím na development (díky tomu mně bude CodeIgniter napovídat s případnými chybami)



##
