# 🏨 Projet Kayak - Recommandation de Destinations

![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)
![Scrapy](https://img.shields.io/badge/Scrapy-2.11+-green.svg)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup4-4.12+-lightgrey.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)
![Folium](https://img.shields.io/badge/Folium-0.14+-orange.svg)
![AWS](https://img.shields.io/badge/AWS%20S3-blue.svg)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15+-316192.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)

## 📋 Description
Application de recommandation de destinations touristiques en France basée sur les données météorologiques et hôtelières. Le projet utilise le scraping de données, des APIs météo, et une visualisation interactive pour aider les utilisateurs à choisir leur prochaine destination de voyage.

## 🏗 Architecture Technique
- **Collecte de données** 📥 :
  - API OpenWeatherMap pour les données météo 🌤
  - Scraping de Booking.com avec Scrapy et BeautifulSoup 🕷
  - Geocoding via Nominatim 🗺
- **Stockage** 💾 :
  - AWS S3 pour le data lake ☁
  - Base de données PostgreSQL sur NeonDB 🐘
- **Visualisation** 📊 :
  - Folium pour les cartes interactives 🗺
  - Interface utilisateur avec contrôles de couches 🎮

## 🚀 Installation

Configurer les variables d'environnement (voir `.env.example` et `.secrets.example`)

## 📂 Structure du Projet
```
project/
│
├── src/
│   ├── projet_instruction.ipynb
│   ├── coordonnees_villes.csv
│   ├── hotels.csv
│   ├── previsions_meteo.csv
│   └── hotels.json
├── carte_hotels.html
├── .gitignore
├── Kayak.ipynb
├── readme.md
├── index.html
├── .env
└── .secrets
```

## 🗺️ Visualisation Interactive

Découvrez notre carte interactive des 5 meilleurs destinations françaises (villes les plus chaudes dans les 5 prochains jours !) :

[Voir la carte en plein écran](https://rom1legrand.github.io/MLE-B1-CollectAndManage-Plan-your_trip_Booking/)

## 🚀 Déploiement de la carte interactive sur GitHub Pages

Pour déployer la carte sur GitHub Pages :

1. Créez une branche gh-pages :
```bash
git checkout -b gh-pages
```

2. Ajoutez les fichiers nécessaires :
```bash
git add index.html carte_hotels.html
git commit -m "Add map page"
git push origin gh-pages
```

3. Configurez GitHub Pages :
   - Dans votre repository, allez dans Settings > Pages
   - Source : Sélectionnez la branche "gh-pages"
   - Save

La carte sera accessible à l'adresse : `https://[votre-username].github.io/[nom-repo]/`

## 🔄 Axes d'Amélioration
1. **Performance** ⚡ :
   - Ajouter de la pagination
   - Code python moins verbeux
   - Amélioration du Scraping (parfois défaillant sur les noms d'hôtels)

2. **Maintenance** 🔧 :
   - Ajouter des tests et retry (gestion des coupures "connect" avec bdd)
   - Documentation complète

3. **Évolutivité** 📈 :
   - Containerisation Docker
   - Automatisation et CI/CD
   - Monitoring
   - API moins limité pour plus de possibilités
