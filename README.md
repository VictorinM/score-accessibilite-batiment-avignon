# Score d'accessibilité à l'échelle du bâtiment à Avignon

Projet personnel de Victorine Maximilienne Djetcheu Toko.

Ce projet mesure ce qu'on peut atteindre à pied dans Avignon, et en combien de minutes. Il construit le réseau piéton de la ville, calcule le temps de marche jusqu'aux services du quotidien, pharmacie, école, commerce, santé et parc, et donne à chaque bâtiment un score d'accessibilité. Il trace aussi les bandes de marche à 5, 10 et 15 minutes depuis le centre.

## La méthode

Je m'appuie sur une méthode classique d'analyse d'accessibilité réseau, que j'ai mise en œuvre sur ma ville avec mon propre code et mes propres choix, pour la maîtriser et pouvoir la réutiliser sur n'importe quel territoire.

## Ce que ça utilise

Python, osmnx pour les données OpenStreetMap, pandana pour les calculs d'accessibilité sur le réseau, geopandas, networkx et matplotlib. Les arrêts de bus viennent du GTFS du réseau Orizo.

## Comment le lancer

Créer un environnement avec les bibliothèques, par exemple avec conda.

```
conda install -c conda-forge osmnx pandana geopandas networkx matplotlib
```

Ouvrir le notebook accessibilite_avignon.ipynb et lancer les cellules dans l'ordre. Laisser DEV_MODE sur True pour un test rapide sur le centre, puis le passer sur False pour tout Avignon. Les arrêts Orizo sont en option, pour les afficher, télécharger le GTFS d'Orizo sur transport.data.gouv.fr et le mettre dans un dossier gtfs_orizo à côté du notebook.

## Mes choix

Vitesse de marche de 4,8 kilomètres par heure, projection Lambert 93 pour des distances justes, seuils à 5, 10 et 15 minutes.

## Les limites

Les données viennent d'OpenStreetMap, donc une aménité oubliée n'est pas comptée. Et on mesure la marche sur le réseau, pas le confort réel du trajet.

## Auteur

Victorine Maximilienne Djetcheu Toko. Projet construit avec des outils open source.
