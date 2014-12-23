# Přehazování a opakující se získávání informací

Viděl jsem, že lidé co vytvářeli specifikaci si kód staré aplikace vytiskli, procházeli ho a tímto způsobem vytvářeli specifikaci. Co to znamenalo pro ostatní lidi na projektu?

Tým, který tvořil specifikaci získal tímto většinou brutálním způsobem vědomosti a zapsal je do dokumentů. Pokud to bylo nezbytné, komunikovali o aplikaci s uživatelem aplikace.

Pak tyto dokumenty předali týmu designerů a architektů. Aby tito lidé pochopili co je v dokumentech napsáno, tak pravidelně komunikovali s týmem, který tuto specifikaci vytvořil. Během této doby získávání znalostí o aplikaci tvořili architekturu a podklady pro programátory.

Po té, se předala specifikace a design programátorům. Aby pochopili co mají naprogramovat, tak komunikovali nejdříve s designéry a následně s týmem co tvořil specifikaci. Byla tam několika měsíční mezera, než se design vytvořil. Stávalo se, že člověk co tvořil specifikaci už nebyl na projektu a tudíž se nemohl naplno věnovat odpovídání otázek od programátorů.

Když bylo všechno naspecifikováno a naprogramováno, předala se aplikace testerům. Ti si vzali specifikaci a vytvořili si z ní testovací scénáře. Pokud se jim podařilo sehnat někoho ze specifikačního týmu, tak s ním komunikovali. V opačném případě testovali aplikaci dle nejlepšího svědomí.

Během programování se našlo velké množství chyb ve specifikaci a designu. Ty se musely opravit a opravy nechat schválit od zákazníka.

Aby jste si predstavili, kolik chyb se v těchto dokumentech našlo. Z počátku žádné, protože nikdo z programátorů nevěděl co má aplikace přesně dělat. Po měsíci se objevili první dotazy a změny ve specifikaci. Po dalším měsíci další a další. Ke konci vývoje (několik posledních měsíců) to byly průměrně 3 změny ve specifikaci za den. To generovalo další a další změny v kódu a designu. Každá změna mohla narušit stabilitu systému a proto se musela aplikace přetestovat.

A jak to bylo s kvalitou testování? Testovací scénáře se tvořili na základě specifikace, která samozdřejmě nebyla ideální a obsahovala spoustu chyb. Naše testování nebylo ale úplně zbytečné. Během testování se našlo velké množství chyb v programu (způsobené chybami v kódu, specifikaci a designu).

#### Co jsme se naučili

* Neexistuje 100% bezchybná specifikace.
* Netvořit aplikaci z dokumentace, ale tvořit ji základě toho, co zákazník potřebuje.
* Pokud bychom dali stejnou specifikaci různým realizačním týmům, vzniklo by několik různých implementací. Proto nelze na specifikaci spoléhat jako na důvěryhodný zdroj informací.
* V aplikaci je tím více chyb, čím více týmů navazuje na práci předchozích týmů.
* Testovací scénáře se nesmí vytvářet ze specifikace. Testovací scénáře musí zachycovat skutečný chod aplikace a musí být definovány z praktického využití uživatelem (nejlépe je vytvářet společně s uživatelem).
* Není potřeba velké množství specifikace. Nejlepší je programovat na základě testovacích scénářů.
* Není výhodné aby týmy pracovali odděleně (jak časově tak i fyzicky). Lepší je vytvořit specifikaci a testovací scénáře pro malou část aplikace, pak ji nadesignovat a hned naprogramovat.
* Vytváření dokumentů a jejich předávání podporuje “Blaming culture”. Lidé mají tendenci obviňovat předchozí tým. A ten předchozí má tendence se proti obviňování bránit.

