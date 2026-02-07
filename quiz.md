# Quiz — implemented features

This document summarizes implemented features.

- **Tryby quizu (Start screen)**
  - `Pełny rejs` (🚢): używa całej puli pytań.
  - `Rejs Pomników` (🗿): filtruje tylko pytania zawierające obrazek (`img`).
  - `Rejs Kapitański` (⛵): filtruje pytania bez obrazków.
  - `Rejs Piracki!` (🏴‍☠️): losowy wybór do 60 pytań z całej puli (jeśli puli < 60, bierze wszystkie).

- **Interfejs pytań**
  - Obsługa pytań jednokrotnego i wielokrotnego wyboru (`radio` / `checkbox`).
  - Losowe tasowanie pytań i tasowanie kolejności opcji przy każdym pytaniu.
  - Wyświetlanie obrazków (jeśli pole `img` jest podane) lub placeholdera, gdy tekst pyta o zdjęcie.
  - Pasek postępu i procent ukończenia (aktualizowany przy ładowaniu pytania).
  - `Sprawdź odpowiedź` i przycisk `Dalej` (pokazywany po sprawdzeniu).

- **Zachowanie po odpowiedzi**
  - Kolorowanie poprawnych i błędnych opcji (`reveal-correct` / `reveal-wrong`).
  - Automatyczne przejście do następnego pytania po 1s **tylko** gdy odpowiedź była poprawna.
  - Wynik (`score`) rośnie tylko przy poprawnej odpowiedzi.
  - `rationale` box (uzasadnienie) istnieje i jest ukryty domyślnie.

- **Nawigacja i kontrolki**
  - `✕` (exit) button na ekranie quizu: natychmiast powraca do ekranu startowego i anuluje ewentualny timer auto-advance.
  - Informacje o trybach: przycisk `i` w prawym górnym rogu ekranu startowego otwiera modal z opisem trybów; modal można zamknąć przyciskiem `✕`, Escape lub klikając poza kartą.

- **Wyniki**
  - Ekran wyników pokazuje punkty i maksymalną liczbę pytań oraz krótki komentarz zależny od stosunku punktów do puli.

- **Dostosowania wizualne**
  - Zmienione gradienty tła w stylu morskim (ciemne tło + jaśniejsza karta quizu).
  - Stylizowane przyciski, opcje i nagłówki dla lepszej czytelności.

- **Inne techniczne szczegóły**
  - Zmienna `autoNextTimer` przechowuje timeout dla automatycznego przejścia; jest czyszczona przy opuszczaniu quizu.
  - Funkcje pomocnicze: `shuffle(array)`, `startQuizMode(mode)`, `showQuestion()`, `checkAnswer()`, `handleNext()`, `showResults()`, `exitToStart()`, `showModeInfo()`, `closeModeInfo()`.

Plik główny: [index.html](index.html)

Jeśli chcesz, mogę dopisać do tego pliku przykładowe screeny, zmienić treść modalnych opisów lub dodać krótką instrukcję obsługi dla graczy.