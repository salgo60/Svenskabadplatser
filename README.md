# Svenska badplatser

**Task:** koppla Wikidata till Svenska badplatser som har [bathingWaterIdentifier](https://www.wikidata.org/wiki/Wikidata:Property_proposal/bathingWaterIdentifier) dvs. det som finns hos [Havs- och vattenmyndighetens i Sverige länk](https://www.havochvatten.se/badplatser-och-badvatten.html) deras API [feature](https://badplatsen.havochvatten.se/badplatsen/api/feature) / [detail](https://badplatsen.havochvatten.se/badplatsen/api/detail) - karta [Wikidata med länk API](https://w.wiki/3MZg) - [deras dokumentation](https://drive.google.com/file/d/1vjv9B5a4gLU2k5jXCjXoB9_2Xwy1mDfU/view?usp=sharing)
* **vilka dataset skall badvatten kopplas till?**
  * [Naturreservat](https://w.wiki/3MwX)
  * [Koppling närliggande vatten](https://query.wikidata.org/embed.html#%23defaultView%3AMap%7B%22hide%22%3A%5B%22%3Fbathcoord%22%2C%22%3Flakecoord%22%2C%22%3Fline%22%2C%22%3Fstr%22%2C%22%3Flayer%22%5D%7D%0ASELECT%20%3Fstr%20%3Fbathwater%20%3FbathwaterLabel%20%3Fbathcoord%20%3Flake%20%3FlakeLabel%20%3Flakecoord%20%3Fdist%20%3Fline%20%3FSJOID%20%3Flayer%20WHERE%20%7B%0A%20%20%3Fbathwater%20wdt%3AP6104%20wd%3AQ106774536.%0A%20%20%20%3Fbathwater%20%20wdt%3AP625%20%3Fxx.%0A%20%20%20%3Fbathwater%20%20p%3AP625%20%5B%20a%20wikibase%3ABestRank%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20psv%3AP625%20%5B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoLatitude%20%3Fbathcoordlat%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoLongitude%20%3Fbathcoordlon%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoGlobe%20%3Fglobe%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%5D%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20ps%3AP625%20%3Fbathcoord%0A%20%20%20%20%20%20%20%20%20%20%5D%0A%20%20OPTIONAL%20%7B%20%3Fbathwater%20wdt%3AP605%20%3FNUTSID.%20%7D%0A%20%20%7B%0A%20%20%20%20%3Fbathwater%20wdt%3AP206%20%3Flake.%0A%20%20%20%3Flake%20%20wdt%3AP625%20%3Frr.%0A%20%20%20%20%20%20%20%3Flake%20%20p%3AP625%20%5Ba%20wikibase%3ABestRank%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20psv%3AP625%20%5B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoLatitude%20%3Flat%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoLongitude%20%3Flong%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoGlobe%20%3Fglobe2%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%5D%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20ps%3AP625%20%3Flakecoord%0A%20%20%20%20%20%20%20%20%20%20%5D%0A%20%20%20%20OPTIONAL%20%7B%20%3Flake%20wdt%3AP761%20%3FSJOID.%20%7D%0A%20%20%7D%0A%20%20%20BIND%28geof%3Adistance%28%3Fbathcoord%2C%20%3Flakecoord%29%20as%20%3Fdist%29%20.%20%0A%20%20%23filter%20%28%3Fdist%20%3E%3D%203%29%0A%20%20BIND%20%28floor%28%3Fdist%2F10%29%2a10%20as%20%3Flayer%29%20%0A%20%20BIND%28CONCAT%28%27LINESTRING%20%28%27%2C%20STR%28%3Fbathcoordlon%29%2C%20%27%20%27%2C%20STR%28%3Fbathcoordlat%29%2C%20%27%2C%27%2C%20STR%28%3Flong%29%2C%20%27%20%27%2C%20STR%28%3Flat%29%2C%20%27%29%27%29%20AS%20%3Fstr%29%20.%0A%20%20BIND%28STRDT%28%3Fstr%2C%20geo%3AwktLiteral%29%20AS%20%3Fline%29%20%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22sv%2Cen%22.%20%7D%0A%7D%0AORDER%20BY%20DESC%28%3Fdist%29%0A) finns inte idag hos Havs- och vattenmyndighetens men intresse fanns 
  * Kustvatten --> [issues/83](https://github.com/salgo60/Svenskabadplatser/issues/83)
---
* **[Data kvalitet i Wikidata](https://www.wikidata.org/wiki/Wikidata:WikiProject_Sweden/Svenska_badplatser/Coverage2)** 2782 badplatser registrerade där 97.05% har "Nutskod", 39.14% är kopplade till närliggande vatten [P206](https://www.wikidata.org/wiki/Property:P206)  
    * **Issues/frågor** 
       * [Havs- och vattenmyndigheten](https://github.com/salgo60/Svenskabadplatser/issues?q=label%3A%22Havs-+och+vattenmyndighetens%22)
       * [Koordinater som uppfattas felaktiga](https://github.com/salgo60/Svenskabadplatser/issues?q=label%3A%22invalid+coordinate%22+) - [SPARQL](https://w.wiki/3NFk)
    * [Wikidata badplatser <-> Open Street Map](https://github.com/salgo60/Svenskabadplatser/blob/main/Jupyter/OSM_Wikidata_Bathwater.ipynb) ej kopplade 2080, vatten ej kopplade 230, naturreservat ej kopplade 84

![](https://github.com/salgo60/Svenskabadplatser/blob/main/img/QA.png)
* **Change log** 
  * 2020-05-23 hur anger vi i vårt data så att det går enkelt att ta sig dit kommunalt se [discussions/88](https://github.com/salgo60/Svenskabadplatser/discussions/88).
  * 2020-05-22 **Nya egenskaper i WD** att rösta på
       * [Naturkartan](https://www.wikidata.org/wiki/Wikidata:Property_proposal/naturkartan.se_ID#%7B%7Bint%3ATalk%7D%7D)
       * [Badkartan](https://www.wikidata.org/w/index.php?title=Wikidata:Property_proposal/Badkartan.se_ID) 
       * [Eionet bathingWaterIdentifier](https://www.wikidata.org/wiki/Wikidata:Property_proposal/bathingWaterIdentifier)
  * 2020-05-21 task att koppla badplatser som finns i ett Naturreservat [issues/77](https://github.com/salgo60/Svenskabadplatser/issues/77)  **Lösning** [SPARQL](https://w.wiki/3MwX)
  * 2020-05-20 [tweet Havsmiljöinstitutet](https://twitter.com/havsmiljo/status/1395294755035258881?s=20) "Miljögifter finns i alla Sveriges vatten" hur påverkar detta Svenska badvatten [diskutera detta](https://github.com/salgo60/Svenskabadplatser/discussions/71), kan wikidata ha data om detta?
  * 2020-05-19 [SPARQL](https://query.wikidata.org/embed.html#%23defaultView%3AMap%7B%22hide%22%3A%5B%22%3Fbathcoord%22%2C%22%3Flakecoord%22%2C%22%3Fline%22%2C%22%3Fstr%22%2C%22%3Flayer%22%5D%7D%0ASELECT%20%3Fstr%20%3Fbathwater%20%3FbathwaterLabel%20%3Fbathcoord%20%3Flake%20%3FlakeLabel%20%3Flakecoord%20%3Fdist%20%3Fline%20%3FSJOID%20%3Flayer%20WHERE%20%7B%0A%20%20%3Fbathwater%20wdt%3AP6104%20wd%3AQ106774536.%0A%20%20%20%3Fbathwater%20%20wdt%3AP625%20%3Fxx.%0A%20%20%20%3Fbathwater%20%20p%3AP625%20%5B%20a%20wikibase%3ABestRank%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20psv%3AP625%20%5B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoLatitude%20%3Fbathcoordlat%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoLongitude%20%3Fbathcoordlon%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoGlobe%20%3Fglobe%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%5D%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20ps%3AP625%20%3Fbathcoord%0A%20%20%20%20%20%20%20%20%20%20%5D%0A%20%20OPTIONAL%20%7B%20%3Fbathwater%20wdt%3AP605%20%3FNUTSID.%20%7D%0A%20%20%7B%0A%20%20%20%20%3Fbathwater%20wdt%3AP206%20%3Flake.%0A%20%20%20%3Flake%20%20wdt%3AP625%20%3Frr.%0A%20%20%20%20%20%20%20%3Flake%20%20p%3AP625%20%5Ba%20wikibase%3ABestRank%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20psv%3AP625%20%5B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoLatitude%20%3Flat%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoLongitude%20%3Flong%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20wikibase%3AgeoGlobe%20%3Fglobe2%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%5D%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20ps%3AP625%20%3Flakecoord%0A%20%20%20%20%20%20%20%20%20%20%5D%0A%20%20%20%20OPTIONAL%20%7B%20%3Flake%20wdt%3AP761%20%3FSJOID.%20%7D%0A%20%20%7D%0A%20%20%20BIND%28geof%3Adistance%28%3Fbathcoord%2C%20%3Flakecoord%29%20as%20%3Fdist%29%20.%20%0A%20%20%23filter%20%28%3Fdist%20%3E%3D%203%29%0A%20%20BIND%20%28floor%28%3Fdist%2F10%29%2a10%20as%20%3Flayer%29%20%0A%20%20BIND%28CONCAT%28%27LINESTRING%20%28%27%2C%20STR%28%3Fbathcoordlon%29%2C%20%27%20%27%2C%20STR%28%3Fbathcoordlat%29%2C%20%27%2C%27%2C%20STR%28%3Flong%29%2C%20%27%20%27%2C%20STR%28%3Flat%29%2C%20%27%29%27%29%20AS%20%3Fstr%29%20.%0A%20%20BIND%28STRDT%28%3Fstr%2C%20geo%3AwktLiteral%29%20AS%20%3Fline%29%20%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22sv%2Cen%22.%20%7D%0A%7D%0AORDER%20BY%20DESC%28%3Fdist%29%0A)för att se [koppling badvatten, närliggande vatten](https://github.com/salgo60/Svenskabadplatser/issues/60#issuecomment-843576672) i Wikidata
  * 2020-05-18 nya [verktyg](https://github.com/salgo60/Svenskabadplatser/discussions/46#discussioncomment-750114) - [Notebook](https://github.com/salgo60/Svenskabadplatser/blob/main/Jupyter/OSM_Wikidata_Bathwater.ipynb) som kollar antal OSM som har koppling bad i Wikidata i detta projekt 
  * 2020-05-14 testar om vi kan koppla historiska badplats bilder från [Digitaltmuseum och RAÄ](https://wcqs-beta.wmflabs.org/embed.html#%23defaultView%3AImageGrid%0ASELECT%20DISTINCT%20%3Ffile%20%3Fitem%20%3FitemLabel%20%3Fimage%20%3FHis%0AWITH%20%0A%7B%20SELECT%20%3Fitem%20%3FitemLabel%20%3FitemDescription%20%3FHis%20WHERE%0A%20%20%7B%20SERVICE%20%3Chttps%3A%2F%2Fquery.wikidata.org%2Fsparql%3E%20%0A%20%20%20%20%7B%3Fitem%20%20wdt%3AP6104%20wd%3AQ106774536.%0A%20%20%20%20%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22sv%2Cen%22.%20%3Fitem%20rdfs%3Alabel%20%3FitemLabel%20.%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D%20AS%20%25Wikidataitems%0A%0AWHERE%20%0A%7B%20%20INCLUDE%20%25Wikidataitems%20.%0A%20%20%3Ffile%20wdt%3AP180%20%3Fitem.%0A%20%20%7B%7B%3Ffile%20wdt%3AP7847%20%3FDigID%7D%0A%20%20%20UNION%0A%20%20%7B%3Ffile%20wdt%3AP1260%20%3FKsam%7D%7D%0A%20%0A%20%20%3Ffile%20schema%3AcontentUrl%20%3Furl.%20%0A%20%20bind%28iri%28concat%28%22http%3A%2F%2Fcommons.wikimedia.org%2Fwiki%2FSpecial%3AFilePath%2F%22%2C%20wikibase%3AdecodeUri%28substr%28str%28%3Furl%29%2C53%29%29%29%29%20AS%20%3Fimage%29%0A%7D) uppdateras [veckovis](https://diff.wikimedia.org/2020/10/29/sparql-in-the-shadow-of-structured-data-on-commons/)
<!---  * 2020-05-13 feedback in Wikidata by User Latske that we have some errors see [Issue 16](https://github.com/salgo60/Svenskabadplatser/issues/16) -->
  * 2020-05-12 en koll vilken data som levereras till Europeiska miljöbyrån ([Q632988](https://w.wiki/3KWh)) se [Notebook](https://github.com/salgo60/Svenskabadplatser/blob/main/Jupyter/BathWater.ipynb) see [issues/18](https://github.com/salgo60/Svenskabadplatser/issues/18)
  * 2020-05-11 ny egenskap föreslagen [bathingWaterIdentifier](https://www.wikidata.org/wiki/Wikidata:Property_proposal/bathingWaterIdentifier) i Wikidata - **RÖSTA GÄRNA PÅ DETTA** alla kan rösta som registrerat ett [wiki konto](https://sv.wikipedia.org/wiki/Wikipedia:Varf%C3%B6r_skapa_ett_anv%C3%A4ndarkonto%3F)
    * kan ta någon vecka eller aldrig bli av    
    * saknas bra formatteringsURL för karta "[StateOfBathingWaters](https://maps.eea.europa.eu/wab/StateOfBathingWaters/)" hos EU EnvironmentAgency se fråga [tweet](https://twitter.com/salgo60/status/1392032878490488832?s=20)
---
* [Wikidata:Status updates/2021 05 24](https://www.wikidata.org/wiki/Wikidata:Status_updates/2021_05_24)
* This weekend [Wikimedia Remote hack](https://www.mediawiki.org/wiki/Wikimedia_Hackathon_2021) 21-23 may [video channel](https://www.youtube.com/watch?v=VujfdGnUnp0) at 6:22:00 [Lucas Werkmeister do Live SPARQL on Wikidata](https://www.youtube.com/watch?v=VujfdGnUnp0&t=22930s)
   * Nya [verktyg som skapats i helgen](https://etherpad.wikimedia.org/p/wmhackshowcase2021) 
   *  :boom::boom::boom:'''[GISpyssel](https://github.com/salgo60/Svenskabadplatser/labels/GISPyssel)''':boom::boom::boom:
<!---  * Weekend todo listen to [Wikipedia listen.hatnote.com](http://listen.hatnote.com/) or more speedy [Wikidata sounds](http://listen.hatnote.com/#wikidata) --->
---
* [Issues](https://github.com/salgo60/Svenskabadplatser/issues?q=is%3Aissue+) / [closed](https://github.com/salgo60/Svenskabadplatser/issues?q=is%3Aissue+is%3Aclosed)
* [diskussion på GITHUB](https://github.com/salgo60/Svenskabadplatser/discussions)
  * [community.dataportal.se Hjälp folk att bada i sommar med Öppna Data!](https://community.dataportal.se/topic/87/hj%C3%A4lp-folk-att-bada-i-sommar-med-%C3%B6ppna-data-tips-och-hj%C3%A4lp-beh%C3%B6vs)
* [Wikidata egenskaper](https://w.wiki/3Ho8) på uppladdade badplatser
* [Wikidata:WikiProject Sweden/Svenska badplatser](https://www.wikidata.org/wiki/Wikidata:WikiProject_Sweden/Svenska_badplatser)
* [bathingWaterIdentifier](https://www.wikidata.org/wiki/Wikidata:Property_proposal/bathingWaterIdentifier)

**Status:** 2695 badplatser har importerats och kopplats till kommuner se [karta](https://w.wiki/3KP5). Nästa steg är att 
1) länka datat till sjö den finns vid, sociala medier som [Instagram plats id](https://www.wikidata.org/wiki/Property:P4173), [naturreservat](https://w.wiki/3MwX) eller annat badet finns vid
1) försöka hitta kommunens egen beskrivning av badet
1) se om vi kan få svar från Tillgänglighetsdatabasen och skapa en koppling. Fråga hur vi kopplar detta på [bästa sätt till Open Street Map](https://www.facebook.com/groups/osmsweden/permalink/5460751970662625/).
1) skapa en ny egenskap i Wikidata se [bathingWaterIdentifier](https://www.wikidata.org/wiki/Wikidata:Property_proposal/bathingWaterIdentifier)
1) koppla badplats till historiska bilder i ex. [Digitaltmuseum](https://digitaltmuseum.se/search/?q=badplats&aq=owner%3F%3A%22S-OLM%22%20license%3F%3A%22CC%20pdm%22%2C%22CC%20by%22%2C%22CC%20by-sa%22%2C%22zero%22&o=0&n=80) och ladda ned dom (DM har tydlig copyright]

**Lesson learned:** finns tydliga fördningar [2001:100](https://www.riksdagen.se/sv/dokument-lagar/dokument/svensk-forfattningssamling/forordning-2001100-om-den-officiella_sfs-2001-100) vilka myndigheter som är ansvariga för statistik där Havs- och vattenmyndigheten har ett ansvar som sedan i deras regleringsbrev [2011:619](https://www.riksdagen.se/sv/dokument-lagar/dokument/_sfs-2011-619) kanske lite vagt beskrivs som *"miljöövervakning, uppföljning av miljökvalitetsmålen och internationell rapportering"* 
   * [Badvattendirektivet](https://www.svensktvatten.se/om-oss/europeiska-unionen/badvattendirektivet/) 
      * På sidan ["Kontroll av badvattenkvalitet"](https://www.havochvatten.se/overvakning-och-uppfoljning/miljoovervakning/marin-miljoovervakning/kontroll-av-badvattenkvalitet.html) står det *Alla EU-bad finns registrerade på webbplatsen Badplatsen och kommunerna får även registrera övriga bad.*
         * min tolkning är att inga problem finns att ha alla bad i detta register - skall verifieras av Havs- och vattenmyndigheten  
           * jag ser inga problem att ha "alla" bad i Wikidata med koppling Open Street Map 
         * hade en kort dialog med [Mattias Andersson](https://www.linkedin.com/in/mattiasrandersson) hos [Havs- och vattenmyndighetens i Sverige länk](https://www.havochvatten.se/badplatser-och-badvatten.html) och det är dom som "tar ut" NUTS för badplatser och min uppfattning var att det inte finns problem för kommuner att registrera sina badplatser hos dom, min gissning är att kan vi ha denna info om badplatser både EU-bad och övriga så är det en fördel   
   * [2006/7/EG Europaparlamentets och rådets direktiv 2006/7/EG av den 15 februari 2006 om förvaltning av badvattenkvaliteten och om upphävande av direktiv 76/160/EEG](https://eur-lex.europa.eu/legal-content/SV/TXT/PDF/?uri=CELEX:32006L0007&from=EN)
   * [Bathing water management in Europe:Successes and challenges](https://www.eea.europa.eu//publications/bathing-water-quality-2020)
     * [Bathing Mater Quality Information for Public in Europe -Availability and Issue of Integration of Data for the European Level](https://www.researchgate.net/publication/267766499_Bathing_Mater_Quality_Information_for_Public_in_Europe_-Availability_and_Issue_of_Integration_of_Data_for_the_European_Level)

* [European bathing water quality in 2019](https://www.eea.europa.eu/publications/european-bathing-water-quality-in-2019/european-bathing-water-quality-in-2019)
* [eea.europa.eu/Bathingwater](https://discomap.eea.europa.eu/Bathingwater/) - database med alla EU bad
* havochvatten.se [Kontroll av badvattenkvalitet](https://www.havochvatten.se/overvakning-och-uppfoljning/miljoovervakning/marin-miljoovervakning/kontroll-av-badvattenkvalitet.html#:~:text=Kommunerna%20ansvarar%20f%C3%B6r%20%C3%B6vervakningen%20av,och%20rapportering%20till%20EU%2Dkommissionen.)

## Wikidata
![](https://community.dataportal.se/assets/uploads/files/1620115933238-84ccdfe1-eadc-4c49-9e7a-cb030a664a93-image.png). 
* karta [badplatser](https://w.wiki/3KP5) - [video](https://youtu.be/uiHFgYUlHU8)
  * karta om [svensk Wikipedia artikel finns](https://w.wiki/3KP8) 
    * vilka språk finns artiklar om Svenska badplatser med NUTS i Wikipedia - [sparql](https://w.wiki/3GyY) / [lista](https://w.wiki/3Gya)
    * bilder om avbildar dessa badplatser [SPARQL Federation](https://wcqs-beta.wmflabs.org/embed.html#%23defaultView%3AImageGrid%0ASELECT%20DISTINCT%20%3Fitem%20%3FitemLabel%20%3FitemDescription%20%3Fimage%20%3FNUTSid%20%3FNUTS%0AWITH%20%0A%7B%20SELECT%20%3Fitem%20%3FitemLabel%20%3FitemDescription%20%3FNUTSid%20%3FNUTS%20WHERE%0A%20%20%7B%20SERVICE%20%3Chttps%3A%2F%2Fquery.wikidata.org%2Fsparql%3E%0A%20%20%20%20%7B%20%3Fitem%20wdt%3AP31%2Fwdt%3AP279%2a%20wd%3AQ567998.%0A%20%20%20%20%20%20%3Fitem%20wdt%3AP605%20%3FNUTSid%3B%0A%20%20%20%20%20%20%20%20%20%20wdt%3AP17%20wd%3AQ34.%0A%20%20%20%20%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22sv%2Cen%22.%20%3Fitem%20rdfs%3Alabel%20%3FitemLabel%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20schema%3Adescription%20%3FitemDescription%20.%7D%0A%20%20%20%20%20BIND%28URI%28CONCAT%28%22https%3A%2F%2Fbadplatsen.havochvatten.se%2Fbadplatsen%2Fkarta%2F%23%2Fbath%2F%22%2C%3FNUTSid%29%29%20AS%20%3FNUTS%29%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D%20AS%20%25Wikidataitems%0A%0AWHERE%20%0A%7B%20%20INCLUDE%20%25Wikidataitems%20.%0A%20%20%3Ffile%20wdt%3AP180%20%3Fitem.%0A%20%20%3Ffile%20schema%3AcontentUrl%20%3Furl.%20%0A%20%20bind%28iri%28concat%28%22http%3A%2F%2Fcommons.wikimedia.org%2Fwiki%2FSpecial%3AFilePath%2F%22%2C%20wikibase%3AdecodeUri%28substr%28str%28%3Furl%29%2C53%29%29%29%29%20AS%20%3Fimage%29%0A%7D) - OBS [är en beta](https://diff.wikimedia.org/2020/10/29/sparql-in-the-shadow-of-structured-data-on-commons/)
  * karta [saknar bild](https://w.wiki/3Gv$) 
    * badplatser [utan bild med länk Wikishootme](https://w.wiki/3LUz) - mer om [Wikishootme](https://meta.wikimedia.org/wiki/WikiShootMe)
  * karta [saknar ligger vid vattenområde](https://w.wiki/3LUs) - egenskap ligger vid vattenområde = [Property:P206](https://www.wikidata.org/wiki/Property:P206) 
  * karta [saknar "plats"](https://w.wiki/3Gw9) - egenskap plats e.g. Naturreservat = [Property:P276](https://www.wikidata.org/wiki/Property:P276) 
    * bra [karta att hitta svenska Naturreservat i Wikidata](https://map.wikilovesearth.se/#59.44228,18.03698,13z)  
  * karta [saknar "placerad på landform"](https://w.wiki/3GwC) - egenskap placerad på landform e.g. ö = [Property:P706](https://www.wikidata.org/wiki/Property:P706) 
  * karta saknar [Instagramplatsid](https://w.wiki/3Gkw) - [Property:P4173](https://www.wikidata.org/wiki/Property:P4173)
    * karta saknar [HashTag](https://w.wiki/3Gom) - [Property:P2572](https://www.wikidata.org/wiki/Property:P2572)
    * karta saknar [Facebook placeid](https://w.wiki/3Gon) - [Property:P1997](https://www.wikidata.org/wiki/Property:P1997)
  * [Wikidata egenskaper dessa badplatser har](https://w.wiki/3LV2)
* karta [hundbadplatser världen](https://w.wiki/3Gkg)
   * utan [koordinat](https://w.wiki/3Gkh)
## Feedback Havs- och vattenmyndighetens i Sverige
Magnus Sälgö 0705937579 - salgo60@msn.com
1) ange vid vilket vatten bad finns gärna med Sjöid [Property:P761](https://www.wikidata.org/wiki/Property:P761) eller Wikidata objekt
1) ange om badet finns på en ö eller liknande med samma som Wikidata objekt
### Fel i datat
see [Issues](https://github.com/salgo60/Svenskabadplatser/issues?q=is%3Aissue+) / [closed](https://github.com/salgo60/Svenskabadplatser/issues?q=is%3Aissue+is%3Aclosed)

## Tillgänglighetsdatabasen <-> badstränder
För att alla skull kunna använda exem pelvis badstränder behöv s tillgänglighetsinformation en variant är Tillgänglighatesdatabasen (dåligt använd men känns som den har stor potential, tveksam dock om det är bra maskinläsbardata) en annan är exempelvis [Open Street Map](https://wiki.openstreetmap.org/wiki/Accessibility)
* [Video om Tillgänglighetsdatabasen](https://vimeo.com/325190731)
Finns idag ingen koppling Wikidata till denna database men skapar en "fusk variant" 
* [Tillgänglighetsdatabasen](https://www.t-d.se/)
* [Wikidata <-> Tillgänglighetsdatabasen](https://w.wiki/3Gou)
  * visar de bad jag hittat i Tillgänglighetsdatabasen och kopplat i Wikidata OBS alla har inte NUTS
  * vilka kommuner har vi hittat flest [badplatser i Tillgänglighetsdatabasen](https://w.wiki/3JR$) / [karta](https://w.wiki/3JSK)
    * samma men [test visa geojson yta](https://w.wiki/3JU5) - verkar som Wikidata yta för många kommuner.... (test [vilka som har yta](https://w.wiki/3JUC))
* exempel [wheelmap.org](https://wheelmap.org/search) hur man borde kunna hitta badplatser med rätt tillgänglighet
  * <em>Wheelmap is a map for finding wheelchair accessible places. The map works similar to Wikipedia: Anyone can contribute and mark public places around the world according to their wheelchair accessibility. The criteria for marking places is based on a simple traffic light system:</em> [FAQ](https://news.wheelmap.org/en/FAQ/)
## Entity schema - definierar vilka egenskaper som skall finnas i Wikidata för dessa objekt med [ShEx](https://www.wikidata.org/wiki/Wikidata:WikiProject_Schemas)
för att data skall bli mer konsistent så skapas olika schema se [video](https://www.youtube.com/watch?v=ZHdjwbLgzvE)
* [EntitySchema:E304](https://www.wikidata.org/wiki/EntitySchema:E304) Hundbadplatser
* [EntitySchema:E305](https://www.wikidata.org/wiki/EntitySchema:E305) Svenskaplatser med NUTS
## API 

* [SMHI Open Data API Docs](https://opendata.smhi.se/apidocs/metfcst/parameters.html)
* [Badkartan](https://www.tedvalentin.com/2009/06/ett-api-for-mina-kartsajter.html)
* [mediawiki API:RecentChanges](https://www.mediawiki.org/wiki/API:RecentChanges) se exempel [listen.hatnote.com](http://listen.hatnote.com/#wikidata) / [wikidata change stream](https://wikidata-todo.toolforge.org/rcvis.html)
* [viss.lansstyrelsen.se/API](https://viss.lansstyrelsen.se/API)

## [Open Data Badplatser](https://www.dataportal.se/sv/datasets?p=1&q=Badplatser&s=2&t=20&f=&rt=dataset%24esterms_IndependentDataService%24esterms_ServedByDataService)
Nedan den öppen data vi hittar idag som tyvärr inte är kopplad med NUTS --> data silos och svårt att använda
* [Uppsala kommun](https://opendata.uppsala.se/datasets/aadc5420e8884d32b2efe0d10fbfdfe5_0/geoservice?geometry=15.925%2C59.642%2C19.874%2C60.125)
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad 
* [Södertälje](https://www.sodertalje.se/kommun-och-politik/for-medborgare/oppna-data/oppen-data/#esc_entry=500&esc_context=1)
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * kontaktat se [issue 14](https://github.com/salgo60/Svenskabadplatser/issues/14)
* [Karlskrona kommun](https://service.karlskrona.se/FileStorageArea/Documents/bad/swimAreas.geojson)
  * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad
* [Gävle kommun](https://www.gavle.se/kommunens-service/kommun-och-politik/statistik-fakta-och-oppna-data/oppna-data/datakatalog/data/#esc_entry=234&esc_context=1)
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
  * behöver nyckel [länk](http://opendata.linkoping.se/)
    * gist med [Linköping WaterQualityObserved](https://gist.github.com/salgo60/3c9b28ca6281ea9fc234baea0776de86) 
      * saknar [NUTS](https://sv.wikipedia.org/wiki/Nomenklaturen_f%C3%B6r_statistiska_territoriella_enheter)
  * ej kontaktad 
* .....

## [Kontakter](#havvatten)
* [Mattias Andersson](https://www.linkedin.com/in/mattiasrandersson) badvatten@havochvatten.se [Enheten för utveckling och systemförvaltning](https://www.havochvatten.se/om-oss-kontakt-och-karriar/organisation/avdelningen-for-digitalisering/enheten-for-utveckling-och-systemforvaltning.html) email: tel: 010-6986286
* [Stina Lindqvist](https://www.havochvatten.se/om-oss-kontakt-och-karriar/organisation/avdelningen-for-miljoanalys/miljoovervakningsenheten.html) Miljöövervakningsenheten 010-6986454
