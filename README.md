# TRANSRAZ

[TRANSRAZ](https://www.fiz-karlsruhe.de/en/forschung/transraz) is an ongoing research project aiming at connecting heterogeneous historical data collections to an architectural 3D virtual research environment (VRE) using KGs. 
The overall goal is to enable the exploration of the historic city of Nuremberg in different time periods ranging from the Middle Ages to the 21st century.

## Nuremberg Address Knowledge Graph

This repository contains resources of ongoing work introduced in the poster paper:
```
Oleksandra Bruns, Tabea Tietz, Mehdi Ben Chaabane, Manuel Portz, Felix Xiong, Harald Sack. 
The Nuremberg Address Knowledge Graph. 
Submitted to ESWC 2021 Poster&Demos.
```
### Abstract

The research of European history cross various time layers gives insights about the development of the European cultural identity. Nuremberg as one of the great European metropolises during the Middle Ages experienced a number of transformations throughout the centuries. Within the TRANSRAZ research project, Nuremberg and the development of its architecture and culture is recreated from the 17th to the 21st century. It will be available for researchers and the public by means of an interactive 3D environment. Goal of this poster paper is to discuss the ongoing work of connecting heterogeneous historical data from sources previously hidden in archives to the 3D model using knowledge graphs for a scientifically accurate exploration of Nuremberg. The contribution of this paper is the Nuremberg Address Knowledge Graph (NA-KG) which contains information of people and organizations in Nuremberg and was created from unstructured data of the Nuremberg address book of 1910.

#### Classes

[vcard:Individual](http://www.w3.org/2006/vcard/ns#Individual)

[vcard:Address](http://www.w3.org/2006/vcard/ns#Address)

[vcard:Organization](http://www.w3.org/2006/vcard/ns#Organization)

[schema:Occupation](https://schema.org/Occupation)

[dbo:Street](https://dbpedia.org/ontology/Street)


#### Object Properties


[dcterms:hasPart](http://purl.org/dc/terms/hasPart)

   *Inverse of* dcterms:isPartOf   
   *Domain* vcard:Address   
   *Range* dbo:Street   


[dcterms:isPartOf](http://purl.org/dc/terms/isPartOf)

   *Inverse of* dcterms:hasPart   
   *Domain* dbo:Street   
   *Range* vcard:Address   


[schema:hasOccupation](http://schema.org/hasOccupation)

   *Domain* vcard:Individual   
   *Range* schema:Occupation   


[vcard:hasAddress](http://www.w3.org/2006/vcard/ns#hasAddress)

   *Domain* vcard:Individual, vcard:Organization   
   *Range* vcard:Address 


[dbo:owingOrganization](https://dbpedia.org/ontology/owningOrganisation)

   *Inverse of* transraz:ownedBy   
   *Domain* vcard:Individual   
   *Range* vcard:Organization


[transraz:ownedBy](http://transraz/addressbook#ownedBy)

   *Inverse of* dbo:owingOrganization   
   *Domain* vcard:Organization   
   *Range* vcard:Individual


#### Datatype Properties


[transraz:abbreviatedName](http://transraz/addressbook#abbreviatedName)

   *Domain* schema:Occupation, vcard:Individual   
   *Range* rdfs:Literal


[transraz:buildingNumber](http://transraz/addressbook#buildingNumber)

   *Domain* dbo:Street   
   *Range* rdfs:Literal


[transraz:civilRights](http://transraz/addressbook#civilRights)

   *Domain* vcard:Individual   
   *Range* xsd:boolean


[transraz:floor](http://transraz/addressbook#floor)

   *Domain* vcard:Address   
   *Range* rdfs:Literal


[transraz:industry](http://transraz/addressbook#industry)

   *Domain* vcard:Organization   
   *Range* rdfs:Literal


[transraz:partOfHouse](http://transraz/addressbook#partOfHouse)

   *Domain* vcard:Address   
   *Range* rdfs:Literal


[transraz:yard](http://transraz/addressbook#yard)

   *Domain* vcard:Address   
   *Range* rdfs:Literal


[vcard:family-name](http://www.w3.org/2006/vcard/ns#family-name)

   *Domain* vcard:Individual   
   *Range* rdfs:Literal


[vcard:given-name](http://www.w3.org/2006/vcard/ns#given-name)

   *Domain* vcard:Individual   
   *Range* rdfs:Literal


[vcard:organization-name](http://www.w3.org/2006/vcard/ns#organization-name)

   *Domain* vcard:Organization   
   *Range* rdfs:Literal



### Access

- The Nuremberg Address Knowledge Graph (NA-KG) can be accessed [here](https://github.com/ISE-FIZKarlsruhe/Transraz/blob/main/NurembergAddressKG/NA-KG.ttl)
- Example queries can be accessed [here](https://github.com/ISE-FIZKarlsruhe/Transraz/blob/main/NurembergAddressKG/SPARQL_Queries/Queries.md)

## Prior Publications about TOPORAZ and TRANSRAZ
```
Tabea Tietz, Oleksandra Bruns, Sandra Göller, Matthias Razum, Danilo Dessi, Harald Sack. 
Knowledge Graph enabled Curation and Exploration of Nuremberg’s city heritage [to be published]. 
In:Proc. of the Conf. on Digital Curation Technologies. CEUR-WS (2021)

Matthias Razum, Sandra Göller, Harald Sack, Tabea Tietz, Oleksandra Vsesviatska, Gerhard Weilandt, Marc Grellert, Torben Scharm. 
Toporaz: Ein digitales Raum-Zeit-Modell für vernetzte Forschungam Beispiel Nürnberg. 
Information-Wissenschaft & Praxis71(4), 185–194 (2020)
```

## Acknowledgement 
This work is funded by the Leibniz Association under project number SAW-2020-FIZ KA-4-Transraz. 
