# 🚀 Annuaire OpenDev Mada

Un annuaire moderne et interactif pour les membres de la communauté OpenDev Madagascar. Cette plateforme permet de découvrir, se connecter et collaborer avec les développeurs malgaches.

![Aperçu de l'Annuaire](https://via.placeholder.com/800x400/1F2937/FFFFFF?text=Annuaire+OpenDev+Mada)

## ✨ Fonctionnalités

- **Profils Détaillés** - Informations complètes des développeurs (compétences, projets, contact)
- **Recherche Avancée** - Filtrage par technologies, localisation, niveau d'expérience
- **Cartes Interactives** - Visualisation géographique des membres à Madagascar
- **Système de Tags** - Classification par compétences et domaines d'expertise
- **Mode Sombre/Clair** - Interface adaptable selon les préférences
- **Responsive Design** - Optimisé pour mobile, tablette et desktop
- **Export de Données** - Téléchargement des contacts en format vCard
- **Statistiques** - Aperçu des technologies les plus utilisées dans la communauté

## 🛠️ Technologies Utilisées

- **Frontend :** [React.js](https://reactjs.org/) - Framework JavaScript
- **Styling :** [Tailwind CSS](https://tailwindcss.com/) - Framework CSS utilitaire
- **Icônes :** [Lucide React](https://lucide.dev/) - Collection d'icônes modernes
- **Cartes :** [Leaflet](https://leafletjs.com/) - Cartographie interactive
- **Recherche :** [Fuse.js](https://fusejs.io/) - Recherche floue avancée
- **Base de Données :** JSON local 
- **Déploiement :** [Vercel](https://vercel.com/) / [Netlify](https://netlify.com/)

## 🚀 Installation et Configuration

### Prérequis

Assurez-vous d'avoir installé sur votre machine :

- [Node.js](https://nodejs.org/) (version 16.0 ou supérieure)
- [npm](https://www.npmjs.com/) ou [yarn](https://yarnpkg.com/)
- [Git](https://git-scm.com/)

### Installation

1. **Cloner le dépôt**
   ```bash
   git clone https://github.com/opendev-mada/annuaire-membres.git
   cd annuaire-membres
   ```

2. **Installer les dépendances**
   ```bash
   npm install
   # ou
   yarn install
   ```

3. **Configurer les variables d'environnement**
   ```bash
   cp .env.example .env.local
   ```
   
   Modifiez le fichier `.env.local` avec vos configurations :
   ```env
   REACT_APP_API_URL=https://api.opendev-mada.mg
   REACT_APP_MAPBOX_TOKEN=your_mapbox_token_here
   REACT_APP_ENVIRONMENT=development
   ```

4. **Lancer le serveur de développement**
   ```bash
   npm start
   # ou
   yarn start
   ```

5. **Ouvrir dans le navigateur**
   
   Rendez-vous sur [http://localhost:3000](http://localhost:3000)

## 📁 Structure du Projet

```
annuaire-opendev-mada/
├── public/
│   ├── index.html
│   ├── favicon.ico
│   ├── manifest.json
│   └── data/
│       └── membres.json
├── src/
│   ├── components/
│   │   ├── common/
│   │   │   ├── Header.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── Layout.jsx
│   │   │   └── Loading.jsx
│   │   ├── membres/
│   │   │   ├── MembreCard.jsx
│   │   │   ├── MembreDetail.jsx
│   │   │   ├── MembresList.jsx
│   │   │   └── MembreForm.jsx
│   │   ├── recherche/
│   │   │   ├── SearchBar.jsx
│   │   │   ├── FilterPanel.jsx
│   │   │   └── TagsFilter.jsx
│   │   ├── cartes/
│   │   │   ├── MapView.jsx
│   │   │   └── MarkerPopup.jsx
│   │   └── statistiques/
│   │       ├── StatsOverview.jsx
│   │       └── TechChart.jsx
│   ├── data/
│   │   ├── membres.js
│   │   ├── technologies.js
│   │   └── regions.js
│   ├── hooks/
│   │   ├── useMembers.js
│   │   ├── useSearch.js
│   │   └── useLocalStorage.js
│   ├── utils/
│   │   ├── api.js
│   │   ├── constants.js
│   │   ├── helpers.js
│   │   └── exportData.js
│   ├── styles/
│   │   └── globals.css
│   ├── pages/
│   │   ├── Home.jsx
│   │   ├── Directory.jsx
│   │   ├── Profile.jsx
│   │   ├── Map.jsx
│   │   └── About.jsx
│   ├── App.js
│   └── index.js
├── .gitignore
├── package.json
├── tailwind.config.js
├── postcss.config.js
└── README.md
```

## 👥 Contribution et Ajout de Membres

### Format des Données Membres

Les profils des membres sont stockés dans `public/data/membres.json` :

```json
{
  "id": "unique-id",
  "nom": "Nom Complet",
  "pseudo": "username",
  "email": "email@exemple.com",
  "telephone": "+261 XX XX XXX XX",
  "poste": "Développeur Full Stack",
  "entreprise": "Nom de l'entreprise",
  "localisation": {
    "ville": "Antananarivo",
    "region": "Analamanga",
    "coordonnees": {
      "lat": -18.8792,
      "lng": 47.5079
    }
  },
  "competences": [
    "JavaScript",
    "React",
    "Node.js",
    "MongoDB"
  ],
  "niveaux": {
    "JavaScript": "Expert",
    "React": "Intermédiaire",
    "Node.js": "Avancé"
  },
  "bio": "Description du développeur...",
  "disponible": true,
  "projets": [
    {
      "nom": "Projet Example",
      "description": "Description du projet",
      "technologies": ["React", "Node.js"],
      "url": "https://github.com/user/projet"
    }
  ],
  "reseaux": {
    "github": "https://github.com/username",
    "linkedin": "https://linkedin.com/in/username",
    "twitter": "https://twitter.com/username",
    "portfolio": "https://monsite.com"
  },
  "dateInscription": "2024-01-15",
  "derniereMiseAJour": "2024-06-20"
}
```

### Ajouter un Nouveau Membre

1. **Forkez le dépôt** sur GitHub
2. **Créez une branche** pour votre ajout :
   ```bash
   git checkout -b ajout-membre-votre-nom
   ```
3. **Ajoutez votre profil** dans `public/data/membres.json`
4. **Testez localement** que tout fonctionne
5. **Committez vos changements** :
   ```bash
   git add .
   git commit -m "Ajout du profil de [Votre Nom]"
   ```
6. **Poussez votre branche** :
   ```bash
   git push origin ajout-membre-votre-nom
   ```
7. **Créez une Pull Request** sur GitHub

### Validation des Données

Avant de soumettre, assurez-vous que :

- [ ] Toutes les informations obligatoires sont renseignées
- [ ] L'email est valide et professionnel
- [ ] Les compétences correspondent aux technologies réelles
- [ ] Les liens vers les réseaux sociaux fonctionnent
- [ ] La localisation est précise (coordonnées GPS)
- [ ] La bio est professionnelle et informative

## 🎨 Personnalisation

### Couleurs et Thème

Modifiez le fichier `tailwind.config.js` pour personnaliser les couleurs :

```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: {
          50: '#f0f9ff',
          500: '#3b82f6',
          900: '#1e3a8a'
        },
        accent: {
          500: '#10b981'
        }
      }
    }
  }
}
```

### Ajout de Nouvelles Technologies

Modifiez `src/data/technologies.js` pour ajouter de nouvelles compétences :

```javascript
export const technologies = [
  {
    nom: 'React',
    categorie: 'Frontend',
    couleur: '#61dafb',
    icone: 'react-icon'
  },
  // Ajoutez vos nouvelles technologies ici
];
```

## 🚀 Déploiement

### Déploiement sur Vercel

1. **Connectez votre dépôt** à Vercel
2. **Configurez les variables d'environnement** dans le dashboard
3. **Déployez automatiquement** à chaque push

### Déploiement sur Netlify

1. **Buildez le projet** :
   ```bash
   npm run build
   ```
2. **Déployez le dossier `build/`** sur Netlify
3. **Configurez les redirections** pour React Router

### Configuration Nginx (serveur personnel)

```nginx
server {
    listen 80;
    server_name annuaire.opendev-mada.mg;
    
    root /var/www/annuaire/build;
    index index.html;
    
    location / {
        try_files $uri $uri/ /index.html;
    }
    
    location /api {
        proxy_pass http://localhost:3001;
    }
}
```

## 📊 Analytics et Statistiques

### Suivi des Visites

Intégration avec Google Analytics :

```javascript
// Dans src/utils/analytics.js
export const trackPageView = (page) => {
  if (window.gtag) {
    window.gtag('config', 'GA_MEASUREMENT_ID', {
      page_path: page
    });
  }
};
```

### Statistiques de la Communauté

Le dashboard affiche automatiquement :
- Nombre total de membres
- Répartition par région
- Technologies les plus populaires
- Taux de disponibilité pour des projets
- Évolution des inscriptions

## 🔒 Sécurité et Confidentialité

### Protection des Données

- Les données personnelles sont anonymisées par défaut
- Seules les informations publiques sont affichées
- Respect des réglementations sur la protection des données

### Contribution Sécurisée

- Validation automatique des données soumises
- Modération des nouveaux profils
- Protection contre les injections et XSS

## 🤝 Contribution au Projet

### Types de Contributions

- **Ajout de membres** - Nouveaux profils de développeurs
- **Amélioration du code** - Corrections de bugs, nouvelles fonctionnalités
- **Documentation** - Amélioration de la documentation
- **Design** - Améliorations UI/UX
- **Traduction** - Support multilingue (Français/Malgache/Anglais)

### Processus de Contribution

1. Consultez les [issues ouvertes](https://github.com/opendev-mada/annuaire-membres/issues)
2. Créez une issue pour discuter des changements majeurs
3. Forkez le projet et créez une branche
4. Développez avec des commits clairs
5. Ajoutez des tests si nécessaire
6. Soumettez une Pull Request détaillée

### Code de Conduite

En participant à ce projet, vous acceptez de respecter notre [Code de Conduite](CODE_DE_CONDUITE.md) basé sur les valeurs de la communauté OpenDev Madagascar.

## 🎯 Roadmap

### Version 2.0 (Q3 2024)
- [ ] Système d'authentification pour les membres
- [ ] Interface d'administration
- [ ] API REST complète
- [ ] Notifications push
- [ ] Chat intégré entre membres

### Version 2.1 (Q4 2024)
- [ ] Application mobile (React Native)
- [ ] Système de matching pour projets
- [ ] Calendrier des événements
- [ ] Badges et certifications

### Version 3.0 (Q1 2025)
- [ ] Intelligence artificielle pour recommandations
- [ ] Intégration avec les plateformes de freelance
- [ ] Système de réputation
- [ ] Marketplace de services

## 📞 Contact et Support

### Équipe OpenDev Mada

- **Site Web :** [https://opendev-mada.mg](https://opendev-mada.mg)
- **Email :** contact@opendev-mada.mg
- **Telegram :** [@OpenDevMada](https://t.me/OpenDevMada)
- **Facebook :** [OpenDev Madagascar](https://facebook.com/OpenDevMadagascar)

### Dépôt du Projet

**GitHub :** [https://github.com/opendev-mada/annuaire-membres](https://github.com/opendev-mada/annuaire-membres)

**Demo Live :** [https://annuaire.opendev-mada.mg](https://annuaire.opendev-mada.mg)

### Support Technique

Pour toute question technique ou problème :

1. Consultez d'abord la [documentation](https://docs.opendev-mada.mg)
2. Recherchez dans les [issues existantes](https://github.com/opendev-mada/annuaire-membres/issues)
3. Créez une nouvelle issue avec le template approprié
4. Contactez l'équipe sur Telegram pour une aide rapide

## 📄 Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE.md](LICENSE.md) pour plus de détails.

## 🙏 Remerciements

Merci à tous les membres de la communauté OpenDev Madagascar qui contribuent à faire grandir l'écosystème tech malgache :

- **Contributeurs principaux** - Développement et maintenance
- **Membres actifs** - Ajout de profils et feedback
- **Partenaires** - Support technique et hébergement
- **Communauté tech malgache** - Inspiration et motivation

### Technologies et Outils

- [React.js](https://reactjs.org/) - Framework JavaScript
- [Tailwind CSS](https://tailwindcss.com/) - Framework CSS
- [Leaflet](https://leafletjs.com/) - Cartographie
- [Vercel](https://vercel.com/) - Plateforme de déploiement
- [GitHub](https://github.com/) - Hébergement du code

---

**Ensemble, construisons l'avenir du développement à Madagascar ! 🇲🇬**

⭐ **N'oubliez pas de mettre une étoile au projet si vous le trouvez utile !**