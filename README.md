# CarDrive – prototyp launchera Android (wersja 0.2)

Projekt przygotowuje ekran główny CarDrive w ciemnej, niebiesko-czarnej stylistyce:
- panel Yanosika jako główny, duży kafel (otwiera pełną aplikację Yanosik),
- skróty do Map, Yanosika, telefonu, WhatsApp i Spotify,
- przycisk komend głosowych w języku polskim,
- deklaracja aplikacji jako HOME/launcher Android, aby można było wybrać ją jako ekran domowy.

## Ważne ograniczenia i rzeczy do sprawdzenia na radiu
1. Yanosik nie jest osadzony wewnątrz panelu. Android nie pozwala standardowemu launcherowi dowolnie wstawiać interfejsu innej aplikacji. Dotknięcie dużego panelu otwiera pełnego Yanosika; powrót wraca do CarDrive.
2. Pakiet Yanosika (`pl.neptis.yanosik.mobi.android`) może się różnić zależnie od wersji. Jeśli skrót nie otworzy aplikacji, trzeba odczytać właściwy identyfikator pakietu z radia.
3. Przycisk głosowy korzysta z Android RecognizerIntent w języku polskim. Wymaga dostępnej usługi rozpoznawania mowy i może wymagać internetu/Google. Nie jest to jeszcze pełny asystent samochodowy.
4. Przypisanie przycisku na kierownicy zależy od fabrycznego menu SWC/Key Study radia. Jeśli pozwala uruchamiać zewnętrzną aplikację, można spróbować wskazać CarDrive/VoiceActivity; nie można tego zagwarantować przed sprawdzeniem urządzenia.
5. Sterowanie tunerem FM wymaga integracji z aplikacją/radiem FM producenta NCS. Obecny prototyp nie przejmuje sterowania fabrycznym tunerem.
6. Ustawienie CarDrive jako domyślnego ekranu HOME powinno umożliwić jego wybór jako launchera. Automatyczne uruchamianie po zapłonie zależy też od firmware radia i jego ustawień startowych.

## Budowanie APK
Otwórz folder projektu w Android Studio, zsynchronizuj Gradle i wybierz:
Build > Build Bundle(s) / APK(s) > Build APK(s).

To nadal projekt źródłowy, nie gotowy APK. Nie został skompilowany ani przetestowany na radiu NCS.
