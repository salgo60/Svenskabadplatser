# Svenska badplatser
Koppla Wikidata till Svenska badplatser som har NUTS dvs. det som finns hos [Havs- och vattenmyndighetens i Sverige länk](https://www.havochvatten.se/badplatser-och-badvatten.html) deras API [feature](https://badplatsen.havochvatten.se/badplatsen/api/feature) / [detail](https://badplatsen.havochvatten.se/badplatsen/api/detail) - karta [Wikidata med länk API](https://w.wiki/3GpF) - [deras dokumentation](https://drive.google.com/file/d/1vjv9B5a4gLU2k5jXCjXoB9_2Xwy1mDfU/view?usp=sharing)
* karta [badplatser](https://w.wiki/3GEr) - [video](https://youtu.be/uiHFgYUlHU8)
  * karta om [svensk Wikipedia artikel finns](https://w.wiki/3Gkm) 
    * vilka språk finns artiklar om Svenska badplatser med NUTS i Wikipedia - [sparql](https://w.wiki/3GyY) / [lista](https://w.wiki/3Gya)
    * bilder om avbildar dessa badplatser [SPARQL Federation](https://wcqs-beta.wmflabs.org/embed.html#%23defaultView%3AImageGrid%0ASELECT%20DISTINCT%20%3Fitem%20%3FitemLabel%20%3FitemDescription%20%3Fimage%20%3FNUTSid%20%3FNUTS%0AWITH%20%0A%7B%20SELECT%20%3Fitem%20%3FitemLabel%20%3FitemDescription%20%3FNUTSid%20%3FNUTS%20WHERE%0A%20%20%7B%20SERVICE%20%3Chttps%3A%2F%2Fquery.wikidata.org%2Fsparql%3E%0A%20%20%20%20%7B%20%3Fitem%20wdt%3AP31%2Fwdt%3AP279%2a%20wd%3AQ567998.%0A%20%20%20%20%20%20%3Fitem%20wdt%3AP605%20%3FNUTSid%3B%0A%20%20%20%20%20%20%20%20%20%20wdt%3AP17%20wd%3AQ34.%0A%20%20%20%20%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22sv%2Cen%22.%20%3Fitem%20rdfs%3Alabel%20%3FitemLabel%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20schema%3Adescription%20%3FitemDescription%20.%7D%0A%20%20%20%20%20BIND%28URI%28CONCAT%28%22https%3A%2F%2Fbadplatsen.havochvatten.se%2Fbadplatsen%2Fkarta%2F%23%2Fbath%2F%22%2C%3FNUTSid%29%29%20AS%20%3FNUTS%29%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D%20AS%20%25Wikidataitems%0A%0AWHERE%20%0A%7B%20%20INCLUDE%20%25Wikidataitems%20.%0A%20%20%3Ffile%20wdt%3AP180%20%3Fitem.%0A%20%20%3Ffile%20schema%3AcontentUrl%20%3Furl.%20%0A%20%20bind%28iri%28concat%28%22http%3A%2F%2Fcommons.wikimedia.org%2Fwiki%2FSpecial%3AFilePath%2F%22%2C%20wikibase%3AdecodeUri%28substr%28str%28%3Furl%29%2C53%29%29%29%29%20AS%20%3Fimage%29%0A%7D) - OBS [är en beta](https://diff.wikimedia.org/2020/10/29/sparql-in-the-shadow-of-structured-data-on-commons/)
  * karta [saknar bild](https://w.wiki/3Gv$) 
  * karta [saknar ligger vid vattenområde](https://w.wiki/3Gw4) - egenskap ligger vid vattenområde = [Property:P206](https://www.wikidata.org/wiki/Property:P206) 
  * karta [saknar "plats"](https://w.wiki/3Gw9) - egenskap plats e.g. Naturreservat = [Property:P276](https://www.wikidata.org/wiki/Property:P276) 
    * bra [karta att hitta svenska Naturreservat i Wikidata](https://map.wikilovesearth.se/#59.44228,18.03698,13z)  
  * karta [saknar "placerad på landform"](https://w.wiki/3GwC) - egenskap placerad på landform e.g. ö = [Property:P706](https://www.wikidata.org/wiki/Property:P706) 
  * karta saknar [Instagramplatsid](https://w.wiki/3Gkw) - [Property:P4173](https://www.wikidata.org/wiki/Property:P4173)
    * karta saknar [HashTag](https://w.wiki/3Gom) - [Property:P2572](https://www.wikidata.org/wiki/Property:P2572)
    * karta saknar [Facebook placeid](https://w.wiki/3Gon) - [Property:P1997](https://www.wikidata.org/wiki/Property:P1997)
* karta [hundbadplatser världen](https://w.wiki/3Gkg)
   * utan [koordinat](https://w.wiki/3Gkh)
## Feedback Havs- och vattenmyndighetens i Sverige
Magnus Sälgö 0705937579 - salgo60@msn.com
1) ange vid vilket vatten bad finns gärna med Sjöid [Property:P761](https://www.wikidata.org/wiki/Property:P761) eller Wikidata objekt
1) ange om badet finns på en ö eller liknande med samma som Wikidata objekt
## Tillgänglighetsdatabasen <-> badstränder
För att alla skull kunna använda exem pelvis badstränder behöv s tillgänglighetsinformation en variant är Tillgänglighatesdatabasen (dåligt använd men känns som den har stor potential, tveksam dock om det är bra maskinläsbardata) en annan är exempelvis [Open Street Map](https://wiki.openstreetmap.org/wiki/Accessibility)
* [Video om Tillgänglighetsdatabasen](https://vimeo.com/325190731)
Finns idag ingen koppling Wikidata till denna database men skapar en "fusk variant" 
* [Tillgänglighetsdatabasen](https://www.t-d.se/)
* [Wikidata <-> Tillgänglighetsdatabasen](https://w.wiki/3Gou)
  * visar de bad jag hittat i Tillgänglighetsdatabasen och kopplat i Wikidata OBS alla har inte NUTS
* exempel [wheelmap.org](https://wheelmap.org/search) hur man borde kunna hitta badplatser med rätt tillgänglighet
  * <em>Wheelmap is a map for finding wheelchair accessible places. The map works similar to Wikipedia: Anyone can contribute and mark public places around the world according to their wheelchair accessibility. The criteria for marking places is based on a simple traffic light system:</em> [FAQ](https://news.wheelmap.org/en/FAQ/)
![](https://news.wheelmap.org/en/wp-content/uploads/sites/2/2018/03/FlowchartWheelmapEN-1797x2048.jpg) 
## Entity schema - att göra definierar vilka egenskaper som skall finnas i Wikidata för dessa objekt
för att data skall bli mer konsistent så skapas olika schema se [video](https://www.youtube.com/watch?v=ZHdjwbLgzvE)
* [EntitySchema:E304](https://www.wikidata.org/wiki/EntitySchema:E304) Hundbadplatser
* [EntitySchema:E305](https://www.wikidata.org/wiki/EntitySchema:E305) Svenskaplatser med NUTS
