# LEGO Speed Champions garázsvásár

Statikus, reszponzív értékesítési oldal. Nincs szükség buildre vagy szerveroldali alkalmazásra: a publikálható webhely teljes tartalma a `dist` mappában található.

## Helyi futtatás

PowerShellből, a projekt gyökerében:

```powershell
py -m http.server 8080 -d dist
```

Ezután nyisd meg: <http://localhost:8080>

Ha a `py` parancs nem érhető el, ugyanez futtatható a `python -m http.server 8080 -d dist` paranccsal.

## Publikálás GitHub Pagesre

1. Hozz létre egy üres GitHub repositoryt.
2. Töltsd fel vagy pushold bele ennek a mappának a tartalmát.
3. A repository **Settings → Pages → Build and deployment → Source** beállításánál válaszd a **GitHub Actions** lehetőséget.
4. Pusholj a `main` vagy `master` ágra, vagy indítsd el kézzel a **Deploy static site to GitHub Pages** workflow-t az Actions oldalon.

A workflow közvetlenül a `dist` mappát publikálja, ezért a projekt almappás GitHub Pages-címen is működik.

## Fájlstruktúra

- `dist/index.html` – az oldal belépési pontja
- `dist/assets/` – CSS és JavaScript
- `dist/images/` – termékfotók
- `.github/workflows/pages.yml` – automatikus GitHub Pages-publikálás

## Megjegyzés

A Messenger- és Telegram-hivatkozások külső oldalakra mutatnak. Az oldal nem tartalmaz szerveroldali adatkezelést vagy titkos kulcsot.
