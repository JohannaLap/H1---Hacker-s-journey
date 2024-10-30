
# Hacker's journey
## X) Tiivistelmä
Tämä tulee myöhässä. Olin ehtinyt tämän koko raportin kirjoittaa kun kone sammui, enkä ollut ehtinyt tallentaa.....jouduin siis aloittamaan raportin kirjoittamisen uudelleen.....Tästä opin, että kannattaa välissä kyllä aina tallennella..

## a) Kalin asentaminen
Asensin kalin ohjeiden mukaisesti.
![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/kali.png)

## b) Irroittaminen verkosta
Irroitin virtuaalikoneen verkosta virtualboxin asetusten kautta.
Testasin yhteyden pingillä.

![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/ping%20kali.png)

## c) Porttiskannaus

Skannasin 1000 tavallisinta tcp-porttia.
Tässä nähdään seuraavia tietoja: 
Nmpapin versio
Virtuaalikoneen ip-osoite (nähdään myös että olemassa on ipv6, jota ei skannattu) 
Aktiivinen yhteys
Skannatut portit ovat suljettuja ( eli ei käynnissä olevia palveluja)

![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/nmap.png)

## d) Uudelleen skannaus
Asensin apache2 ja ssh2. Varmistin, että nämmä käynnistyvät automaattisesti. 

![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/pakettien%20asennus.png)

![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/d26d3e4089cdf9b29ccb6ab33fb1350881a7f3c0/enable%20apache2%20enable%20ssh.png)

Ennen asennusta yhdistin koneen uudelleen verkkoon ja asennuksen jälkeen irrotin virtuaalikoneen uudelleen verkosta. 
Skannasin uuselleen portit. 
Skannauksen tulooksesta nähdään että varattuja portteja on nyt 2. 22 ja 80. Portti 22 käytössä ssh ja 80 käytössä http. 

![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/nmap%20localhost%20uusi.png)

## e) Metasploitable 2 asentaminen virtuaalikoneeseen
Loin uuden virtuaalikoneen, johon asensin onnistuneesti metasploitablen ohjeiden mukaisesti.


## f) Koneiden välinen virtuaaliverkko
Tein koneiden välille virtuaali verkon virtualboxin asetusten kautta.
Jotakin ongelmia tuli, kun en Kali koneella saanutkaan enää yhteyttä nettiin, enkä osaa sanoa mistä tämä johtuu. Ohjeiden mukaan jätin asetuksissa adapter1 natin päälle, mutta yhteys ei silti toiminut. 
Sain kuitenkin koneiden välisen yhteyden toimimaan, joten jatkoin siitä.

Tässä kokeilu pingillä metasploitablekoneeseen:

![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/ping%20to%20m.png)

Metasplotin tietokannan käynnistäminen ja tarkistus, että se on onnistunut: 

![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/msf%20run.png)

![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/dbstatus.png)


## g) Metasploitablen etsiminen porttiskannaamalla
Tein porttiskanneuksen koneiden yhteisessä verkossa. Tuloksena nähdään kahden koneen osoitteet.
![kuvateksti](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/sn%20verkko.png)

Tarkistin selaimella, että löysin oikean osoitteen

![](https://github.com/JohannaLap/H1---Hacker-s-journey/blob/main/webbi.png)


## h) Metasploitablen porttiskannaus
Tätä kohtaa en saanut tehtyä.


