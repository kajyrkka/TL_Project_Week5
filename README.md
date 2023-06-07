# TL_Project_Week5

# Viikon perustavoite = Toteuta Pythonilla opetusalgoritmi K-means luokittelijalle.

Hae tietokannasta keräämäsi kiihtyvyysanturilla mitattu sensoridata (x,y,z + suuntatieto) omalle
koneellesi ja tee opetusalgoritmi K-means luokittelijalle (suuntatietoa ei tarvita K-means algoritmissa,
mutta ylimääräisessa neuroverkon opetustehtävässä sitä tarvitaan).

Tehtävä on kuvattu tarkemmin Viikon 5 tehtävat.ppt tiedostossa, mikä löytyy tästä samasta github
repositorystä. Opetuksen tuloksena on siis keskipisteet.h tiedosto, missä on c-source tiedostoon
helposti incluudattava 2 uloitteisen taulukon alustus = opetetut keskipisteet alustettuna. Esim
seuraavaan tyyliin:

int CP[6][3]={
	           {1,0,0},  // keskipiste 1, missä x-akselilla pieni arvo, y ja z akseleilla kiihtyvyys 0
			   {2,0,0},  // keskipiste 2, missä x-akselilla suuri arvo, y ja z akseleilla kiihtyvyys 0
			   {0,1,0},  // jne... CP = CenterPoint
			   {0,2,0},
			   {0,0,1},
			   {0,0,2}
};


# Viikon ylimääräinen tavoite = Opeta Google Colabin avulla neuroverkkoluokittelija.

Suunnittele neuroverkkoluokittelijan rakenne, joka ottaan inputtina x,y,z arvot ja luokittelee
inputin 6:een luokkaan. Ei kannata tehdä neuroverkosta liian monimutkaista (korkeintaan yksi hidden layer
inputin ja output layerin väliin), koska opetettu algoritmi pitää osata vielä toteutta c:llä
viikolla 6 ylimääräisenä tehtävän.

Lähde liikkeelle esim https://keras.io/examples/vision/mnist_convnet/ esimerkistä ja opeta suunnittelemasi
neuroverkko omalla datalla (x,y,z + suunta). 

Tee python koodi, joka ottaa inputtina opettamasi neuroverkon parametrit (weight+bias arvot hidden ja
output layereille) ja joka laskee inputtina annetuista x,y,z arvoista saman tuloksen, jonka saat
google GoLabissa model.predict funktiolla samalle x,y,z arvolle. Eli tämähän todistaa, että osaat
ainakin pythonilla laskea neuroverkon tuloksen oikein. Tämä nimittäin auttaa ensi viikon ylimääräisessä
toteutuksessa varsinkin, jos olet toteuttanut neuroverkon pythonin for-luuppien avulla eikä numpyn
vektorilaskentaa hyödyntäen.

Tuloksena ylimääräisestä tehtävästä on tuo "todistus" neuroverkon oikeasta laskennasta Pythoilla ja
neuroverkonKertoimet.h tiedosto, joka voidaan helposti incluudata ensi viikolla c-toteutukseen.