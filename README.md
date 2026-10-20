# Cellar

**Zrób zdjęcie etykiety – Cellar powie Ci, co pijesz.** Aplikacja mobilna (iOS i Android), która rozpoznaje wino, whisky czy piwo po zdjęciu etykiety albo kodzie kreskowym, opisuje jego smak i zapisuje butelkę w prywatnej piwniczce.

Strona: **[jandabrowski2002.github.io/cellar](https://jandabrowski2002.github.io/cellar/)** · [Regulamin](https://jandabrowski2002.github.io/cellar/regulamin) · [Polityka prywatności](https://jandabrowski2002.github.io/cellar/prywatnosc)

> To repozytorium zawiera stronę aplikacji i jej dokumenty. Kod aplikacji i serwera jest w osobnym, prywatnym repozytorium – chętnie pokażę go na rozmowie.

## Co robi

- **Skan etykiety lub kodu kreskowego** – zdjęcie przodu wystarczy; tył butelki uzupełnia szczepy, rocznik i moc.
- **Profil smaku** – trzy proste zdania o barwie, zapachu i smaku.
- **Piwniczka** – listy „Mam”, „Chcę mieć”, „Degustowane”, „Widziane”, z oceną 0–10, ceną i notatkami.
- **Wspólny katalog** – potwierdzone butelki trafiają do bazy, więc kolejny skan tej samej etykiety jest natychmiastowy i darmowy.

## Jak działa rozpoznawanie

Każdy skan zaczyna od najtańszego sposobu i idzie wyżej tylko przy wątpliwościach:

| # | Szczebel | Koszt / skan |
|---|---|---|
| 1 | Znany kod kreskowy → produkt z bazy | 0 ¢ |
| 2 | OCR na telefonie (ML Kit) porównany z katalogiem i potwierdzonymi skanami (pg_trgm) | 0 ¢ |
| 3 | Claude Haiku czyta sam tekst OCR (~20× mniej tokenów niż zdjęcie) | ułamek centa |
| 4 | Claude Haiku czyta zdjęcie i weryfikuje kandydatów z bazy | ok. 0,05 ¢ |
| 5 | Wyszukiwanie w internecie (tylko Premium) | ok. 1 ¢ |

## Technologie

| Warstwa | Stos |
|---|---|
| Aplikacja | Flutter / Dart – jedna baza kodu na iOS i Androida |
| Serwer | ASP.NET Core 8 (minimal API), EF Core, ASP.NET Identity, logowanie Google |
| Baza | PostgreSQL + `pg_trgm` (wyszukiwanie rozmyte) |
| AI | Anthropic API – Claude Haiku: structured outputs (JSON Schema), web search |
| Na urządzeniu | Google ML Kit – OCR, kody kreskowe, klasyfikacja zdjęcia przed wysyłką |
| Monetyzacja | RevenueCat (StoreKit 2, Google Play Billing, webhooki), AdMob z server-side verification |

## Decyzje projektowe

- **Spike przed budową** – najpierw test odczytu etykiet z progami go/no-go (trafność nazwy i producenta, kategorii, rocznika; mediana czasu; koszt skanu) na prawdziwych zdjęciach, porównanie modeli i poziomów wysiłku.
- **Kontrola kosztów AI** – dzienny budżet całej aplikacji z bezpiecznikiem, limity na plan i użytkownika, rate limiting na minutę; odrzucone skany też liczą się do limitów.
- **Pochodzenie danych** – każde pole produktu pamięta źródło (etykieta, wiedza modelu, internet, użytkownik). Wiedza modelu nigdy nie nadpisuje danych z etykiety, a zmianę istniejącej wartości musi potwierdzić kilku niezależnych użytkowników.
- **Prywatność** – zdjęcia są zmniejszane i czyszczone z metadanych (GPS) na telefonie; zgoda RODO na reklamy przez Google UMP.

## Autor

Jan Dąbrowski – [jandabrowski77@gmail.com](mailto:jandabrowski77@gmail.com)

## Strona

Statyczna strona na GitHub Pages (Jekyll), bez zewnętrznych skryptów, czcionek i ciasteczek. Dokumenty są w Markdownie (`regulamin.md`, `prywatnosc.md`), wygląd w `_layouts/` i `assets/style.css`.
