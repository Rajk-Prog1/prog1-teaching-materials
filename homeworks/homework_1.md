
Ebben a háziban programok leírását és ezekhez tartozó specifikációkat találtok. 

A házi ezeket összepárosítani. Lehet, hogy van aminek nincsen párja.

Ezen kívül előfordulhat hogy valamelyik specifikációban van valami hiba, valami nem teljes. Ha ilyet találtok, jelezzétek és írjátok le részletesen miért gondoljátok hogy baj van a specifikációval. 

Ennek a leadási határideje is **kedd kurzus kezdete**.

## Jelölés beli segítség:

- $\mathbb{B}$ a logikai értékek halmaza.
  - $l \in \mathbb{B}$ azt jelenti hogy $l$ egy logikai változó
  - $P: \mathbb{R} \to \mathbb{B}$ pedig azt, hogy $P$ egy valós számból logikai értékbe képző függvény (más néven predikátum)
- $\mathbb{N}^n$ az $n$ elemű tömböket jelöli amikben $\mathbb{N}$ típusú elemek vannak
  - $v \in \mathbb{N}^n$ azt jelenti, hogy $v$ egy $n$ elemszámú tömb és mindegyik elem természetes szám, amiket lehet $(v_1,v_2 ... v_n)$-el jelölni
  - Ha az előző módon kikötöttük micsoda $v$, használhatjuk az $x \in v$ jelölést arra, hogy $v$ egyik eleme $x$ (ez ugye nem alap, mivel $\in$ egy halmazművelet és $v$ nem egy halmaz hanem tömb, de most megengedjük)
- $a = a'$ ami jellemzően az előfeltételben szerepel, annyit jelent, hogy a egy konkrét értékkel rendelkezik a program futása elején

## Specifikációk

### 1.
#### A: $(v \in \mathbb{N}^n, a,b  \in \mathbb{N})$
#### Ef:   $(v=v' \land n \geq 2)$
#### Uf: $(Ef \land \exists c,d(c,d \in v \land (\nexists k ( k \in \mathbb{N} \land k \neq 1 \land \frac{c}{k} \in \mathbb{N} \land \frac{d}{k} \in \mathbb{N} )) \Rightarrow a,b \in v \land (\nexists k ( k \in \mathbb{N} \land k \neq 1 \land \frac{a}{k} \in \mathbb{N} \land \frac{b}{k} \in \mathbb{N} )$

### 2. 
#### A: $(a,b,c \in \mathbb{R}, l \in \mathbb{B})$
#### Ef: $(a=a' \land b=b'\land c=c' \land a > 0 \land b > 0 \land c > 0 \land c < a + b \land a < b + c \land b < a + c)$
#### Uf: $(Ef \land l   \Leftrightarrow (a^2 + b^2 = c^2 \lor a^2 + c^2 = b^2 \lor b^2 + c^2 = a ^2) )$

### 3.
#### A: $(t \in \mathbb{N}^n , x \in \mathbb{N})$
#### Ef: $(x=x')$
#### Uf: $(Ef \land (x / t_i \in \mathbb{N} \land t_i \in \mathbb{N}) \Leftrightarrow (t_i \in t))$

### 4.
#### A: $(a,b,x \in \mathbb{N})$
#### Ef: $(a=a',b=b')$
#### Uf: $(Ef \land x/a \in \mathbb{N} \land \frac{x}{b} \in \mathbb{N} \land \nexists y ( y < x \land y/a \in \mathbb{N} \land y/b \in \mathbb{N} )$

### 5.
#### A: $(t \in \mathbb{N}^n , x,y \in \mathbb{N})$
#### Ef: $(x=x' \land y=y')$
#### Uf: $(Ef \land (t_i \in t) \Leftrightarrow (\forall m (m \in \mathbb{N} \land t_i / m \in \mathbb{N} \Rightarrow (m = 1 \lor m = t_i) ) \land t_i \geq x \land t_i \leq y) )$

### 6.
#### A: $(a \in \mathbb{N}^+, b \in \mathbb{N})$
#### Ef: $(a=a' \land a \geq 3)$
#### Uf: $(Ef \land b = \frac{a (a-3)}{2} )$

### 7.
#### A: $(v \in \mathbb{N}^n, b \in \mathbb{N})$
#### Ef: $(v=v' \land n = 10)$
#### Uf: $(Ef \land \exists p (p \in v \land 2 \mid p) \Rightarrow (b = \prod_{t \in v} t ) \land \nexists p (p \in v \land 2 \mid p) \Rightarrow (b \in v \land \nexists k (k \in v \land k < b))  )$

### 8.
#### A: $(v \in \mathbb{R}^{n}, x \in \mathbb{R})$
#### Ef: $(v=v')$
#### Uf: $(Ef \land x \in v \land \nexists y(y \in v \land y > x))$

### 9.
#### A: $(a,b,c \in \mathbb{R}^+)$
#### Ef: $(a=a', b=b')$
#### Uf: $(Ef \land a^2+b^2 = c^2 )$

## Leírások

### A 
Válassza ki a megadott számok közül a legnagyobbat   

### B 
találjuk meg az összes prím számot két adott természetes szám között

### C 
Egy természetes számokat tartalmazó halmazból válasszunk ki két relatív prímet (ha van)!

### D 
Adott három szám ami egy háromszög 3 oldalának hossza. Döntsük el, hogy derékszögű-e a háromszög

### E 
Egy tíz számból álló tömbben ha van páros, számoljuk ki a 10 szám szorzatát, ha nincs közte páros szám, adjuk meg a legkisebb számot

### F 
Találjuk meg két természetes szám legkisebb közös többszörösét

### G 
Számoljunk ki egy tömböt amiben szerepel egy adott szám minden egész osztója

### H 
Adott egy tömb, amihez számoljunk ki egy olyan tömböt amiben az eredeti tömbben szereplő négyzetszámok gyöke szerepel, a nem négyzetszámok pedig önmaguk

### I 
Állapítsd meg hogy "a" oldalszámú sokszögnek hány darab átlója van!