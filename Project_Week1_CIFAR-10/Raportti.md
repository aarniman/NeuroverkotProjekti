### Raportti projektista

Tässä raportissa vertaillaan kahta eri mallia CIFAR-10CNN ja CIFAR-10_FCN. Kun vertaillaan suorituskykyä CNN antaa tarkemman tarkkuuden (0.76289). FCN on hieman epätarkempi ja antaa testin tarkkuudeksi (0.533999). Tämä johtuu siitä, koska CNN on suunniteltu käsittelemään kuvia kuten taas FCN ei ole tehokas kuvien käsittelemisessä.

Kun vertaillaan mallien opetusaikoja, FCN on nopeampi kouluttaa verrattuna CNN:ään. Tämä johtuu siitä, että FCN-mallissa ei ole konvoluutio (conv2d_2) kerroksia, jotka vaativat enemmän laskentatehoa. CNN käyttää useita konvoluutiokerroksia, jotka parantavat sen tarkkuutta, mutta tekevät koulutuksesta hitaampaa.

Parametrien ero määrässä on huomattava CNN:ssä parametreja on 79,754 (311.54 KB) ja FCN:ssä niitä on 1,738,890 (6.63 MB). FCN:ssä on paljon parametereja, koska se käyttää suuria Dense layereitä, kun taas CNN käyttää konvoluutiolayereitä

### Johtopäätöksen ja havainnot

- FCN soveltaminen kuvankäsittelytehtävään ei ole tehokasta. FCN malli ei pysty hyödyntämään kuvassa olevia piirteitä yhtä hyvin kuin CNN malli, mikä johtaa virheisiin tuloksessa luokittelutehtävässä.

- CNN saavutti tarkkuuden 0.7629, mikä tarkoittaa, että se on tehokas kuvankäsittelyssä. Tämä johtuu siitä, että CNN on erityisesti suunniteltu löytämään kuvista piirteitä, kuten tekstuureja, mikä auttaa luokittelussa.

- CNN-mallilla huomaaa, että vaikka malli oli tarkka se teki virheitä kuten kissojen ja koirien tunnistamisessa. Tämä voi johtua siitä, että näiden luokkien visuaaliset piirteet voivat olla samankaltaisia, ja malli ei pysty erottamaan niitä aina.

- FCN-malli oli nopeampi koulutuksessa, mutta sen suorituskyky jäi heikommaksi
