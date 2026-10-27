---
layout: doc
title: Polityka prywatności aplikacji Cellar
effective: 20 października 2026 r.
description: Jakie dane zbiera aplikacja Cellar, po co i jak długo je przechowuje.
---

## §1. Administrator danych

1. Administratorem danych osobowych Użytkowników aplikacji Cellar jest Jan Dąbrowski, ul. Kazimierza Wielkiego 41/8, 30-074 Kraków (dalej: „Administrator”).
2. We wszystkich sprawach dotyczących danych osobowych można pisać na adres [jandabrowski77@gmail.com](mailto:jandabrowski77@gmail.com).
3. Administrator nie wyznaczył inspektora ochrony danych – nie ma takiego obowiązku.
4. Pojęcia pisane wielką literą (Aplikacja, Konto, Skan, Katalog, Piwniczka) mają znaczenie nadane im w [Regulaminie aplikacji Cellar](regulamin).

## §2. Jakie dane przetwarzamy i dlaczego

Administrator przetwarza tylko dane potrzebne do działania Aplikacji. Podstawy prawne to art. 6 ust. 1 RODO: lit. b (wykonanie umowy, czyli Regulaminu), lit. c (obowiązek prawny), lit. f (prawnie uzasadniony interes Administratora) i lit. a (zgoda).

| Dane | Cel | Podstawa | Jak długo |
| --- | --- | --- | --- |
| Adres e-mail, hasło (przechowuje je wyłącznie Firebase Authentication, jako skrót, nie jawnym tekstem), identyfikator konta logowania | Założenie Konta, logowanie, potwierdzenie adresu e-mail, reset hasła | lit. b | Do usunięcia Konta |
| Z konta Google: adres e-mail, identyfikator Google, imię i nazwisko, zdjęcie profilowe | Logowanie przez Google, nazwa i zdjęcie w profilu | lit. b | Do usunięcia Konta |
| Z konta Apple: identyfikator Apple, adres e-mail (także ukryty adres przekierowujący Apple), imię i nazwisko, jeśli Użytkownik je udostępni | Logowanie przez Apple | lit. b | Do usunięcia Konta |
| Nazwa wyświetlana, własne zdjęcie profilowe | Profil Użytkownika | lit. b | Do zmiany lub usunięcia Konta |
| Piwniczka: butelki, statusy, ilość, oceny, notatki, cena, miejsce zakupu | Prowadzenie Piwniczki, zbiorcza ocena produktu w Katalogu | lit. b | Do usunięcia wpisu lub Konta |
| Skany: zdjęcia etykiet, tekst etykiety odczytany na telefonie, kod kreskowy, wynik rozpoznania, data | Rozpoznanie butelki | lit. b | Historia Skanów do usunięcia Konta |
| j.w. | Dzienne limity, kontrola kosztów, ochrona przed nadużyciami | lit. f | Do usunięcia Konta |
| Zdjęcia i tekst etykiet | Miniatury butelek, poprawa rozpoznawania etykiet | lit. f | Bez określonego terminu; po usunięciu Konta bez powiązania z Użytkownikiem |
| Informacje dodane do Katalogu i propozycje zmian | Wspólny Katalog | lit. b i f | Wpis w Katalogu bezterminowo; powiązanie z Kontem do jego usunięcia |
| Plan, data ważności Premium, identyfikator Konta w RevenueCat | Obsługa subskrypcji Premium | lit. b | Do usunięcia Konta |
| Zdarzenia płatności od RevenueCat (rodzaj subskrypcji, sklep, kraj, cena, identyfikator transakcji) | Rozliczenia i obowiązki podatkowe | lit. c i f | 5 lat od końca roku podatkowego |
| Potwierdzenia obejrzenia reklamy z nagrodą (identyfikator transakcji AdMob, data) | Przyznanie dodatkowych Skanów | lit. b | Do usunięcia Konta |
| Adres IP | Ochrona przed nadużyciami (limit Skanów na minutę) | lit. f | Tylko w pamięci serwera, kilka minut; nie jest zapisywany w bazie |
| Treść korespondencji e-mail | Odpowiedź na pytania, reklamacje, zgłoszenia | lit. b i f | Do załatwienia sprawy, potem do przedawnienia roszczeń |

Podanie danych jest dobrowolne, ale bez adresu e-mail (lub konta Google albo Apple) nie można założyć Konta. Administrator nie podejmuje wobec Użytkowników decyzji opartych wyłącznie na zautomatyzowanym przetwarzaniu, które wywoływałyby skutki prawne (art. 22 RODO).

## §3. Skanowanie i sztuczna inteligencja

