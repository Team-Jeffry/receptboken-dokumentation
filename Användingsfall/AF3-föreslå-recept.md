## <u>Föreslå recept</u>
### Kap.1 - Formulär 
| Fält                       	| Innehåll                     	| Typ av input                             	|
|----------------------------	|------------------------------	|------------------------------------------	|
| Ingrediens              	| Namnet på en ingrediens           	| React tags, obligatorisk      	|


### Kap.2 - Normalflöde
N1. Användaren navigerar till föreslå recept. <br>
N2. Systemet visar formulär enligt kap.1. <br>
N3. Användaren adderar ingredienser till sökningen. <br>
N4. Systemet adderar ingrediensen till sökningen. <br>
N5. Användaren klickar på föreslå. <br>
N6. Systemet visar recept som matchar informationen i angivet fält. <br>
N7. Användningsfall avslutat. <br>

### Kap.3 - Alternativflöde (*inträffar i Kap.2.N3*)
N3. Användaren adderar ingredienser till sökningen. <br>
N4. Systemet adderar ingrediensen till sökningen. Flödet fortsätter i Kap.2.N3 tills alla önskade ingredienser är angivna. Flödet fortsätter i Kap.2.N5. <br>
