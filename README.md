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
<ul>
<li>Intégrer le changement d’API en faveur d’open meteo :</li>
○ prendre en main la documentation et le fonctionnement de l’API open meteo,
○ intégrer les changements dans la requête, 
○ intégrer les mises à jour nécessaires pour le traitement des données et l’affichage du résultat, en fonction du format de réponse de l’API d’open meteo.

<li>Intégrer l’évolution pour ne plus avoir de recherche de la ville mais une localisation pré-configurée dans un fichier de configuration.</li>
<li>Intégrer le rafraîchissement des données toutes les heures.</li>
</ul>

✨Tester l’application et livrer
<ul>
<li>validez, puis livrez votre projet sur un dépôt Git en ligne.</li>
</ul>

## Critères de qualité

✨Critères pour pour le projet

<ul>
<li>Les consignes sont respectées dans leur intégralité,</li>
<li>la structure de l’application existante est respectée,</li>
<li>les règles css sont fonctionnelles et effectivement liées à la page html.</li>
<li> → il n’y a pas de critères concernant les visuels, le design et la mise en page. La ville concernée et les informations météo doivent cependant être lisibles sans doute possible,</li>
<li>les données météo récupérées sont effectivement celle de la ville configurée dans le fichier dédié,</li>
<li>les données météo sont correctement restituées depuis l’interface,</li>
<li>le rafraîchissement des données météo toutes les heures est intégré au programme,</li>
<li>les données sont effectivement rafraîchies toutes les heures.</li>
</ul>

✨Critères pour le jour J

<ul>
<li>Le candidat décrit les tâches qu'il a effectuées pour parvenir à un résultat,</li>
<li>le⸱a candidat⸱e explique le fonctionnement logique de la récupération des données météo,</li>
<li>le⸱a candidat⸱e explique les règles d’intégration des interfaces et des données météo,</li>
<li>le⸱a candidat⸱e a identifié les améliorations possibles,</li>
<li>le⸱a candidat⸱e a identifié comment ces améliorations pourraient être implémentées concrètement et les apprentissages qu’il ou elle devrait faire pour y arriver.</li>
</ul>

## Organisation et préparation :

● ✅ Préparation en amont via un Trello, avec tâches à effectuer :
https://trello.com/b/xugCrEWb/open-meteo-api

![Capture d'écran 2025-06-24 215740](https://github.com/user-attachments/assets/c969c1c2-404f-448e-842a-b61800f178f0)

<ul>
<li>✅ Clonage projet d'origine de madzadev</li>
<li>✅ Familiarisation avec projet d'origine de madzadev</li>
<li>✅ Consultation README du projet</li>
<li>✅ Etude de la doc Open Meteo ( + doc Geocode pour géolocalisation )</li>
<li>✅ Etude de la doc Open Weather ( ancienne API à remplacer )</li>
<li>✅ Lancement projet et repérage des différents composants de l'application</li>
<li>✅ Liste des données appelées par Open Weather</li>
<li>✅ Recherche de donnée équivalente dans Open Meteo</li>
<li>✅ Mise à jour de la requête vers l'API Open Meteo (ne nécessite pas de clé, la config de l'environnement n'est pas utile), + ajustement du fichier data.js</li>
<li>✅ Ajustement de l'index.js et des composants concernés par la mise à jour des données</li>
<li>✅ Préparation d'un mapper pour remplacer les pictogrammes fournis par Open Weather par les pictogrammes fournis par Weather Icons, selon le code météo appelé</li>
<li>✅ Test du remplacement de l'API avec la fonction recherche initialement présente</li>
<li>✅ Remplacement de la fonction recherche avec un fichier config.json (comprenant une ville prédéfinie), et màj du composant MetricsBox pour enlever la fonctionnalité de recherche</li>
<li>✅ Ajustement du helper.js pour récupération du jour selon fuseau horaire</li>
<li>✅ Ajustement du converteur.js pour conversion donnée horaires (en int pour Open Weather, en string ISO pour Open Meteo)</li>
<li>✅ Test de l'application puis livraison via guthub</li>
</ul>


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
