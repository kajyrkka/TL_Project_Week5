# TL_Project_Week5

## 1. Viikon 5 tavoite (arvosana max 3)
Toteuta **Pythonilla opetusalgoritmi K-means-luokittelijalle** kiihtyvyysanturidatan (x, y, z + suuntatieto) avulla.  

## 1.1 Toteuta Pythonilla K-means-luokittelija

### Tehtävän kuvaus
Hae tietokannasta keräämäsi kiihtyvyysanturilla mitattu data (**x, y, z + suuntatieto**) omalle koneellesi ja tee **K-means-luokittelijan opetusalgoritmi** Pythonilla.  
K-means algoritmin toteutus koostuu seuraavista vaiheista:
1) Arvotaan 6 kpl keskipisteitä 3D-ulottuvuudessa (x,y,z)
2) Mitataan kaikkien x,y,z datapisteiden etäisyys jokaiseen 6:teen keskipisteeseen. Keskipiste, johon etäisyys on pienin voittaa ja "saa" pisteen itselleen.
3) Lasketaan uudet 6 kpl keskipisteitä edellisessä vaiheessa (2) voitettujen pisteiden avulla
4) Toistetaan kohtia 2 ja 3 kunnes keskipisteet eivät enää muutu (= algoritmi on löytänyt parhaat keskipisteet 6 suunnan luokittelemiseksi)
5) Lopuksi kirjoita algoritmin antamat 6 keskipistettä keskipisteet.h tiedostoon seuraavan viikon mikrokontrolleritoteutusta varten.

Tehtävä on kuvattu vielä edellistä tarkemmin tiedostossa **"Viikon 5 tehtävät.ppt"**, joka löytyy tästä samasta GitHub-repositorystä.

**HUOM: tämä tehtävä on tarkoitus suorittaa ilman AI:n tukea. Ottakaa haaste vastaan ja yrittäkää koodata algoritmi ihan itse**

### Opetuksen tulos
Opetuksen tuloksena syntyy tiedosto **`keskipisteet.h`**, joka sisältää C-kielisen taulukon opetetuista keskipisteistä.  

Esimerkki rakenteesta:
<pre> int CP[6][3] = {
    {1, 0, 0},  // Keskipiste 1: x-akselilla pieni arvo, keskipiste arvot kuvitteellisia
    {2, 0, 0},  // Keskipiste 2: x-akselilla suuri arvo
    {0, 1, 0},  // Keskipiste 3
    {0, 2, 0},  // Keskipiste 4
    {0, 0, 1},  // Keskipiste 5
    {0, 0, 2}   // Keskipiste 6
};
</pre>


# 🧠 Viikon 5 – lisätavoite (arvosanat max 4-5)

## Opeta Google Colabissa konvoluutioneuroverkko (CNN)
### Vaihe 1 – Datan valmistelu

Tuo aiemmin keräämäsi 1 sekunnin mittaiset X, Y, Z -datat tiedostoina.

Järjestä data omiin hakemistoihinsa luokkien (labelien) perusteella.

### Vaihe 2 – Datasetin muodostus

Muodosta opetus-, validointi- ja testidatasetit seuraamalla TensorFlow Simple Audio -mallia:
🔗 https://www.tensorflow.org/tutorials/audio/simple_audio

Muunna sekunnin mittaiset signaalit spektrogrammikuviksi, kuten Simple Audio -mallissa.

Eri luokkien (labelien) tunnistus perustuu näihin 2D-spektrogrammikuviin.

### Vaihe 3 – CNN:n opetus

Opeta konvoluutioneuroverkko (CNN) spektrogrammikuvien perusteella.

Pyri minimoimaan mallin parametrien määrä, jotta malli voidaan toteuttaa myöhemmin NRF5340DK-mikrokontrollerissa.

### Vaihe 4 – Mallin arviointi ja tallennus

Laske confusion matrix Simple Audio -mallin mukaisesti.

Tallenna opettamasi malli myöhempää käyttöä varten.

