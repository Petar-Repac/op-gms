
Na ovim vežbama ćemo proći kroz proces pisanja jedne jednostavne Java AWT aplikacije da bismo se bolje upoznali sa klasama i metodama koje nam AWT programski paket nudi.


## Aplikacija

Aplikacija koju pišemo će biti prozor veličine 300x300px (ovo je format ŠIRINA x VISINA) i sadržaće dugme određenih dimenzija na određenoj poziciji na kojem piše "Klikni me". Klik na dugme, za sada, neće imati nikakav efekat na aplikaciju.

![[Capture.png]]

### Kod

```java
import java.awt.*;

public class PrviPrimer extends Frame {

	public PrviPrimer() {
		
		Button dugme = new Button("Klikni me");
		
		// Pozicija i dimenzije dugmeta (x, y, width, height)
		dugme.setBounds(30, 100, 80, 30); 
		
		// dodajemo dugme u ovaj Frame (PrviPrimer je instanca klase Frame)
		add(dugme); 
		
		// velicina ovog prozora ce biti 300x300px
		setSize(300,300); 
		
		// ako ne postavimo nikakav Layout, default ce biti BorderLayout
		setLayout(null); 
		
		// sada je Frame vidljiv, po defaultu nisu vidljivi
		setVisible(true); 
	}
	
	
	public static void main(String[] args) { 
			
		PrviPrimer instancaAplikacije = new PrviPrimer();
	}

}

```

#### Kako smo dobili prikaz Frame-a?

Klasa *"PrviPrimer"* koju smo napisali  nasleđuje, tj. proširuje klasu *Frame*, to jest nasčeđuje sva njena zaštićena i javna polja i metode.
Nasleđivanjem klase *Frame* imamo pogodnost da ne moramo pisati gomilu koda "od nule" za iscrtavanje prozora, već je to neko unapred napisao za nas u programskom paketu AWT.

#### Kako radi setBounds()?

Metoda *setBounds()* koju pozivamo nad objektom dugme prihvata četiri celobrojna argumenta, koji predstavljaju veličine izražene u [pikselima](https://sr.wikipedia.org/sr/%D0%9F%D0%B8%D0%BA%D1%81%D0%B5%D0%BB) : 

- x koordinatu
- y koordinatu
- širinu
- visinu

Koordinate u programskom paketu AWT, ali i u GUI desktop aplikacijama uopšte se tumače na sledeći način:

**Gornja leva tačka samog početka prozora je na koordinati (0,0). 
Povećavanjem X koordinate pomeramo element za toliko piksela od leve ivice, tj. pomeramo ga za toliko piksela udesno.
Povećavanjem Y koordinate pomeramo element za toliko piksela od gornje ivice, tj. pomeramo ga nadole.**

Nakon što smo odredili poziciju i veličinu dugmeta, dodajemo ga našem Frame-u i postavljamo veličinu Frame-a na 300x300px.

Pozivom metode **setLayout(null)** našem Frame-u postavljamo LayoutManager (sistem raspoređivanja/pozicioniranja komponenti).
Pošto smo prosledili prazan pokazivač, Frame PrviPrimer će kao LayoutManager imati postavljen svoj default: [BorderLayout](https://docs.oracle.com/javase%2F7%2Fdocs%2Fapi%2F%2F/java/awt/BorderLayout.html).
Više o Layoutima ćemo pričati kasnije.

Nakon što smo postavili vidljivost Frame-a na **true**, sigurni smo da će se naša aplikacija prikazati.


### Pitanja

1. Šta se dešava kada kliknemo na dugme?
2. Šta se dešava kada pokušamo zatvoriti prozor? Zašto?
3. Kako možemo isključiti našu aplikaciju?

*Oznake lekcije:*

#java #awt #gui #vežbe 



