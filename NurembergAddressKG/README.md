# Nuremberg Address Knowledge Graph

The Nuremberg Address Knowledge Graph is part of the ongoing TRANSRAZ project. It contains 860K triples on persons and organizations in the Nuremberg address book of 1910. This contribution is valuable for historical scientists and digital humanists intending to study citizens' names, historical occupations as well as companies and their distribution in Nuremberg. After its integration into the 3D VRE of TRANSRAZ, the address book data can be explored by researchers as well as the general public. 

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




## Access

- The NA-KG is available [here](https://github.com/ISE-FIZKarlsruhe/Transraz/blob/main/NurembergAddressKG/NA-KG.ttl). 
- Example SPARQL Queries are available [here](https://github.com/ISE-FIZKarlsruhe/Transraz/blob/main/NurembergAddressKG/SPARQL_Queries/Queries.md).

