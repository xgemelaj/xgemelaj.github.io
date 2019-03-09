---
layout: post
subject: "Database systems"
title: "Transfermarket"
picture_path: /images/transfermarket.jpg
description: "In Java, create a database application in the selected domain."
date: 2018-04-28
---

### Zadanie
Vo vami zvolenom prostredí vytvorte databázovú aplikáciu, ktorá komplexne rieši päť vami zadefinovaných scenárov (prípadov použitia) vo vami zvolenej doméne tak, aby ste demonštrovali využitie relačnej databázy podľa pokynov uvedených nižšie. Presný rozsah a konkretizáciu scenárov si dohodnete s Vašim cvičiacim na cvičení. Projekt sa rieši vo dvojiciach, pričom sa očakáva, že na synchronizáciu práce so spolužiakom / spolužiačkou použijete git.

### Scenáre

#### SCENÁR 1 - Prestup hráča do iného tímu

**Situácia**: Hráč prestúpi do iného tímu a je potrebné nahrať prestup a tým upraviť informácie v aplikácií.

**Opis**: Po prestupe hráča do iného tímu je nutné pre aktualizáciu nahrať do tabuľky historia prestupov nový prestup. Kde uvádzame aký hráč prestúpil do akého tímu, za akú cenu a dátum uskutočnenia prestupu. Pomocou týchto informácií sa následne upravia uvádzané informácie v aplikácií.

#### SCENÁR 2 - Výhra trofeje tímu

**Situácia**: Tím vyhrá nejakú súťaž, za ktorú dostane trofej, ktorých zisk chceme evidovať v našej aplikácií.

**Opis**: Po odohraní finálneho zápasu sa do tabuľky trofejí musia nahodiť údaje  o tom akú trofej vyhral aký tím a v aký dátum čo nám bude slúžiť na určenie na sezónu. Následne budú tieto informácie slúžiť v aplikácii na detailne informácie či už o hráčovi alebo o tíme, ktoré jednotlivé trofeje vyhral v akej sezóne.

#### SCENÁR 3 - Zmena tržnej ceny hráča

**Situácia**: Tržná hodnota hráča sa zmenila a je potrebné ju aktualizovať v tabuľke aby aplikácia bola aktuálna.

**Opis**: V tabuľke tržných hodnôt hráčov budeme mať históriu všetkých zmien tržných hodnôt hráčov. Ak sa tržná hodnota hráča zmení tento údaj sa zapíše do tejto tabuľky s dátumom zmeny. Tieto údaje budeme využívať na poskytnutie lepších údajov v aplikácií -konkrétne graf vývoju tržnej hodnoty hráča.

#### SCENÁR 4  - Pridanie štatistiky za posledný zápas.

**Situácia**: Zápas bol ukončený a je potrebné zaevidovať jednotlivé štatistiky.

**Opis**: V systéme si udržiavame tabuľku štatistík jednotlivých hráčov, pričom pre každý zápas má hráč osobitný záznam. To znamená, že po ukončení zápasu sa štatistiky, ktoré boli zaznamenané zaevidujú do (databázy) tabuľky štatistík. Naša tabuľka štatistík obsahuje bežné typy štatistických zápisov, ako napríklad dátum odohratého zápasu (match_date), góly (goals) atď.

#### SCENÁR 5 - Podpis nového kontraktu s trénerom.

**Situácia**: Tréner podpísal kontrakt s novým tímom alebo predĺžil kontrakt s aktuálnym zamestnávateľom.

**Opis**: Na uchovávaní informácií o pôsobení jednotlivých trénerov v kluboch bude slúžiť tabuľka - história kontraktov, kde si budeme uchovávať záznamy o jednotlivých pôsobeniach hráčov. Pri uzavrení novej zmluvy alebo po obnovení zmluvy sa do tabuľky pridá nový záznam, v ktorom bude aký tréner uzatvára zmluvu s akým tímom, jeho plat a dátum kedy túto zmluvu uzavrel.

#### SCENÁR 6 - Vyhľadávanie jednotlivých hráčov pomocou zadaných kritérií

**Situácie**: 
* Oceňovanie najlepších hráčov - Zlatá lopta, Zlatá kopačka, atď. 
* Nákup nových hráčov - napríklad získanie hráča s najlepšími štatistikami, avšak za prijateľnú cenu

**Opis**: Takýto scenár je určený pre rôzne typy udalostí. V prípade, že sa konajú každoročné oceňovania najlepších hráčov, strelcov alebo brankárov je potrebné takéhoto hráča nájsť. Náš systém preto umožňuje veľmi jednoducho nájsť hráča so špecifickými požiadavkami - najväčší počet gólov, prihrávok, dobrých prihrávok atď. 
Pri nákupe hráčov zase záleží na tom aby bol priaznivý pomer dobrých štatistík a ceny. Ak sa teda rozhodne niektorý tím investovať do hráča, musí dobre zvážiť aktuálnu trhovú cenu hráča a podľa nej sa riadiť

