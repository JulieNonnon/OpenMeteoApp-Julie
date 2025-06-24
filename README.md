# Projet de candidature : Mise à jour Open Meteo App

## Scénario

Vous êtes développeur web pour le compte d’une agence web. Votre agence a signé un contrat pour le développement d’interfaces météo à destination des usagers du réseau de transport en commun de plusieurs villes de taille moyenne en France. Les écrans seront intégrés aux écrans d’information dans les stations et dans les transports.
Les écrans doivent être programmés avec les technologies web, embarquées dans la webview du système des écrans de la compagnie de transports en commun de la ville.
Par chance vous avez un projet existant disponible. 
Mais celui-ci utilise l’API REST d’open weather map. Hors vous devez utiliser l’API d’open meteo à la place.
De plus, l’interface ne doit plus inclure de moteur de recherche pour la localisation de l’information météo. Mais, elle doit inclure un fichier de configuration (JSON par exemple) dans lequel l’information de la ville concernée sera entrée par l’entreprise de transport, et utilisée par votre code pour récupérer les bonnes données météo.

Le dépôt git du projet existant, votre point de départ :
GitHub - madzadev/weather-app: ⛅ Check the current weather in any city on the planet.
https://github.com/madzadev/weather-app

## Livrables

Les fichiers source seront partagés via l’url d’un dépôt Git accessible en ligne (Github, Gitlab...).

https://github.com/JulieNonnon/OpenMeteoApp-Julie

## L’organisation de votre travail

✨Mettre à jour l’application
● Intégrer le changement d’API en faveur d’open meteo :
○ prendre en main la documentation et le fonctionnement de l’API open meteo,
○ intégrer les changements dans la requête, 
○ intégrer les mises à jour nécessaires pour le traitement des données et l’affichage du résultat, en fonction du format de réponse de l’API d’open meteo.

● Intégrer l’évolution pour ne plus avoir de recherche de la ville mais une localisation pré-configurée dans un fichier de configuration.
● Intégrer le rafraîchissement des données toutes les heures.

✨Tester l’application et livrer
● validez, puis livrez votre projet sur un dépôt Git en ligne.

## Critères de qualité

✨Critères pour pour le projet

● Les consignes sont respectées dans leur intégralité,
● la structure de l’application existante est respectée,
● les règles css sont fonctionnelles et effectivement liées à la page html.
→ il n’y a pas de critères concernant les visuels, le design et la mise en page. La ville concernée et les informations météo doivent cependant être lisibles sans doute possible,
● les données météo récupérées sont effectivement celle de la ville configurée dans le fichier dédié,
● les données météo sont correctement restituées depuis l’interface,
● le rafraîchissement des données météo toutes les heures est intégré au programme,
● les données sont effectivement rafraîchies toutes les heures.

✨Critères pour le jour J

● Le candidat décrit les tâches qu'il a effectuées pour parvenir à un résultat,
● le⸱a candidat⸱e explique le fonctionnement logique de la récupération des données météo,
● le⸱a candidat⸱e explique les règles d’intégration des interfaces et des données météo,
● le⸱a candidat⸱e a identifié les améliorations possibles,
● le⸱a candidat⸱e a identifié comment ces améliorations pourraient être implémentées concrètement et les apprentissages qu’il ou elle devrait faire pour y arriver.

## Organisation et préparation :

● ✅ Préparation en amont via un Trello, avec tâches à effectuer :
https://trello.com/b/xugCrEWb/open-meteo-api

● ✅ Clonage projet d'origine de madzadev
● ✅ Familiarisation avec projet d'origine de madzadev
● ✅ Consultation README du projet
● ✅ Etude de la doc Open Meteo ( + doc Geocode pour géolocalisation )
● ✅ Etude de la doc Open Weather ( ancienne API à remplacer )
● ✅ Lancement projet et repérage des différents composants de l'application
● ✅ Liste des données appelées par Open Weather
● ✅ Recherche de donnée équivalente dans Open Meteo
● ✅ Mise à jour de la requête vers l'API Open Meteo (ne nécessite pas de clé, la config de l'environnement n'est pas utile), + ajustement du fichier data.js
● ✅ Ajustement de l'index.js et des composants concernés par la mise à jour des données
● ✅ Préparation d'un mapper pour remplacer les pictogrammes fournis par Open Weather par les pictogrammes fournis par Weather Icons, selon le code météo appelé
● ✅ Test du remplacement de l'API avec la fonction recherche initialement présente
● ✅ Remplacement de la fonction recherche avec un fichier config.json (comprenant une ville prédéfinie), et màj du composant MetricsBox pour enlever la fonctionnalité de recherche
● ✅ Ajustement du helper.js pour récupération du jour selon fuseau horaire
● ✅ Ajustement du converteur.js pour conversion donnée horaires (en int pour Open Weather, en string ISO pour Open Meteo)
● ✅ Test de l'application puis livraison via guthub


________________________________________________________

## Features

1. User's ability to search cities

2. Current local time and date

3. Temperatures and humidity

4. Wind speed and direction

5. Sunrise and sunset times

6. Metric vs Imperial system

7. Error handling and loading info

## Installation

1. `git clone https://github.com/madzadev/weather-app.git`

2. `cd weather-app`

3. `npm install`

4. Log-in to [Openweathermap.com](https://openweathermap.org/)

5. Create an API key

6. `cp .env.example .env.local`

7. Paste API key for `OPENWEATHER_API_KEY`

8. `npm run dev`

## Contributions

Any feature requests and pull requests are welcome!

## License

The project is under [MIT license](https://choosealicense.com/licenses/mit/).
