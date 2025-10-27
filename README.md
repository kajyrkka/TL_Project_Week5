# TL_Project_Week5

## 🎯 Viikon perustavoite
Toteuta **Pythonilla opetusalgoritmi K-means-luokittelijalle** kiihtyvyysanturidatan (x, y, z + suuntatieto) avulla.  
Lisäksi viikon ylimääräisessä tehtävässä opit käyttämään **Google Colabia** konvoluutioneuroverkon (CNN) opettamiseen samoista kiihtyvyysanturidatoista.

---

## 0. Ohjeet Scrum-tiimille (= 6 työparia)
- Viikon vastuullinen työpari pitää **daily-palaverit keskiviikkoisin ja torstaisin**.  
- Daily-palavereista raportoidaan **Scrum-tiimin Discord-kanavalle**:
  - Ketkä olivat paikalla  
  - Missä vaiheessa kukin työpari on menossa  
  - Mahdolliset ongelmat  

- Viikon vastuullinen työpari järjestää **perjantaisin sprint review -palaverin** ja laatii **Discordiin raportin viikon tuloksista**.  
  Raportissa mainitaan myös seuraavan viikon vastuullinen työpari.

- Tutustukaa alla oleviin viikon tehtäviin ja laatikaa **GitHubin projektin Kanban-tauluun suunnitelma**, missä vaiheissa aiotte tehtävät toteuttaa ja testata.  


---

## 1. Toteuta Pythonilla K-means-luokittelija

### Tehtävän kuvaus
Hae tietokannasta keräämäsi kiihtyvyysanturilla mitattu data (**x, y, z + suuntatieto**) omalle koneellesi ja tee **K-means-luokittelijan opetusalgoritmi** Pythonilla.  
Suuntatietoa ei tarvita K-means-algoritmissa, mutta sitä tarvitaan myöhemmin neuroverkon opetustehtävässä.

Tehtävä on kuvattu tarkemmin tiedostossa **"Viikon 5 tehtävät.ppt"**, joka löytyy tästä samasta GitHub-repositorystä.

### Opetuksen tulos
Opetuksen tuloksena syntyy tiedosto **`keskipisteet.h`**, joka sisältää C-kielisen taulukon opetetuista keskipisteistä.  

Esimerkki rakenteesta:
<pre> int CP[6][3] = {
    {1, 0, 0},  // Keskipiste 1: x-akselilla pieni arvo
    {2, 0, 0},  // Keskipiste 2: x-akselilla suuri arvo
    {0, 1, 0},  // Keskipiste 3
    {0, 2, 0},  // Keskipiste 4
    {0, 0, 1},  // Keskipiste 5
    {0, 0, 2}   // Keskipiste 6
};
</pre>
💡 Tämä tiedosto toimii myöhemmin mikrokontrolleriohjelmassa valmiina alustustaulukona.

# 🧠 Viikon 5 – Lisätehtävät (valinnaiset), Opeta Google Colabissa konvoluutioneuroverkko (CNN)
### 1️⃣ Vaihe 1 – Datan valmistelu

Tuo aiemmin keräämäsi 1 sekunnin mittaiset X, Y, Z -datan ja suuntatiedon Google Colabiin.

Järjestä data omiin hakemistoihinsa luokkien (labelien) perusteella.

### 2️⃣ Vaihe 2 – Datasetin muodostus

Muodosta opetus-, validointi- ja testidatasetit seuraamalla TensorFlow Simple Audio -mallia:
🔗 https://www.tensorflow.org/tutorials/audio/simple_audio

Muunna sekunnin mittaiset signaalit spektrogrammikuviksi, kuten Simple Audio -mallissa.

Eri luokkien (labelien) tunnistus perustuu näihin 2D-spektrogrammikuviin.

### 3️⃣ Vaihe 3 – CNN:n opetus

Opeta konvoluutioneuroverkko (CNN) spektrogrammikuvien perusteella.

Pyri minimoimaan mallin parametrien määrä, jotta malli voidaan toteuttaa myöhemmin NRF5340DK-mikrokontrollerissa.

### 4️⃣ Vaihe 4 – Mallin arviointi ja tallennus

Laske confusion matrix Simple Audio -mallin mukaisesti.

Tallenna opettamasi malli myöhempää käyttöä varten.

📋 Yhteenveto

1. K-means-luokittelija	Toteuta Pythonilla opetusalgoritmi kiihtyvyysdatalle	keskipisteet.h
2. Ylimääräinen tehtävä	Opeta CNN Google Colabissa käyttäen spektrogrammikuvia	CNN-malli + confusion matrix

Tsemppiä viikon 5 tehtäviin! 🚀