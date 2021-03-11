1. How many persons had the civil rights?


SELECT ?civilRight (COUNT(?civilRights) as ?counter_cvR)
WHERE {
	?Individual rdf:type vcard:Individual.
	?Individual transraz:civilRights ?civilRights
}
GROUP BY ?civilRights
ORDER BY DESC (? counter_cvR)


2. What were the most common occupations in 1910?

SELECT ?name (COUNT(?name) as ?frequency)
WHERE {
?Individual schema:hasOccupation ?Occupation.
?Occupation rdfs:label ?name
}
GROUP BY ?name
ORDER BY DESC (?frequency)

3. What were the most common first names in 1910?

SELECT ?givenName  (COUNT(?givenName) as ?frequency)
WHERE {
  ?Individual vcard:givenName ?givenName .
}
GROUP BY ?givenName
ORDER BY DESC (?frequency)

4. What were the most common last names in 1910?

SELECT ?familyName  (COUNT(?familyName) as ?frequency)
WHERE {
  ?Individual vcard:familyName ?familyName .
}
GROUP BY ?familyName
ORDER BY DESC (?frequency)

5. Where were most of the companies located?

SELECT ?Streetname (COUNT(?Streetname) as ?frequency)
WHERE {
?Organization rdf:type vcard:Organization.
?Organization vcard:hasAddress ?AddressID.
?AddressID vcard:hasStreetAddress ?Street.
?Street rdfs:label ?Streetname 
}
GROUP BY ?Streetname
ORDER BY DESC(?frequency)

6. What was the most populated street? 

SELECT ?Streetname (COUNT(?Streetname) as ?frequency)
WHERE {
?Individual rdf:type vcard:Individual.
?Individual vcard:hasAddress ?AddressID.
?AddressID vcard:hasStreetAddress ?Street.
?Street rdfs:label ?Streetname 
}
GROUP BY ?Streetname
ORDER BY DESC(?frequency)

