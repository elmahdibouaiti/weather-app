# Application Next.js Weather

Cette application Next.js vous permet de rechercher la météo d'une ville spécifique en se connectant à l'API OpenWeatherMap.

## Fonctionnalités

- Recherchez la météo d'une ville en utilisant le champ de recherche.
- Affichez les informations météorologiques telles que la température, la description, l'humidité, etc.

## Installation

1. Clonez ce dépôt sur votre machine locale.

2. Accédez au répertoire du projet.

```bash
cd weather-app-nextjs
```

## Installez les dépendances
```bash
npm install
```

## Lancez l'application
```bash
npm run dev
```

## Technologies utilisées
- Next.js
- React
- Axios
- TailwindCSS

## Configuration de l'API OpenWeatherMap
L'application utilise l'API OpenWeatherMap pour récupérer les données météorologiques. Assurez-vous de suivre les étapes ci-dessous pour configurer correctement la connexion avec l'API :

1. Rendez-vous sur le site OpenWeatherMap et créez un compte gratuit.

2. Une fois connecté, accédez à votre tableau de bord et récupérez votre clé d'API.

3. Dans le répertoire du projet, renommez le fichier .env.example en .env.

4. Ouvrez le fichier .env et remplacez YOUR_WEATHER_API_KEY par votre clé d'API OpenWeatherMap.

5. Sauvegardez le fichier .env.

6. L'application utilisera maintenant votre clé d'API pour effectuer des requêtes vers l'API OpenWeatherMap.

## Structure du projet
Le projet est organisé en utilisant la structure par défaut de Next.js. Voici une vue d'ensemble de la structure des fichiers importants :

- pages/_app.js: Ce fichier contient le composant racine de l'application Next.js et est utilisé pour envelopper les autres composants.
- pages/index.js: Ce fichier contient la page principale de l'application où vous pouvez rechercher et afficher la météo.
- components/Spinner.jsx: Ce composant affiche un spinner de chargement lorsqu'une requête est en cours pour récupérer les données météorologiques.
- components/Weather.jsx: Ce composant affiche les informations météorologiques pour une ville spécifique.


## L'utilisation de l'API OpenWeatherMap pour afficher les résultats se fait de la manière suivante :
1. Lorsque l'utilisateur saisit une ville dans le champ de recherche et soumet le formulaire, la fonction fetchWeather est appelée.

2. Dans la fonction fetchWeather, une requête HTTP GET est effectuée en utilisant Axios vers l'URL de l'API OpenWeatherMap avec la ville saisie et votre clé d'API.

3. Une fois que la réponse est obtenue, les données de la météo sont mises à jour dans l'état weather à l'aide de la fonction setWeather.

4. Le composant Weather est rendu avec les données de la météo, et il affiche les informations telles que la température, la description, l'humidité, etc.

5. Pendant le chargement des données, le composant Spinner est affiché à la place du composant Weather.

## Remarques
Assurez-vous d'avoir une clé d'API OpenWeatherMap valide pour pouvoir récupérer les données météorologiques.
