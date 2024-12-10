# Izveštaj o Statičkoj Analizi Koda

## LOC
Ukupan broj linija koda: 148
Broj linija koda u fajlu Calculator: 129
Broj linija koda u fajlu Start: 19

## Statička Analiza Koda

### Fajl: Calculator.java
- Linija 6: Upotrebljena globalna promenljiva finalResult, bolja praksa je koristiti povratne vrednosti metoda.
- Linija 15: Bespotrebna privatna konstrukcija Operations klase, ukoliko je namera sprečiti instanciranje, to bi bilo poželjno navesti u dokumentaciji.
- Linija 24: Metoda Run bi trebala da glasi runExpression radi konvencije o imenovanju.
- Linija 32-35: Potrebno je dodati validaciju za prazan niz kako ne bi došlo do exception-a.
- Linija 55-59: Bolja praksa bi bila unapred definisana metoda Double.isInfinite() umesto ručnih provera pri parsiranju.
- Linija 74-186: Umesto rekurzivnog pristupa, bolje je koristiti iterativni kako ne bi došlo do greške pri kalkulaciji izraza sa velikim brojem operacija.
### Code Smell:
- Metoda Calculate je previše velika i složena, bolja opcija bi bila podeliti je na manje metode za svaku operaciju.
- Mnoge metode pretpostavljaju da je ulaz validan, primer su prethodno navedene linije 32-35.

### Fajl: Start.java
- Linija 11: Poruka nije prilagođena višekratnom unosu, poželjno razjasniti.
- Linija 12: Scanner se inicijalizuje u svakoj iteraciji petlje, poželjno je premestiti ga izvan while petlje.
### Code Smell:
- Kod ne proverava validnost izraza pre prosleđivanja kalkulatoru.
- Upotreba reči exit za izlazak, bolja praksa je definisati EXIT_COMMAND konstantu.

### Zaključak
- Kod je funkcionalan i strukturiran, međutim ima prostora za poboljšanja u vidu čitljivosti, robostnosti i performansi. Najveći nedostatak je veličina i kompleksnost funkcije Calculate.
