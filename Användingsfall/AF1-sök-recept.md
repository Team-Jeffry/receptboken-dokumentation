## <u>Sök recept</u>
### Kap.1 - Formulär 
| Fält                       	| Innehåll                     	| Typ av input                             	|
|----------------------------	|------------------------------	|------------------------------------------	|
| Receptnamn 	| Namnet på receptet          	| Sträng, max 50 tecken, ej obligatorisk      	|
| Tid (minuter)        	| Tillagningstid     	| Int, ej obligatorisk      	|
| Kategori          	| Fyller i namnet på en kategori           	| React tags, ej obligatorisk      	|

### Kap.2 - Normalflöde
N1. Användaren navigerar till sök recept. <br>
N2. Systemet visar formulär enligt kap.1. <br>
N3. Användaren fyller i formuläret och klickar på sök. <br>
N4. Systemet validerar formuläret och visar feedback för användaren. <br>
N5. Användningsfall avslutat. <br>

### Kap.3 - Alternativflöde
N3. Användaren adderar kategorier till sökningen. <br>
N4. Systemet adderar kategorin till sökningen. Flödet fortsätter i Kap.2.N3 tills alla önskade kategorier är angivna. Flödet fortsätter i Kap.2.N4. <br>
