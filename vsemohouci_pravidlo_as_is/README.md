# Pravidlo "as is"

Toto pravidlo bylo domluveno se zákazníkem jako první. Co znamená pravidlo "as is"?

Jak jsem zmiňoval v předchozí kapitole: zákazník nechce investovat do přeškolení zaměstnanců a tudíž vše v nové aplikaci musí vypadat a chovat se stejně jako ve staré aplikaci.

Jen si to představte, z hlediska zákazníka se jedná o velmi jednoduchý princip. Proč by dodavatel neměl být schopný jednoduše převést starou aplikaci do nové technologie?

Dodavatel má k dispozici starou funkční aplikaci, z které můžeme zjistit veškeré chování a funkce, které aplikace poskytuje koncovým uživatelům. K této aplikaci se navíc manuálním refactoringem starého kódu vytvořila dokumentace!

Vypadá to tak jednoduše a krásně. Nicméně zde uvedu zde několik úskalí, na které jsme postupem času přišli:

* Tímto přístupem se zkopírují do nové aplikace chyby ze staré aplikace.
* Nepoužívané části jsou implementovány do nové aplikace. A zákazník platí za něco, co nebude využívat.
* Není dostatek prostoru pro kreativitu a vlastní invenci (což jsou skvělé a největší motivátory pro realizační tým). To působí negativně na stabilitu týmu. Tímto se zvyšují náklady kvůli úbytku členů týmu a zaškolování nových členů.
* Díky tomuto přístupu se omezí komunikace se zákazníkem. Nedostatek této komunikace vygeneruje mnoho překvapení (v podobě velké chybovosti) při závěrečném akceptačním testovaní.

#### Co jsme se z toho naučili

* Nepřistupovat na pravidlo “as is”
* Udělat prototyp nové aplikace, promluvit si s zákazníkem a získat jeho názor na novou aplikaci.
* Je klíčové periodicky diskutovat se zákazníkem a vysvětlit, proč je potřeba prioritizovat to, které funkce jsou nejdůležitější a mají se naprogramovat první.
* Během vývoje se pokoušet zjistit, jestli zákazník opravdu potřebuje všechny funkce ze staré aplikace.
* Také je klíčové zapojit do vývoje i koncové uživatele daného software. V našem projektu to byli bankovní úředníky (tzn, nekomunikovat pouze s managementem zákazníka).
* Refaktoring kódu je vhodný pouze pro algoritmy. Nikdy ne pro tvorbu uživatelských scénářů.
