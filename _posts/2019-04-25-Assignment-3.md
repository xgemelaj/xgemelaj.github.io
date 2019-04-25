---
layout: post
subject: "Web Publishing"
title: "XML prezentácia"
picture_path: /images/question-mark.png
description: "Vytvorenie XML prezentácie a transformácia do HTML a PDF."
date: 2019-04-25
---

## Zadanie 

Analyzujte možnosti zápisu jednoduchej prezentácie v jazyku XML. Identifikujte základné súčasti prezentácie a navrhnite XML elementy pre ich označkovanie (metadátové, štrukturálne, inline). Dbajte na znovupoužiteľnosť a vyvarujte sa redundancií. Návrh elementov zrealizujte opísaním typu dokumentu pomocou vybraného jazyka (DTD, XSD, RELAX NG) spolu s vysvetlením účelu jednotlivých elementov. Vo vami navhrnutom jazyku vytvorte ukážkovú prezentáciu, ktorá bude demonštrovať možnosti tvorby prezentácií podľa definície typu dokumentu.

Navrhnite a vytvorte XSLT šablóny pre konverziu prezentácie z XML do XHTML+CSS a pre konverziu prezentácie z XML do PDF. Klaďte dôraz na znovupoužitie jednotlivých šablon pre viaceré výstupné formáty. Umožnite zadávanie parametrov transformácií.

Súčasťou požiadaviek na zadanie je vytvorenie správy o zadaní 3, v ktorej zdokumentujete splenie jednotlivých bodov zadania. Správa bude súčasťou vašej stránky o Webovom publikovaní na GitHube.

## Dokumentácia

V dokumnetácii si postupne prejdeme všetkými povinnými bodmi ktoré sa v dokumente majú nachádzať.

##### Opis typu dokumentu + opis účelu navrhnutých elementov - možnosť výberu (práve jedného) z variantov

Vybrali sme si variantu DTD ktorú sme skontrolovali a je validná pre nami vytvorený XML dokument. Nachádza sa v súbore presentation.xml.

##### Vytvorenie ukážkovej XML prezentácie demonštrujúcej možnosti definície typu dokumentu

Vytvorili sme prezentáciu ktorá sa nachádza v súbore presentation.xml. Táto prezentácia má 6 slidov a demonštrovali sme na nej všetky základne funckie a možnosti bežných nástrojov na tvorbu prezentácií čo sa týka nadpisov, textu, listov a obrázkov. Je pripravená pre rôzne zmeny ktoré sme pri tvorbe považovali ako dôležité pri tvorbe prezentácií.

##### Základný návrh XSL transformácií, ich vhodnosť, parametrizácia

Použili sme to ako číslovanie či už v pdf formate ale aj v html pomocou XSL transformácií. Myslím si že vhodnosť využitia je veľká pretože inak by sa to msuelo riešiť ručním dopĺňaním čo sa v normálnych nástrojoch na tvorbu prezentácií takto nerobí.

##### Vytvorenie XSLT pre konverziu prezentácie z XML -> XHTML+CSS

V priečinku presentation sa nachádza vygenerovana prezentácia vo formáte HTML spolu s CSS. Každý jeden slide sa nachádza v samostatnom súbore ako bolo požadované v zadaní.

##### Vytvorenie XSLT pre konverziu prezentácie XML -> PDF

Súbor output.pdf predstavuje výslednú vygenerovanú prezentáciu vo formáte pdf ktorú sme transformovali zo súboru presentation.xml.