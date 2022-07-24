# Azure-Data-Factory
Demonstration of an Azure Data Factory study project

HAMKin IT-tradenomi muuntokoulutuksessa "Tiedon analysointi"-kurssilla tutustuimme Azureen ja tein viikkotehtävänä videolla kuvatun Azure Data Factoryn, jossa käsiteltiin Covid19-dataa (lähde: https://github.com/owid/covid-19-data/tree/master/public/data).

Tässä repossa on tallennettuna Azure Resource Manager template Data Factorystani, sekä video, jolla päällisin puolin esittelen tuotokseni. 

Kuvaus & toimintaperiaate:
- Tarvittavat resurssit olivat SQL server, SQL tietokanta, Storage Account sekä itse Data Factory.
- Kopioidaan ensin dataa HTTP-lähteestä Storage Accountin Containeriin
- DataFlowPipelinessa muokataan dataa suodattamalla haluttu data maanosan mukaan ja sitten tiputtamalla turhia sarakkeita pois ja uudelleennimeämällä muutama sarake. Muodostettiin uusi CSV-tiedosto samaan Containeriin.
- Prosessoidun datan vienti CSV-tiedostosta Azure SQL -tietokantaan (Tietokantataulu luotiin Query editorilla ennen tietojen vientiä)
