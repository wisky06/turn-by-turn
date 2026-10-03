# Couverture mobile 4G (tuiles)

Tuiles de couverture mobile 4G utilisées par l'application Rally Notes pour signaler un « réseau inégal » le long des
spéciales d'un rallye. Zone traitée : départements 04, 06 et 83 (Alpes-de-Haute-Provence, Alpes-Maritimes, Var).

- **Source** : Arcep, « Mon Réseau Mobile », cartes de couverture théorique 4G (Orange, SFR, Bouygues Telecom, Free
  Mobile), trimestre **2026 T2**. Données publiées par l'Arcep sous Licence Ouverte (Etalab) —
  https://data.arcep.fr/mobile/couvertures_theoriques/ · https://www.data.gouv.fr/datasets/mon-reseau-mobile
- **Contours des départements** : communes de geo.api.gouv.fr (IGN / INSEE), pour distinguer « sans couverture » de
  « hors zone traitée ».
- **Traitement** : modifié par Rally Notes — les polygones de couverture « très bonne » et « bonne » de chaque
  opérateur sont réduits en une grille de 0,0025° (environ 280 m × 200 m) ; chaque case vaut le nombre d'opérateurs
  (0 à 4) qui y proposent une bonne couverture 4G, ou « . » hors des départements traités.
- **Format** : un fichier `<latitude>_<longitude>.json` par carré de 1° (coin sud-ouest), au format
  `{ v, quarter, lat, lon, cell, cols, rows, data }`, `data` étant `cols × rows` caractères, ligne par ligne du sud
  au nord et d'ouest en est.
- **Limites** : ce sont des simulations déclarées par les opérateurs, optimistes en forêt et en fond de vallée. Elles
  n'engagent pas les opérateurs et ne garantissent pas le réseau réel.
