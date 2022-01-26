## Exercice du 26 janvier 2022 / Antoine Courtin  

### Faire afficher sur une carte, les lieux de conservation pour les sculptures d'Auguste Rodin uniquement conservées aux Etat-Unis 

#### La requette Wikidata Query 
````sparql
#defaultView:Map
SELECT ?item ?itemLabel  ?image ?lieudeconservation ?coord WHERE { 
   ?item wdt:P170 wd:Q30755.
  ?item wdt:P31 wd:Q860861 .
  ?lieudeconservation wdt:P17 wd:Q30.
  ?item wdt:P18 ?image .
  ?item wdt:P276 ?lieudeconservation.
 ?lieudeconservation wdt:P625 ?coord .

````
 
  
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en ". }
}

#### La carte géographique  

<iframe style="width: 80vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%23defaultView%3AMap%0ASELECT%20%3Fitem%20%3FitemLabel%20%3Fimage%20%3Flieudeconservation%20%3Fcoord%20WHERE%20%7B%0A%20%20%3Fitem%20wdt%3AP170%20wd%3AQ30755.%0A%20%20%3Fitem%20wdt%3AP31%20wd%3AQ860861.%0A%20%20%3Fitem%20wdt%3AP17%20wd%3AQ30.%0A%20%20%3Fitem%20wdt%3AP18%20%3Fimage.%0A%20%20%3Fitem%20wdt%3AP276%20%3Flieudeconservation.%0A%20%20%3Flieudeconservation%20wdt%3AP625%20%3Fcoord.%0A%20%20%7D" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>