1. Część rozpoznania dzieje się na telefonie, bez wysyłania zdjęcia do Google: odczyt tekstu etykiety, odczyt kodu kreskowego i wstępne sprawdzenie, czy zdjęcie przedstawia etykietę. Używa do tego biblioteki Google ML Kit, która może przesyłać Google anonimowe dane diagnostyczne o swoim działaniu.
2. Na serwer Administratora trafia zdjęcie etykiety (zmniejszone na telefonie), odczytany tekst i kod kreskowy. Przed wysyłką Aplikacja usuwa ze zdjęcia metadane zapisane przez aparat, w tym lokalizację.
3. Jeśli butelki nie da się rozpoznać po kodzie albo tekście, serwer wysyła zdjęcie lub tekst etykiety do modelu Claude firmy Anthropic. Anthropic nie otrzymuje adresu e-mail, nazwy Użytkownika ani identyfikatora Konta. Zgodnie z warunkami komercyjnymi Anthropic nie wykorzystuje tych danych do trenowania swoich modeli.
4. W Planie Premium model może wyszukać butelkę w internecie. Do wyszukiwarki trafia tylko tekst zapytania o produkt (np. nazwa i producent z etykiety).
5. Prosimy, by na zdjęciach były butelki i etykiety, a nie osoby, dokumenty czy inne dane osobowe.

## §4. Komu przekazujemy dane

Administrator nie sprzedaje danych. Serwer Aplikacji należy do Administratora i jest przez niego obsługiwany. Dane przekazuje tylko firmom, bez których Aplikacja nie mogłaby działać:

| Odbiorca | Jakie dane | Po co | Rola |
| --- | --- | --- | --- |
| Apple Distribution International (iCloud) | Kopie zapasowe danych z §2 | Przechowywanie kopii zapasowych | Podmiot przetwarzający |
| Anthropic, PBC (USA) | Zdjęcia i tekst etykiet | Rozpoznanie butelki (§3) | Podmiot przetwarzający |
| RevenueCat, Inc. (USA) | Identyfikator Konta, dane zakupów Premium | Obsługa i weryfikacja subskrypcji | Podmiot przetwarzający |
| Google Ireland Ltd (Firebase Authentication) | Adres e-mail, hasło (jako skrót), identyfikatory kont Google i Apple, adres IP i dane urządzenia przy logowaniu | Logowanie, wysyłka maili z potwierdzeniem adresu i resetem hasła | Podmiot przetwarzający |
| Google Ireland Ltd | Dane logowania kontem Google | Logowanie przez Google | Odrębny administrator |
| Apple Distribution International | Dane logowania kontem Apple | Logowanie przez Apple | Odrębny administrator |
| Google Ireland Ltd (AdMob) | Identyfikator reklamowy, dane urządzenia, adres IP, interakcje z reklamami | Wyświetlanie reklam w Planie Free, potwierdzanie reklam z nagrodą (§6) | Odrębny administrator |
| Google (Google Fonts, ML Kit) | Adres IP, anonimowe dane diagnostyczne | Pobranie czcionek Aplikacji, działanie odczytu etykiet na telefonie | Odrębny administrator |
| Apple Distribution International, Google Commerce Ltd | Dane zakupu i płatności | Sprzedaż Premium w App Store i Google Play | Odrębny administrator |

Administrator nie widzi danych karty ani innej metody płatności – obsługuje je sklep. Dane mogą też zostać udostępnione organom państwa, gdy wymaga tego prawo.

## §5. Przekazywanie danych poza Europejski Obszar Gospodarczy

1. Anthropic i RevenueCat mają siedziby w USA, a Google i Apple mogą przetwarzać dane także poza EOG.
2. Przekazanie odbywa się na podstawie decyzji Komisji Europejskiej o odpowiednim stopniu ochrony (EU-US Data Privacy Framework), jeśli odbiorca jest nim objęty, albo na podstawie standardowych klauzul umownych zatwierdzonych przez Komisję (art. 46 ust. 2 lit. c RODO).
3. Kopię zabezpieczeń można otrzymać, pisząc na adres [jandabrowski77@gmail.com](mailto:jandabrowski77@gmail.com).

## §6. Reklamy i zgody

