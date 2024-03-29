# Drinkkiarkisto

Drinkkiarkisto on selainpohjaista käyttöliittymää käyttävä drinkinhakusovellus. 
Drinkkejä ovat cocktailit ja muut juomasekoitukset. 
Drinkkejä voi hakea juoman nimeen liittyvällä hakusanalla tai osa-aineen mukaan. 

Järjestelmään kirjaudutaan sisään.

Tavallinen käyttäjä voi hakea drinkkejä kannasta ja ehdottaa uusien lisäämistä kantaan. Tavallinen käyttäjä voi myös lisätä drinkkejä suosikkeihinsa jotka näytetään käyttäjälle. Käyttäjälle näytetään myös hänen lempi osa-aineensa laskettuna siitä montako kertaa aineosa on käyttäjän suosikki drinkeissä.
Järjestelmän ylläpitäjä voi lisätä järjestelmään drinkkejä joko kokonaan itse tai ehdotettuja hyväksymällä.  
Ylläpitäjä voi myös antaa muille käyttäjille admin oikeudet tai poistaa muun käyttäjän tilin.

Toimintoja:

  * Kirjautuminen
  * Drinkin haku
  * Drinkkien selailu
  * Drinkkien lisäys lomakkeella
  * Drinkin lisäys suosikkeihin
  * Uuden drinkin ehdottaminen / ehdotuksen hyväksyminen
  * Uuden osa-aineen ehdottaminen / ehdotuksen hyväksyminen
  * Käyttäjätunnuksen luominen
  * Salasanan muutos ja tilin poisto
  
### Heroku

https://tsoha-drinkkisovellus.herokuapp.com/

Admin
```
käyttäjätunnus: admin, salasana: salainen1
```
Regular
```
käyttäjätunnus: eika, salasana: salainen1
```

### Dokumentaatio

[Tietokantakaavio ja CREATE TABLE -lauseet](https://github.com/karoliinaemilia/drinkkiarkisto/blob/master/documentation/tietokantakaavio.md)

[User Stories ja SQL-kyselyt](https://github.com/karoliinaemilia/drinkkiarkisto/blob/master/documentation/userstories.md)

[Asennus- ja käyttöohjeet](https://github.com/karoliinaemilia/drinkkiarkisto/blob/master/documentation/asennus_kayttoohje.md)

### Omat ajatukset

Suunnitelluista käyttötapauksista melkein kaikki on toteutettu lukuun ottamatta drinkkien järjestämistä. Haku toiminnallisuus olisi myös voinut olla hieman laajempi.

Uuden drinkin lisääminen ja varsinkin siihen aineosien lisääminen oli hankalampaa kuin osasin odottaa. Tällä hetkellä drinkki ensin luodaan ja sitten siihen aletaan lisäämään ainesosia. Drinkin luomisessa aineosien lisäämisessä oleva hyväksy nappi on periaatteessa käytännöllisyydeltä aivan turha sillä sitä painamalla drinkki ei talletu tietokantaan sillä se on siellä jo. Nappi on enemmänkin käyttäjälle tarkoitettu että drinkin ehdotus tuntuu onnistuneen.

Sivutus oli odotettua helpompaa ainoa mikä ei onnistunut oli se että aineosien lisääminen on samalla sivulla listauksen kanssa joten en tiennyt miten saisin lähetettyä helposti sivutuksen uudestaan formin validoinnin epäonnistuessa joten ainesosan formi ei tällä hetkellä validoi uniikkisuutta mitä alunperin oli ajatus. Ylläpitäjän täytyy katsoa ettei lisää samaa ainetta joka sovelluksessa jo on ehdotuksia hyväksyessään.

Haku toiminto ei toimi herokussa enkä osannut sitä korjata, mutta se toimii kyllä lokaalisti. 

#### Sain haku toiminnon toimimaan vihdoinkin herokussa, olin pari minuuttia myöhässä, toivottavasti ei vaikuta kauheasti pisteisiin.
