# Oppimisteht-v-4

##AppLogger

**AppLogger** on C# kehitetty kirjasto lokitietojen kirjaamiseen. Se tarjoaa kätevän tavan tallentaa viestejä konsoliin, mikä voi olla hyödyllistä sovelluksen virheenkorjauksessa ja seurannassa.

`AppLogger`-kirjaston päätavoitteena on helpottaa lokituksen integroimista muihin projekteihin tarjoamalla minimaalisen mutta laajennettavissa olevan käyttöliittymän. Tässä tapauksessa `AppLogger` on toteutettu yksinkertaisena kirjastona, joka sisältää yhden `Logger`-luokan ja `Log`-metodin viestien tulostamiseen.

## Projektin rakenne

Projekti koostuu kahdesta pääosasta:

1. **AppLogger (class library)** — tämä on kirjasto, joka sisältää `Logger`-luokan ja `Log`-metodin. Metodi vastaanottaa merkkijonon ja tulostaa sen konsoliin, jolloin sovelluksen tapahtumia ja viestejä on helppo seurata. Kirjasto käyttää myös **Humanizer**-pakettia tekstin muotoilun parantamiseen.

2. **App (console application)** — tämä on konsolisovellus, joka demonstroi `AppLogger`:in toimintaa. Tässä sovelluksessa `Logger.Log`-metodia käytetään viestin tulostamiseen, minkä avulla voidaan nähdä, kuinka lokitus toimii reaaliajassa.

## Miten se toimii

1. **`Logger`-luokka** — kirjaston keskeinen osa. Se sisältää `Log`-metodin, joka vastaanottaa merkkijonon ja näyttää sen konsolissa. Metodia voidaan kutsua mistä tahansa sovelluksesta, joka on yhdistetty `AppLogger`-kirjastoon. Tässä projektissa käytetään vain perustoimintoja, mutta sitä voidaan laajentaa monimutkaisempiin tarpeisiin.

2. **Käyttöesimerkki** — konsolisovelluksessa `App` kutsu `Logger.Log("Viesti")` tulostaa annetun viestin konsoliin. Tämä mahdollistaa `AppLogger`-kirjaston käytön yksinkertaisena ja yleiskäyttöisenä lokitusratkaisuna, joka voidaan helposti liittää muihin projekteihin.
