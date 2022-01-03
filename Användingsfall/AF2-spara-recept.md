## <u>Spara recept</u>
### Kap.1 - Formulär 
| Fält                       	| Innehåll                     	| Typ av input                             	|
|----------------------------	|------------------------------	|------------------------------------------	|
| Receptnamn 	| Namnet på receptet          	| String, max 50 tecken, obligatorisk      	|
| Kategori          	| Dropdown fält på existerande kategorier            	| Dropdown, max 50 tecken, obligatorisk      |
| Beskrivning         	| Beskrivning av receptet     	| CLOB, obligatorisk      	|
| Tid (minuter)        	| Tillagningstid     	| int, obligatorisk      	|
| Ingrediens              	| Namnet på en ingrediens           	| Sträng, max 50 tecken, obligatorisk      	|
| Instruktioner        	| Instruktioner till receptet    	| CLOB, obligatorisk      	|


### Kap.2 - Normalflöde
N1. Användaren navigerar till spara recept. <br>
N2. Systemet visar formulär enligt kap.1. <br>
N3. Användaren fyller i formuläret och klickar på sök. <br>
N4. Systemet validerar formuläret och visar recept som matchar informationen i angivna fält. <br>
N5. Användningsfall avslutat. <br>

### Kap.3 - Felflöde
#### ***F1 - Fel format (inträffar i N3)***
F1.1 Systemet visar feedback att något är fel. <br>
F1.2 Flödet fortsätter i N1. <br>