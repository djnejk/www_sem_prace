# Česnekomat – semestrální práce (Frontend webové aplikace)

Statický frontend kioskové webové aplikace **Česnekomat** – samoobslužný automat na prodej českého česneku a vyzvednutí rezervace.

* **HTML + CSS** (bez povinného JavaScriptu)
* **Responzivní layout** (min. 3 stavy: výchozí / 720 px / 420 px)
* **Bez CSS/JS frameworků**
* Projekt je záměrně statický – prvky (klávesnice, +/−, platba) jsou pouze **vizuální prototyp**.

## Obsah / Obrazovky (layouty)

Repozitář obsahuje několik samostatných statických layoutů (HTML soubory):

* `index.html` – vstupní stránka (start)
* `main.html` – hlavní menu (volba akce)
* `pickup.html` – vyzvednutí rezervace (zadání 6místného PIN – pouze vzhled)
* `buy.html` – výběr množství a platby (hotově / kartou – pouze vzhled)
* `checkout-cash.html` – průběh platby hotově (stav zařízení + souhrn částek)
* `checkout-card.html` – průběh platby kartou (stav terminálu + souhrn)
* `success.html` – potvrzení úspěšného nákupu (dokončení)

### Navigační tok (simulace)

* **Standby / start → Main**
* **Main → (Pickup / Buy)**
* **Buy → (Checkout cash / Checkout card) → Success**
* **Success → zpět na začátek**

> Pozn.: V rámci statického prototypu jsou některé kroky řešeny jen jako odkazy (bez logiky a bez zpracování vstupů).

## Struktura projektu

* `css/` – společné styly

  * `css/styles.css` – jednotné styly pro všechny obrazovky
* `favicon/` – ikony a manifest pro aplikaci (favicon + PWA manifest)

## Spuštění

Projekt je čistě statický – stačí otevřít v prohlížeči:

1. Stáhnout / naklonovat repozitář:

   * `git clone https://github.com/djnejk/www_sem_prace.git`
2. Otevřít `index.html` v prohlížeči
   *(doporučeno: VS Code → rozšíření Live Server pro pohodlný lokální běh)*

## Použité technologie

* HTML5 (sémantické značky: `header`, `main`, `nav`, `section`, `footer`)
* CSS3 (CSS proměnné, grid/flex, responzivita přes media queries)
* SVG ikony vložené přímo do HTML
* Bez externích knihoven a frameworků

## Responzivita

Layout je navržen pro kiosk/desktop, tablet i mobil:

* výchozí styl (desktop / kiosk)
* `@media (max-width: 720px)` – tablet / menší displeje
* `@media (max-width: 420px)` – malé telefony

## Přístupnost (A11y)

* ovládací prvky jsou řešeny jako odkazy/tlačítka podle účelu (navigace vs. akce)
* fokus pro klávesnici je zvýrazněn (`:focus-visible`)
* použity popisky `aria-label` tam, kde dává smysl
* doplňkový text pro čtečky (`.sr-only`) u prvků, které jsou primárně vizuální

## Validace

* HTML: doporučeno ověřit přes W3C HTML validator
* CSS: doporučeno ověřit přes W3C CSS validator

## Autor

* Jiří Januš (@djnejk)
* © 2025 DjDevs.eu




Chceš README spíš **stručnější (1 obrazovka textu)**, nebo naopak doplnit i sekci **„Požadavky ze zadání a jak jsou splněné“** (aby to bylo přímo obhajitelné)?
