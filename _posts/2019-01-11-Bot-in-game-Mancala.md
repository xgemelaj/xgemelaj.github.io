---
layout: post
subject: "Application Programming in C++"
title: "Bot in the game Mancala"
picture_path: /images/mancala.jpg
description: "Create a bot that will be able to play Mancala effectively."
date: 2019-01-11
---

### Zadanie

Úloha je za 12+2 bodov.

Vašou úlohou bude naprogramovať bota, ktorý bude vedieť hrať hru Mancala. Samotnú hru si môžete naštudovať a vyskúšať napríklad na stránke http://play-mancala.com/. Pravidlá sú napríklad na stránke https://www.thesprucecrafts.com/how-to-play-mancala-409424 v sekcii "How to play". Je tam jedna taká nejasnosť a to, že kedy hra končí. Budeme to brať tak, že ak je nejaký hráč na ťahu a nemôže urobiť ťah (teda má prázdne pole), tak hra končí a oponent si nechá všetky "guľôčky", ktoré mu ostali na jeho ploche. Od pravidiel sa ešte odchýlime tak, že na úvod nebudú v jamkách 4 gulôčky, ale 8. Zo štyrmi je totiž hra príliš ľahká. 

Protokol je taký, že vám vždy na začiatku príde START, potom 0..n krát MOVE a nakoniec STOP, ak toto tak nebude, tak treba vypísať chybu a skončiť (tentokrát už skôr nie abort (wink)). Chyby a vlastne čokoľvek iné nevypisujte na štandardný výstup (cout), keďže ten je šúčasťou protokolu, ale napríklad na štandadtný chybový výstup (cerr, resp. clog).

Ako to naprogramujete je na vás, asi budete potrebovať niečo ako move generator a potom min max search (tu pozor, lebo hráči sa nutne nestriedajú po jednom ťahu). Mám naprogramovaného hráča, ktorý hra podľa funkcie rand(), keď toho porazíte, tak máte 6 bodov istých. Ďalších 6 je ako vždy za to, aby ste tam nemali nedefinované správanie, neinicializované premenné, priveľa kopírovania, pekne nazvané premenné a funkcie, atď.

Ešte pár slov k časovému limitu. Testovacia aplikácie vám dá ešte plus mínus trochu času aby ste stihli odpovedať, teda stačí ak po časovom limite zastavíte výpočet a odpoviete. V zásade sú dve možnosti ako to spraviť.

* Každú chvíľu sa spýtate na aktuálny time() a ak už treba končiť tak return. Pýtať sa ale každú chvíľu na čas nevyzerá moc pekne.
* Spustíte si jeden thread, ktorý necháte čakať daný čas (v podstate aj sleep by sa dal na toto dobre použiť, lepšie ale použiť CV), ten neskôr nastaví bool (pozor, ten musí byť atomic). Ostatné thready si budú kontrolovať tento bool.


### Zhodnotenie

Náš **bot** úspešne porazil expertného bota na testovacej stránke. Na jeho zkonštruovanie sme využili **MIN-MAX algoritmus**.  V turnaji medzi botmi vytvorenými z predmetu obsadil solídne umiestnenie.