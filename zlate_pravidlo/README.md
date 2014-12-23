# Zlaté pravidlo

Jednou z prvních otázek, kterou jsem potřeboval mít zodpovězenou po zapojení se do projektu bylo - "Proč se aplikace převádí pouze do jedné technologie (tedy Javy)? Proč se musí zanechat i další technologie, která není s Javou kompatibilní (v tomto případě VisualBasic)? S jedinou platformou by měl být vývoj přece rychlejší".

Odpovědí a zdůvodnění bylo několik:

1. Zákazník chce, aby aplikace měly stejný vzhled a chování. Také nechce přeškolovat své zaměstnance kvůli novinkám, které by vznikly při použití jiné technologie pro uživatelské rozhraní.
2. Existuje pravidlo, které říká, že při technologickém převodu softwaru se má vyměnit pouze jedna technologie. Jinými slovy, technologie se mají nahrazovat jedna za druhou - ale nikdy ne všechny zároveň.

Všichni víme a určitě jsme získali i zkušenost, že neexistují bezchybné aplikace. Co více, neexistují ani bezchybné platformy, na kterých naše aplikace běží. Zkusme se například podívat na to, kolik bylo vydáno verzí Javy 6. Bylo jich 31. Každá nová verze obsahovala průměrně kolem sedmi opravených chyb. Což znamená, že bylo nalezeno a opraveno něco přes 217 chyb.

Při nalezení chyby v platformě, kterou používáte nelze okamžitě platformu aktualizovat verzí, kde byla chyba vyřešena. Mohli bysme tím rozbít již existující kód. Abychom zajistili dobrou stabilitu a kvalitu aplikace, tak bychom měli celou aplikaci přetestovat.

V našem projektu jsme bohužel používali dvě platformy a to Java a VisualBasic. Tím se počet chyb a s nimi spojených komplikací zvýšil.
Bohužel se situace s platformami ještě více komplikovala. Musela se totiž zajistit spolupráce mezi Javou a VisualBasicem. Čímž vzniknul “podomácku” vytvořený framework, který poskytoval propojení mezi uživatelským rozhraním napsaným ve VisualBasic a logikou aplikace napsanou v jazyce Java.

S tvorbou tohoto frameworku nikdo v původních odhadech na náklady projektu nepočítal. Proto se tento framework dělal za interní náklady a nebyla mu věnována důležitost, jakou by zasloužil. Možná i to byl důvod, proč nebyly všechny funkčnosti frameworku důkladně otestovány a během vývoje aplikací programátoři nevěděli jestli jde o chybu způsobenou jejich zaviněním, vinou frameworku, nebo jestli je to snad nějaká chyba ve VisualBasicu nebo Javě.

Tímto “podomácku” vytvořeným frameworkem se docílilo:
* Nemožnost jednoduše debugovat a dohledat se chyb.
Komplikovaná konfigurace a složitý nasazovací proces.
Zkomplikovala se možnost automatického a jednotkového testování.
* Musela se řešit podivná chybová hlášení z VisualBasic (error 13, apod.).
* Implementace některých uživatelských akcí nebyla možná (např. změna kurzoru na specifické textové pole). Taková řešení vyžadovala opravy chyb nebo změny v frameworku. Nejčastějším řešením bylo přijít na dočasné obejítí chyby (workaround), který by problém nějak vyřešil.
* Zvýšení nákladů pro naši společnost.
* Po několika málo měsících se ukázalo, že díky tomuto pravidlu o převodu pouze jediné technologie všichni více trpíme, než máme užitek.

A co na to zákazník? Projekty byly ve časovém zpoždění a zákazník spokojený nebyl. Upřímě si myslím, že z převodu jedné technologie nějakou zvláštní radost neměl. Pokud vůbec něco takového zaregistroval.

#### Co jsme se z toho naučili

* Nenásledovat slepě pravidla, které se k nám dostali. Vždy to chce zamyšlení nad tím, co aplikace daného pravidla bude znamenat pro konkrétní projekt.
* Akceptovat, že nelze předpovědět všechny důsledky.
* Pokud vidíme nějaké nedostatky, je potřeba spočítat, jaká je předpokládaná finanční ztráta a poté se pokusit o schválení změny (jinak nemá smysl snažit se o prosazení jiného řešení).
* Pokud jsme se špatně rozhodli, můžeme to jednoduše přiznat a změnit co je potřeba, abychom zajistili hladký chod projektu. Ušetříme tak peníze a energii sobě i našemu zákazníkovi.
* Při konverzi je dobré zvážit, zda by bylo lepší předělat větší část aplikace a tím nahradit více starých technologií za nové. Pamatujte, že postupem času vznikají lepší a jednodušeji použitelná technologická řešení.
