---
noneSelected: A rendszer modell szükséges.
invalidVersion: Ez nem tűnik egy érvényes rendszer verziónak.
head:
  - - script
    - src: /assets/js/selecting.js
---

# Kezdeti lépések

Mielőtt elkezdenénk ezt az útmutatót, ellenőrizzük, hogy van-e már egyedi firmware telepítve, illetve mi a konzolod jelenlegi rendszer verziója.

### Section I - CFW Check

1. Kapcsold ki a konzolod
2. Nyomd le és tartsd nyomva (Select) gombot
3. Kapcsold be a konzolod, miközben nyomva tartod a (Select) gombot
4. Ha nem látod az egyedi menüt (a konzolod a HOME Menü-be bootol), akkor folytasd a következő résszel

::: warning

Ha a Luma3DS konfigurációs képernyőt vagy egyéb egyedi menüt (pl. GodMode9, Decrypt9WIP), ÁLLJ - már van egyedi firmware-ed! Folytasd [innen](checking-for-cfw#what-to-do-next).

:::

### Section II - System Version Check

1. Lépj be a "System Settings"-be a konzolodon
2. Your system version will be displayed on the bottom right of the top screen (e.g. "Ver. 11.17.0-50U")

### Section III - Select a Method

A korrrekt metódushoz a konzolodhoz, kérjük add meg azt a rendszer verziót, amit a II. részben találtál.

<!--@include: @/_internal/consoleVersionSelect.html -->

---

#### Alternate Methods

Ha lehetséges, azt a metódust kell követned, ami feljebb látszik.

Egyéb esetekben más, az összes verziónál használható metódus elérhető, de további hardvert igényelnek:

1. [ntrboot](ntrboot) - kompatibilis DS flashcard-ra van szükség hozzá
2. [Boot9strap telepítése (Hardmod)](installing-boot9strap-\(hardmod\)) - forrasztást igényel