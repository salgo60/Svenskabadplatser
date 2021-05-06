# Svenska badplatser
* [Issues](https://github.com/salgo60/Svenskabadplatser/issues?q=is%3Aissue+) / [closed](https://github.com/salgo60/Svenskabadplatser/issues?q=is%3Aissue+is%3Aclosed)
* [diskussion](https://github.com/salgo60/Svenskabadplatser/discussions)

**Status:** 2695 badplatser har importerats och kopplats till kommuner se [karta](https://w.wiki/3GEr). Nästa steg är att länka datat till sjö den finns vid, sociala medier som [Instagram plats id](https://www.wikidata.org/wiki/Property:P4173), naturreservat eller annat badet finns vid, försöka hitta kommunens egen beskrivning av badet, se om vi kan få svar från Tillgänglighetsdatabasen och skapa en koppling

**Task:** koppla Wikidata till Svenska badplatser som har [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter) dvs. det som finns hos [Havs- och vattenmyndighetens i Sverige länk](https://www.havochvatten.se/badplatser-och-badvatten.html) deras API [feature](https://badplatsen.havochvatten.se/badplatsen/api/feature) / [detail](https://badplatsen.havochvatten.se/badplatsen/api/detail) - karta [Wikidata med länk API](https://w.wiki/3GpF) - [deras dokumentation](https://drive.google.com/file/d/1vjv9B5a4gLU2k5jXCjXoB9_2Xwy1mDfU/view?usp=sharing)

**Lesson learned:** finns tydliga fördningar [2001:100](https://www.riksdagen.se/sv/dokument-lagar/dokument/svensk-forfattningssamling/forordning-2001100-om-den-officiella_sfs-2001-100) vilka myndigheter som är ansvariga för statistik där Havs- och vattenmyndigheten har ett ansvar som sedan i deras regleringsbrev [2011:619](https://www.riksdagen.se/sv/dokument-lagar/dokument/_sfs-2011-619) kanske lite vagt beskrivs som *"miljöövervakning, uppföljning av miljökvalitetsmålen och internationell rapportering"* 
   * [Badvattendirektivet](https://www.svensktvatten.se/om-oss/europeiska-unionen/badvattendirektivet/) 
      * På sidan ["Kontroll av badvattenkvalitet"](https://www.havochvatten.se/overvakning-och-uppfoljning/miljoovervakning/marin-miljoovervakning/kontroll-av-badvattenkvalitet.html) står det *Alla EU-bad finns registrerade på webbplatsen Badplatsen och kommunerna får även registrera övriga bad.*
         * min tolkning är att inga problem finns att ha alla bad i detta register - skall verifieras av Havs- och vattenmyndigheten  
           * jag ser inga problem att ha "alla" bad i Wikidata med koppling Open Street Map 
   * [2006/7/EG Europaparlamentets och rådets direktiv 2006/7/EG av den 15 februari 2006 om förvaltning av badvattenkvaliteten och om upphävande av direktiv 76/160/EEG](https://eur-lex.europa.eu/legal-content/SV/TXT/PDF/?uri=CELEX:32006L0007&from=EN)
   * [Bathing water management in Europe:Successes and challenges](https://www.eea.europa.eu//publications/bathing-water-quality-2020)
     * [Bathing Mater Quality Information for Public in Europe -Availability and Issue of Integration of Data for the European Level](https://www.researchgate.net/publication/267766499_Bathing_Mater_Quality_Information_for_Public_in_Europe_-Availability_and_Issue_of_Integration_of_Data_for_the_European_Level)

* [European bathing water quality in 2019](https://www.eea.europa.eu/publications/european-bathing-water-quality-in-2019/european-bathing-water-quality-in-2019)
* [eea.europa.eu/Bathingwater](https://discomap.eea.europa.eu/Bathingwater/) - database med alla EU bad
* havochvatten.se [Kontroll av badvattenkvalitet](https://www.havochvatten.se/overvakning-och-uppfoljning/miljoovervakning/marin-miljoovervakning/kontroll-av-badvattenkvalitet.html#:~:text=Kommunerna%20ansvarar%20f%C3%B6r%20%C3%B6vervakningen%20av,och%20rapportering%20till%20EU%2Dkommissionen.)

## Wikidata
![](https://community.dataportal.se/assets/uploads/files/1620115933238-84ccdfe1-eadc-4c49-9e7a-cb030a664a93-image.png). 
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
### Fel i datat
* koordinat Kullöbadet saknas [SE0110187000005215](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0110187000005215) = [Q106712251](https://www.wikidata.org/wiki/Q106712251)
* [SE0622031000005258](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0622031000005258) - WD [Q106712254](https://www.wikidata.org/wiki/Q106712254) - badplats Glistjärn
* koordinat [SE0A21492000005899](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0A21492000005899) - WD [Q106712312](https://www.wikidata.org/wiki/Q106712312) - badplats Ärr - Fröskog - [issues/8](https://github.com/salgo60/Svenskabadplatser/issues/8)
* [SE0230509000004536](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0230509000004536) se [Issue 2](https://github.com/salgo60/Svenskabadplatser/issues/2)
* koordinat Kullöbadet saknas [SE0110187000005215](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0110187000005215) = [Q106712251](https://www.wikidata.org/wiki/Q106712251)
* koordinat [SE0611785000005779](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0611785000005779) - Strandbad, Ekenäs , Säffle se [Issue 4](https://github.com/salgo60/Svenskabadplatser/issues/4)
* koordinat fel [SE0110188000005455](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0110188000005455) WD [Q106712277](https://www.wikidata.org/wiki/Q106712277) - badplats Lågarö-Örn
* [SE0611763000005739](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0611763000005739) - WD [Q106712301](https://www.wikidata.org/wiki/Q106712301) - [ssues/5](https://github.com/salgo60/Svenskabadplatser/issues/5)
* [SE0230581000005959](https://badplatsen.havochvatten.se/badplatsen/karta/#/bath/SE0230581000005959) - WD [Q106712315](https://www.wikidata.org/wiki/Q106712315) - badplats Dalbystrand - [issues/6](https://github.com/salgo60/Svenskabadplatser/issues/6)

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
## API 

* [SMHI Open Data API Docs](https://opendata.smhi.se/apidocs/metfcst/parameters.html)

## [Open Data Badplatser](https://www.dataportal.se/sv/datasets?p=1&q=Badplatser&s=2&t=20&f=&rt=dataset%24esterms_IndependentDataService%24esterms_ServedByDataService)
* [Uppsala kommun](https://opendata.uppsala.se/datasets/aadc5420e8884d32b2efe0d10fbfdfe5_0/geoservice?geometry=15.925%2C59.642%2C19.874%2C60.125)
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad 
* Södertälje
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad
* [Karlskrona kommun](https://service.karlskrona.se/FileStorageArea/Documents/bad/swimAreas.geojson)
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad
* Gävle kommun
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad 
* [Skövde kommun](https://geodata.skovde.se/linkdokument/OpenData/Skovde_Badanlaggningar_Badplatser.json)
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad 
* [Umeå kommun](https://www.dataportal.se/sv/datasets/43_43844/badplatser)
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad 
* [Sundbybergs stad](https://www.dataportal.se/sv/datasets/281_1606/badplatser-i-sundbyberg#ref=?p=1&q=Badplatser&s=2&t=20&f=&rt=dataset%24esterms_IndependentDataService%24esterms_ServedByDataService)
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad 
* [Linköpings kommun](http://waterqualityobserved.linkoping.se/swagger/index.html)
* .....

## Kontakter
* [Mattias Andersson](https://www.linkedin.com/in/mattiasrandersson) badvatten@havochvatten.se [Enheten för utveckling och systemförvaltning](https://www.havochvatten.se/om-oss-kontakt-och-karriar/organisation/avdelningen-for-digitalisering/enheten-for-utveckling-och-systemforvaltning.html) email: tel: 010-6986296
