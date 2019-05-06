# Érettségire való készüléshez
>Végső gyűjtemény az érettségire való készüléshez

## Programozás

Az érettségin **Microsoft Visual Studio** és **NotePad++** használható fejlesztő környezetként.
Mi - dobpergés - **Visual Studio**-t használunk, hisz azon tanultunk.
>Ha bárki valamilyen másik nyelvet szeretne használni, szíve joga, ezen sosem fogunk összeveszni

Válasszuk ki a C++ nyelvet, azon belül pedig a **...Wizzard** opciót.
Szedjük ki a megfelelő pipákat a nem szükséges helyekről, majd hozzuk létre a projektet.
>TODO: Ide egy Kép fog bekerülni

Ekkor egy szinte üres **main függvényt** kell látnunk.
>Ehhez első körben nem kell nyúlnunk

Mivel minden érettségi feladat valamilyen adatfeldolgozásról (valamilyen fájl kiolvasásáról és kilértékeléséről) szól, így eslő feladatunk az, hogy egy megfelelő **osztályt** hozzunk létre.
Ehhez nézzük meg, hogy mit kell tárolnunk:

Példánkban egy futóversenyt fogunk feldolgozni, amiben 3 adat van eltárolva
- Vezetéknév
- Életkor években
- Megtett táv méterben

>Ez csak egy példa, természetesen érettségin bármilyen adatot adhatnak, a lényeg, hogy megfelelően tudjuk őket egy osztály által a kiolvasáskor párosítani

Tudjuk, hogy a nevet szövegként, az életkort és a megtett távot egész számokként tudjuk eltárolni.
Így az osztályunk a következőket fogja tartalmazni:
- string nev
- int kor
- int tav

>A változók neveit érdemes úgy megválasztani, hogy rövidek, de egyértelműek legyenek, tehát ne int a és int b legyen, de azért nem kell túlzásokba sem esni, mint string aversenyenresztvettfutoneve

Ha már tudjuk, hogy mit szeretnénk tárolni, akkor létre is hozhatjuk a két szükséges **konstruktor**unkat:
- Egyet, ami minden szükséges adatot bekér **paraméter**ként, és 
- egyet, amit üresen hagyunk
>TODO: Ide kerül egy kép a végleges osztályról

Mivel a versenyen nem csak egy futó vett részt, sőt, igazából előre nem tudjuk pontosan, hogy hány futónk lesz, így egy olyan tárolóra lesz szükségünk, melyet dinamukusan tudunk növelni.
Erre mi a **vector**t tanultuk.
Legegyszerubb talán úgy elnevezni (mivel az osztályunk neve Futo, hisz egy példánya egy darab futó adatait tartalmazza), mivel futókat fog tartalazni, hogy **futok**.

Ezek után eltárolom a feladatban meghatározott elválaszót/elválasztókat, jelen esetben ez a **TAB** karakter lesz, majd pedig eltárolom a meghatározott fájlnevet. 
>Ezeket minden esetben **const**ként tárolom, nehogy véletlen módositsam a későbbiekben.

Ha ezekkel megvagyok, akkor elkezdhetem feltölteni a vectoromat, vagyis elkezdhetem kiolvasni a megadott fájlból az adatokat.
