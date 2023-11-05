# JUMP2DIGITAL
# 1. Introducció: Presentació del conjunt de dades i de les variables seleccionades.
S'han escollit dos conjunts de dades. El primer inclou informació sobre el lloguer mitjà mensual, tant per superfície com per metre quadrat, en diferents districtes ("Nom_Districte") i barris ("Nom_Barri") durant l'any 2017, detallat per trimestres ("Trimestre"). El segon conjunt de dades conté informació sobre els diferents nivells de soroll ocasionats per diverses fonts en cada barri de Barcelona. Les columnes més rellevants són "Concepte", que especifica l'origen del soroll, i "Rang Soroll" i "Valor", que determinen la quantitat de soroll en un rang específic de decibels. Algunes de les fonts de soroll són el trànsit diürn i nocturn, els vianants, la indústria, els ferrocarrils de la Generalitat, entre d'altres.

Les variables seleccionades dels dos conjunts de dades són: "Codi_Districte", "Codi_Barri", "Lloguer mitjà mensual", "Lloguer mitjà m2", "Concepte" (font de soroll), "Rang de soroll" i el "Valor del soroll".

# 2. Depuració de dades: Descripció detallada de les tècniques de preprocessament aplicades i els criteris d'avaluació utilitzats.
La depuració de dades ha consistit en:
- Gestionar els valors nuls a la columna "Lloguer_mitja" del primer conjunt de dades.
- Crear dues noves columnes, "Lloguer_mitja_mensual" i "Lloguer_mitja_m2", i eliminar la columna "Lloguer_mitja". S'han utilitzat visualitzacions com bar plots i scatter plots per a una millor comprensió dels conjunts de dades.
- Unificar en un únic conjunt de dades la informació dels preus de lloguer i dels nivells de soroll a la ciutat de Barcelona.
- Convertir la columna de percentatge de tipus string a tipus int.
- Produir visualitzacions finals.

# 3. Resultats: Presentació dels resultats obtinguts.
Els resultats principals són visualitzacions dels diferents preus de lloguer per barri i per districte de la ciutat de Barcelona, així com visualitzacions de matrius de correlació entre els nivells de soroll als barris i els preus de lloguer. També s'ha desenvolupat una funció que, donat un barri, retorna les fonts de soroll presents en cada rang, per identificar els principals causants en funció del barri.

# 5. Conclusions: Principals inferències derivades dels resultats obtinguts.
La inferència principal és la correlació existent entre els nivells de soroll als barris i el preu per metre quadrat. S'ha trobat una correlació positiva del 40% entre els nivells de soroll de 40-45 dB i el preu per m2. En canvi, s'ha obtingut una correlació negativa del 40% amb el preu per m2 quan el soroll està en un rang de 60-65 dB. Això indica que, mentre el soroll no superi els 60-65 dB, el preu no es veu afectat significativament; però en aquests nivells, la relació esdevé negativa, suggerint que el preu per m2 disminueix en barris amb nivells de soroll elevats.
