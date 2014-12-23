# Možnosti

Nejdříve se podívejme, jaké jsou možnosti pro provedení převodu ze starých do nových technologií. Níže zmíněné možnosti nastiňují základní rozdělení do tří skupin s výpisem jejich základních vlastností. Další způsoby, které zde nejsou zmíněny, by měli být variace níže zmíněných.

##### 1. Automatický převod

* Existuji nástroje, které jsou schopné automaticky převést, například C++ kód do Java kódu.
* Před samotným převodem se musí udělat velké množství konfigurací, aby bylo možné aplikaci uvést do provozu.
* Po automatickém převedení kódu, je většinou potřeba dělat úpravy ve vygenerovaném kódu tak, aby byla aplikace spustitelná.
* Výsledkem je poměrně nepřehledný kód, který je těžko spravovatelný. Obsahuje spoustu míst, o kterých nikdo nic neví a nejsou zdokumentovaná. Změny v takovémto kódu jsou časově a finančně velmi náročné.
* Staré aplikace většinou nevyužívají výhod objektově orientovaného programování.
* Automatický převod se nedá použít ve všech případech.

##### 2. Refactoring

* Zákazník poskytne starou aplikaci ve spustitelném prostředí a zdrojové kódy.
* Dodavatel vytvoří základní specifikaci tím, že se naučí používat starou aplikaci a zrefaktoruje staré zdrojové kódy. Proto, aby se dodavatel naučil používat aplikaci potřebuje pochopit co a jak daná aplikace řeší (tzn. tvůrci specifikace často komunikují se zákazníkem).
* Specifikace většinou není popsána z uživatelského pohledu, je to přepsaný kód do dokumentů a je těžké pochopit, jak uživatel s aplikací pracuje, co nejvíce potřebuje a bude využívat.

##### 3. Řízeno zákazníkem

* Podobá se vývoji nové aplikace.
* Zákazník definuje a prioritizuje, které části aplikace chce mít převedeny. Může se stát, že s něčím, co je ve staré aplikaci není spokojený a požádá o změnu stávajícího řešení.
* Zákazníkovi může přirozeně ovlivňovat průběh vývoje.