1. W Planie Free Aplikacja wyświetla reklamy Google AdMob. W Planie Premium reklam nie ma.
2. Użytkowników z EOG, Wielkiej Brytanii i Szwajcarii Aplikacja przed pierwszą reklamą pyta o zgodę na reklamy spersonalizowane i użycie identyfikatorów urządzenia (komunikat Google). Podstawą jest zgoda (art. 6 ust. 1 lit. a RODO).
3. Bez zgody Aplikacja wyświetla reklamy niespersonalizowane. Google nadal przetwarza wtedy część danych (np. adres IP, przybliżoną lokalizację), aby wyświetlić reklamę i chronić przed oszustwami.
4. Zgodę można w każdej chwili zmienić lub wycofać w Aplikacji: Ustawienia → Prywatność reklam. Wycofanie zgody nie wpływa na zgodność z prawem przetwarzania przed jej wycofaniem.
5. Na iPhonie Aplikacja nie prosi o dostęp do identyfikatora reklamowego (IDFA) i nie śledzi Użytkownika w innych aplikacjach. Na Androidzie identyfikator reklamowy można zresetować lub usunąć w ustawieniach telefonu (Google → Reklamy).
6. Aplikacja wyświetla tylko reklamy przeznaczone dla dorosłych odbiorców i nie prowadzi reklam kierowanych do dzieci.
7. Więcej o tym, jak Google przetwarza dane: [policies.google.com/technologies/partner-sites](https://policies.google.com/technologies/partner-sites).

## §7. Dane na telefonie i uprawnienia

1. Na telefonie Aplikacja zapisuje tylko:
   1. dane sesji logowania – zapisuje je biblioteka Firebase Authentication (na iPhonie w Pęku kluczy, na Androidzie w pamięci Aplikacji),
   2. adres serwera Aplikacji i proste ustawienia.
2. Aplikacja nie używa plików cookies ani narzędzi analitycznych do śledzenia Użytkownika.
3. Aplikacja prosi o uprawnienia tylko wtedy, gdy są potrzebne:
   1. **aparat** – zdjęcia etykiet, kody kreskowe, zdjęcie profilowe,
   2. **zdjęcia (galeria)** – wybór zdjęcia etykiety lub zdjęcia profilowego; Aplikacja widzi tylko zdjęcia wybrane przez Użytkownika.
4. Uprawnienia można w każdej chwili cofnąć w ustawieniach telefonu. Bez aparatu kod kreskowy można wpisać ręcznie, a zdjęcie wybrać z galerii.
5. Aplikacja nie pobiera lokalizacji telefonu, kontaktów ani nagrań dźwięku.

## §8. Twoje prawa

1. Użytkownik ma prawo do:
   1. dostępu do swoich danych i otrzymania ich kopii (art. 15 RODO),
   2. sprostowania danych (art. 16),
   3. usunięcia danych (art. 17),
   4. ograniczenia przetwarzania (art. 18),
   5. przeniesienia danych przetwarzanych na podstawie umowy lub zgody (art. 20),
   6. sprzeciwu wobec przetwarzania opartego na prawnie uzasadnionym interesie (art. 21),
   7. wycofania zgody w dowolnym momencie (art. 7 ust. 3).
2. Konto razem z Piwniczką, ocenami, historią Skanów, zdjęciem profilowym i kontem logowania w Firebase Authentication można usunąć samodzielnie: Ustawienia → Usuń konto.
3. Zdjęcia etykiet i informacje w Katalogu zostają po usunięciu Konta bez powiązania z Użytkownikiem ([Regulamin](regulamin), §3 i §5). Jeśli zdjęcie zawiera dane osobowe (np. twarz lub dokument), na żądanie Administrator je usunie.
4. Pozostałe żądania należy wysyłać na adres [jandabrowski77@gmail.com](mailto:jandabrowski77@gmail.com). Administrator odpowiada w ciągu miesiąca. W wyjątkowych przypadkach termin może zostać wydłużony o kolejne dwa miesiące, o czym Administrator informuje. Może poprosić o potwierdzenie tożsamości, np. wiadomością z adresu e-mail Konta.
5. Użytkownik może złożyć skargę do Prezesa Urzędu Ochrony Danych Osobowych (ul. Stawki 2, 00-193 Warszawa, [uodo.gov.pl](https://uodo.gov.pl)), jeśli uważa, że jego dane są przetwarzane niezgodnie z prawem.

## §9. Postanowienia końcowe

1. Aplikacja jest przeznaczona wyłącznie dla osób pełnoletnich. Administrator nie zbiera świadomie danych osób poniżej 18 lat. Konto takiej osoby zostanie usunięte po zgłoszeniu.
2. Administrator chroni dane m.in. przez szyfrowane połączenie (HTTPS) między Aplikacją a serwerem, przechowywanie haseł wyłącznie jako skrót kryptograficzny w Firebase Authentication (serwer Aplikacji haseł nie zna), ograniczony dostęp do serwera i regularne kopie zapasowe.
3. O zmianach polityki Administrator informuje w Aplikacji. O istotnych zmianach, np. nowym celu przetwarzania lub nowym odbiorcy danych, informuje z wyprzedzeniem.
4. Polityka obowiązuje od 20 października 2026 r.
