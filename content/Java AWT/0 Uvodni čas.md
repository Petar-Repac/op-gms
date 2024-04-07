## O programskom paketu AWT

**Java AWT**  (Abstract Window Toolkit) je [API](https://sr.wikipedia.org/wiki/API) za razvoj *Grafičkih Korisničkih Interfejsa* (Graphical User Interface - GUI) ili grafičkih aplikacija pisanih u Javi.

Da bismo mogli napisati neku grafičku aplikaciju koristeći AWT, potrebno je prvo da se upoznamo sa hijerarhijom klasa koje nam  AWT pruža:

![[Pasted image 20240407163230.png]]

## Komponente

Elementi GUI-ja kao što su: dugmići, tekstualna polja, labele itd. nazivaju se komponente.
Nazivi klasa komponenti u AWT-u su prikazani na dijagramu.
Da bismo mogli prikazati komponentu na ekranu, ona se mora nalaziti unutar nekog **Container-a**.

### Kontejneri (Container)

Kontejneri su elemnti grafičkog interfejsa, predstavljeni posebnom klasom u AWT-u koji služe tome da sadrže komponente.
Kontejner je apstrakcija, sa svojim konkretnim implementacijama koje vidimo na dijagramu: **Frame**, **Dialog** i **Panel**.
U suštini kontejner određuje svoj sadržaj (koje komponente u sebi drži) i raspored/pozicioniranje komponenti koje sadrži ( *Layout*, više o ovome kasnije).

Tipovi kontejnera u Java AWT paketu su:
			1. Window
			2. Panel
			3. Frame
			4. Dialog
#### Prozor (Window)

Window je kontejner koji nema ivice niti trake za menije. Moramo napraviti instancu Frame, Dialog ili drugu instancu Window klase da bismo napravili ovu vrstu Containera.

#### Dijalog (Dialog)

Dialog je jednostavan kontejner sa ivicama i naslovom. Može postojati samostalno, i uglavnom se koristi za prikaz upozorenja, obaveštenja ili jednostavnih ulaznih komponenti.

#### Panel 

Panel je kontejner koji ne koristi ni naslov, ni trake za menije, niti ima ivice. To je generički kontejner za smeštanje i pozicioniranje sadržaja. Da bismo prikazivali komponente, uglavnom ćemo ih smeštati u Panele.

#### Okvir (Frame)

Frame je kontejner koji sadrži naslov, ivice i traku za meni. Može i direktno sadržati druge komponente (dugmiće, labele, skrol-trake itd..). Može i sadržati više drugih kontejnera (uglavnom panela).


## Korisne metode klase Component

```java
// dodaje komponentu c komponenti nad kojom je pozvana
public void add(Component c);  

// podešava dimenzije komponente
public void setSize(int width,int height);

// određuje način raspoređivanja/pozicioniranja komponenti unutar ove komponente
public void setLayout(LayoutManager m);

// određuje vidljivost - da li se komponenta prikazuje ili ne
public void setVisible(boolean status);
 
```


*Oznake lekcije:*

#java #awt #gui #teorija
