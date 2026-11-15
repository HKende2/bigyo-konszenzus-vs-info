# Célkitűzések - Konszenzus vs. információtartalom

## 1. Projektcél

A projekt célja két motívumkeresési fitneszfüggvény objektív összehasonlítása azonos kísérleti keretben:

- konszenzus-pontszám alapú fitnesz
- információtartalom (information content) alapú fitnesz

A bioinformatikai motiváció transzkripciós faktor kötőhelyek (TFBS) felderítése rövid DNS-szekvenciákban.

## 2. Vizsgálati kérdés

Milyen gyakorisággal és milyen hatékonysággal találja meg a beültetett 8-mer motívumot a két fitneszfüggvény, különös tekintettel A/T-gazdag háttéreloszlásra?

## 3. Kísérleti beállítás rögzített paraméterei

- Minta: 15 szekvencia/futás
- Motívum: beültetett 8-mer
- Ábrázolás: egész vektor
- Variánsok: 2 (konszenzus vs. információtartalom)
- Ismétlésszám: legalább 20 futás variánsonként
- Költségvetés: azonos kiértékelési keret mindkét variánsnál

Kritikus fairness-feltétel: a két variáns minden egyéb komponense megegyezik, kizárólag a fitneszfüggvény térhet el.

## 4. Hipotézisek

- H1: Az információtartalom-alapú fitnesz legalább olyan gyakran találja meg a beültetett motívumot, mint a konszenzus-pontszám.
- H2: A/T-gazdag háttér esetén az információtartalom-alapú fitnesz robusztusabb (jobb találati arány vagy gyorsabb konvergencia).

## 5. Mérőszámok és kiértékelés

A következő mérőszámokat mindkét variánsra külön gyűjteni kell:

- találati arány (a futások hány százalékában azonosítja helyesen a motívumot)
- kiértékelések száma a cél eléréséig (speed-to-target)
- végső legjobb fitnesz / végső minőség
- medián és IQR a fő mérőszámokra

Ajánlott másodlagos mutatók:

- szórás
- kvantilisek (Q1, Q3)
- sikertelen futások aránya

## 6. Kötelező leadandók

- Colab-notebook (.ipynb), amely ugyanabban a vázban tartalmazza mindkét változatot
- boxplot ábrák a fő mutatókra
- mediánokat és IQR-t tartalmazó táblázat
- elvárt-kapott táblázat
- rövid jelentés + 5-8 mondatos értelmezés

## 7. Elfogadási kritériumok

A projekt akkor tekinthető teljesítettnek, ha mindegyik alábbi feltétel egyszerre igaz:

- mindkét algoritmusváltozat implementálva van ugyanazon keretrendszerben
- legalább 20-20 futás történt, azonos költségvetéssel
- az eredmények reprodukálhatók rögzített seed-listával
- szerepel legalább egy boxplot és egy medián/IQR táblázat
- elkészült az elvárt-kapott összevetés
- az értelmezés külön kitér a variancia és a medián jelentésére

## 8. Pontozási megfeleltetés (100 pont)

- Implementáció (mindkét változat): 25 pont
- Összehasonlító kísérlet (>=20 futás/variáns, azonos költségvetés): 25 pont
- Elvárt viselkedés igazolása: 20 pont
- Statisztika és ábrák (medián, IQR, boxplot): 15 pont
- Dokumentáció és értelmezés: 15 pont

## 9. Reprodukálhatósági elvek

- Rögzített seed-lista minden variánshoz ugyanazzal a sorrenddel
- Verziózott függőséglista (requirements.txt)
- Egységes kimeneti struktúra (results/figures, results/tables)
- Paraméterek és futási konfiguráció dokumentálása notebookban

## 10. Kockázatok és csökkentésük

- Kockázat: egyetlen kiugróan jó futás félrevezető.
  - Kezelés: medián + IQR + teljes eloszlás boxploton.
- Kockázat: eltérő induló állapotok torzítják az összehasonlítást.
  - Kezelés: azonos seed-lista és azonos inicializációs szabályok.
- Kockázat: eltérő költségkeret miatt nem fair az összevetés.
  - Kezelés: egységes kiértékelési budget és stopping criterion.

## 11. Minimális munkafolyamat (kódolás előtt)

1. Paraméter- és metrika-séma véglegesítése.
2. Seed-lista rögzítése.
3. Notebook váz és output-struktúra jóváhagyása.
4. Implementáció és futtatás.
5. Statisztikai összegzés, ábrázolás, értelmezés.

## 12. Várt projektkimenet röviden

A végső anyagnak világosan és statisztikailag alátámasztva kell megmutatnia, hogy az információtartalom-alapú fitnesz legalább versenyképes a konszenzus-pontszámmal, és A/T-gazdag háttérben előnyben lehet.
