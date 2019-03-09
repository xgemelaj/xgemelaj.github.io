---
layout: post
subject: "Web Publishing"
title: "Assignment 1"
picture_path: /images/page.jpg
description: "Create a personal page using GiHub pages, Jekyll and Markdown."
date: 2019-03-08
---

# Zadanie

Vytvorte webovú prezentáciu (webové sídlo) o sebe. Zamerajte sa jednak na vaše profesné záujmy (napr. projekty, ktoré riešite/riešili ste, čo vás v informatike najviac baví, fascinuje = váš developerský profil) a jednak vaše osobné záujmy, hobby.

V rámci developerského profilu vytvorte sekciu Webové publikovanie, kde budete publikovať všetky tri vaše vypracované zadania z predmetu.

Využite pritom technológie Git + GitHub Pages + Jekyll + Markdown. Využite potenciál statického generátora Jekyll a jeho templatovacích možností.

Výsledok zadania vložte do AISu do 10. 3. 23:59 ako jeden ZIP archív pomenovaný vaším AIS loginom (Z1-aislogin.zip), ktorý získate ako export projektu z GitHub-u. Okrem toho bude archív obsahovať najviac dva súbory navyše: github.url, kde bude url vášho projektu na GitHub-e, a prípadný readme.txt s pokynmi pre rozbehanie vášho webového sídla (môže obsahovať napr. aj informáciu o podporovanom prehliadači).

# Dokumentácia

### Sídlo je rozdelené do 5 podstránok

1. **Home page** - uvítacia stránka kde sa nachádza moja fotka s uvitácou vetou a zároveň veta s odkazom na viac informácii omne.
2. **About me** - stránka kde sa nachádza viac informácii omne. Sú tam obrázkami zobrazené moje hobby (kolekcia v priečinku *_hobbies*) a zároveň pomocou *pluginu* pridané youtube video na aktuálne najobľubenejšiu hudbu keďže je to moja záľuba.
3. **Skills** - táto podstránka je zameraná na moje skúsenosti a zrućnosti. Vo vrchnej časti sú súbežne zobrazené pracovné skúsenosti a vzdelanie. Zdroje k týmto zobrazeniam sa nachádzajú v kolekcii *_skills* a sú následne *filtrovane* pre jednotlive zobrazenie. V spodnej časti sa zároveň nachádzajú moje informatické zručnosti. Tie sa zobrazujú pomocou tabuľky ktorá sa dá priamo na stránke *filtrovať* návštevníkom. Je možné zobrazovať len zrućnosti v ktorých som pokročilý alebo len zrućnosti v ktorých som začiatočník.
4. **Projects** - táto podstránka nevyužíva *default* layout ale jeho nadstavbu a to layout *project*. V tejto stránke sú zobrazené všetky väčšie školské projekty na ktorých som sa podieľal. Ku každému je ilustračná fotka a krátky opis. K detailnejším informáciam je možné jednotlivé projekty cez ich názov rozkliknúť a tak zobraziť ich detail.
	* **Detail of Project** - pomocou layoutu *post* zobrazí *Markdown* súbor kde sa nachádzajú informácie o jednotlivom projekte.
5. **Web publishing** - je podstránka kde sú *vyfiltrovane* projekty ktoré sa týkajú len predmetu Webove publikovanie. Rovnako ako pri predchádzajúcej podstránke je spolu s názvom projektu zobrazená aj ilustračná fotka, dátum vytvorenia a krátky opis.

### Layouty

1. **default** - nachádza sa vňom forma ktorá bude zobrazená v každej ćasti našej stránky. Preto sú tam navigačná lišta a zároveň pätička stránky.
2. **post** - tento *layout* sa využíva pri zobrazovaní detailov jednotlivých projektov.
3. **project** - tento *layout* sa využíva v podstránkach *Projects* a *Web publishing* keďže v oboch sa zobrazujú projekty akurát s iným obmedzením. Keďže pre zobrazene sme použili rovnaký dizajn, bolo vhodné vytvoriť pre tieto dve podstránky layout. V layoute sa najprv v *jumbotrone* zobrazia informácie ktoré sú uložené v premenách týchto podstránok a následne sa zobrazí obsah stránky samotnej.

### Premenné
* Premenné sme využili na viacerích miestach :
	* V kolekcii záľub (*_hobbies*) - každá záľuba má *dve* premenné ktoré sa využívaju pri ich zobrazovaní v podstránke *About me*
	* V kolekcii zrućností (*_skills*) - kde IT zručnosti majú *tri* premenné a údaje o vzdelaní a pracovných skúsenostiach majú *šesť* premenných, tieto premenné sa pouźívajú pre *filtrovanie* a zároveň ako informácie pri zobrazovaní v podstránke *Skills*
	* V kolekcii príspevkov o projektoch (*_posts*) - v tejto kolekcii má každý záznam premenných ktoré sa využívaju na *filtrovanie* a na dópĺňanie informácií o jednotlivýc projektoch pri ich výpisoch
	* V podstránkach *Projects* a *Web publishing* - využíva sa premenné na výpis prostredníctvom layoutu *project*

### Kolekcie
* V našej stránke vyuźívame tri kolekcie:
	* *_hobbies* - v tejto kolekcie si uchovávame všetky naše záľuby a informácie o nich ktoré následne vypisujeme cyklom cez celú kolekciu v podstránke *About me*
	* *_posts* - kolekcia *_posts* slúži na ukladanie všetkých záznamov o mnou vypracovaných projektoch. Tieto projekty následne všetky vypisujeme cyklom v podstránke *Projects* a zároveň v podstránke *Web publishing* vypisujeme *vyfiltrovane* projekty ktoré sa týkajú projektu Webove publikovanie
	* *_skills* - v tejto kolekcii si uchovávame všetky naše dosiahnuté zručnosti ktoré sa týkajú informatiky, vzdelania ale aj pracóvné skúsenosti. Táto kolekcia sa využíva v podstránke *Skills* kde je viackrát *filtrovana* a nasledne sa vypisuju informácie ktoré su uložené v premenných k jednotlivým zručnostiam

### Filtre 
* Filtre sme využili na nasledujúcich miestach:
	* Podstránka *Skills* -
		* Filtrovanie zručností so zameraním vzdelania
		* Filtrovanie pracovných zručností 
		* Filtrovanie informatických zručností so začiatočníckymi znalosťami (tento filter si uživateľ určuje sám a je možné ho zmeniť klikom na ďalšiu možnosť)
		* Filtrovanie informatických zručností s pokročilými znalosťami
	* Podstránka *Web publishing* -
		* Filtrovanie projektov ktoré sa týkajú predmetu Webové publikovanie

### Plugin
* V tejto stránke sme využili plugin na zobrazovanie *Youtube* videí:
	* Konkrétne v podstránke *About me* kde sa zobrazuje pri mojich záľubách zobrazuje vtipné video ktoré dopĺňa infromáciu o tom že som programátor.
	* Tento plugin by mal rovnako veľké využitie ak by som ako osoba mal nejaké video ohľadom svojej osoby. Vtedy by sa dal veľmi dobre zakomponovať do sekcie či už úvodnej stránky alebo informácii o mne.

* Inštalácia pluginu - jediné čo je potrebné je zadať do konzoly: *gem install jekyll-youtube*