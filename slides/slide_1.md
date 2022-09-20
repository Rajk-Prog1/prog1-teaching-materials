---
title: Course 1
description: Tudás és Specifikáció
paginate: true
marp: true
theme: uncover
---

# Tudás és Specifikáció

---

## Kurzus Menete

1. Tudás és Specifikáció I.
2. Specifikáció II., Alapfogalmak
3. Lokális/Globális, Strukturális programozás
4. Függvények, Számítógép architektúra
5. Algoritmusok intro, Git, Github
6. Csoportmunka
7. Bonyolultság analízis, Algoritmusok +
8. Class, Package
**Kurzushétvége**
---

## Kurzus Menete

9. Turing-gép, Dokumentáció
10. Internet architektúra, Scrape
11. Adat tárolása, adatbázisok, Pandas
12. Vizualizáció és Automatizáció intro, Kvantumszámítógép

---

## Kurzus célja

- Megfogalmazni egy programozási problémát
- Számításelmélet értelmét elmagyarázni
- Lebontani egy komplex problémát egyszerűbbekre
- Megérteni egy leírt programot
- Megírni egy programot
- Találni érdeklődést és folytatást

---

## Tudás Típusai

---

## Tudás Típusai

| Dekleratív Tudás | Imperatív Tudás |
| ----------- | ----------- |
| A "mit?" kérdésre adott válasz egy probléma kapcsán | A "hogyan" kérdésre adott válasz egy probléma kapcsán |
| tervrajz, térképjelzés, anatómiai ábra ...| recept, IKEA útmutató, útvonalterv|

---

## Mit adunk át a gépnek?

Egy probléma megoldására szeretnénk megtanítani/megkérni:

Tetszőleges x-re, számolja ki $\sqrt x$ úgy, hogy csak osztani, szorozni, meg összeadni tud.

---

| Ember | Gép |
| ----------- | ----------- |
| okos, kreatív, tud következtetni, memóriája ködös, szeretné minél kevesebbet nyomkodni a számológépet | buta, nincs önálló gondolata, memóriája tökéletes másodpercenként töbmilliárd műveletet el tud végezni |

---

## Ember

- felhasznál csomó meglévő deklaratív tudást

- összeállítja egy komplex tippelési folyamattá

- tippek eredményéből továbbfejleszti a folyamatot

- felhasznál olyan komplex fogalmakat mint nagyságrend, vagy előjelváltás

---

## Gép

- tippel egy nagyon rosszat, pl G = 1

- valaki megtanította neki hogy G′=$\frac{G + \frac{x}{G}}{2}$ közelít, szóval elkezdi


- Megoldandó probléma: $\sqrt1366561$=?

- 1, 683281, 341641, 170822, 85415, 42715, 21373, 10718, 5423, 2837, 1659, 1241, 1171, **1169**

---
## Specifikáció
Egyfajta deklaratív leírása egy programnak

**Miből, mit?**

- **állapottér** - bemenő/kimenő adatok
- **előfeltétel** - amit tudunk a bemenetről
- **utófeltétel** - az eredmény kiszámítási szabálya (amit tudunk az eredményről)

legyen **teljes** és **részletes**

---

## Példa

Valós számok halmazán megoldható másodfokú egyneletet oldjon meg a program, ami $ax^2+bx+c=0$ formában van megadva

- Á: ?
- Ef: ?
- Uf: ?

---

Valós számok halmazán megoldható másodfokú egyneletet oldjon meg a program, ami $ax^2+bx+c=0$ formában van megadva

- Á: $(a,b,c,x_{1},x_{2} \in \R)$
- Ef: ?
- Uf: ?

---

Valós számok halmazán megoldható másodfokú egyneletet oldjon meg a program, ami $ax^2+bx+c=0$ formában van megadva

- Á: $(a,b,c,x_{1},x_{2} \in \R)$
- Ef: $(a≠0∧b^2−4ac≥0)$
- Uf: ?

---

Valós számok halmazán megoldható másodfokú egyneletet oldjon meg a program, ami $ax^2+bx+c=0$ formában van megadva

- Á: $(a,b,c,x_{1},x_{2} \in \R)$
- Ef: $(a≠0∧b^2−4ac≥0)$
- Uf:  $(x_{1}= \frac {−b+\sqrt{b^2−4ac}}{{2a}} ∧ x_{2}= \frac {−b-\sqrt{b^2−4ac}}{{2a}})$

---

## Alternatív megoldás

Valós számok halmazán megoldható másodfokú egyneletet oldjon meg a program, ami $ax^2+bx+c=0$ formában van megadva

- Á: $(a,b,c,x_{1},x_{2} \in \R)$
- Ef: $(a≠0∧b^2−4ac≥0)$
- Uf: $(∀i(ax^2_{i}+bx_{i}+c=0)∧(x_{1}=x_{2}⟺b^2−4ac=0))$

---

## Teljesség

Amit az előfeltétel megenged az állapottéren belül, azt az utófeltételnek kezelnie kell

Pl: Válassza ki két szám közül azt amelyiknek több prím osztója van
több különböző vagy több összesen?
mi van ha ugyanannyi?
Válassza ki egy számsorból azt az 5 számot ami legjobban eltér az átlagtól
mi van ha nincs 5 szám a számsorban?
mi van ha minden szám ugyanaz?

---

## Részletesség

A program főzzön rántottát:

Á: (konyha)
Ef: ( )
Uf: (ha a konyha alkalmas ennek elkészítésére, a konyhában legyen egy finom rántotta)

vagy:

Á: (serpenyő, főzőlap, 3 tojás, olaj, só, fakanál, tányér)
Ef: (a serpenyő, tányér és fakanál tiszta ...)
Uf: (a tojások összekeverve kerültek a 200 fokos serpenyőbe ...)

---

## Példa 2.

Két természetes szám legnagyobb közös osztójának megtalálása

Á: ?
Ef: ?
Uf: ?

---

## Példa 2.

Két természetes szám legnagyobb közös osztójának megtalálása

Á: $(a,b,x \in \N)$
Ef: ?
Uf: ?

---

## Példa 2.

Két természetes szám legnagyobb közös osztójának megtalálása

Á: $(a,b,x \in \N)$
Ef: $(a≠0∧b≠0)$
Uf: ?

---

## Példa 2.

Két természetes szám legnagyobb közös osztójának megtalálása

Á: $(a,b,x \in \N)$
Ef: $(a≠0∧b≠0)$
Uf: $(x|a∧x|b∧ \nexists i(i|a∧i|b∧i>x))$
