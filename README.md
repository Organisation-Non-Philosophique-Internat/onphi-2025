# ONPhI - Site Web

Site web de l'Organisation Non-Philosophique (ONPhI) développé avec Laminas Framework.

## 🚀 Fonctionnalités

### Interface Utilisateur
- **Accueil** : Page d'accueil avec éditorial de François Laruelle
- **Bibliothèque** : Catalogue des textes philosophiques
- **Corpus** : Collection de textes organisés par thèmes
- **Cours** : Système de réservation et gestion des cours
- **Forum** : Espace de discussion communautaire
- **Boutique** : Vente de livres et produits philosophiques

### Administration
- **Tableau de bord** : Interface d'administration complète
- **Gestion des utilisateurs** : Inscription, authentification, rôles
- **Gestion du contenu** : Éditoriaux, textes, cours
- **Réservations** : Gestion des réservations de cours
- **Cotisations** : Suivi des adhésions et paiements
- **Ventes** : Gestion des commandes et livraisons
- **Mailing list** : Gestion des abonnements OVH
- **Chatbot** : Interface de gestion des conversations IA

### Outils de Développement
- **phpinfo** : Affichage sécurisé des informations PHP (`/admin/phpinfo`)
- **Tests** : Interface d'exécution des fichiers de test (`/admin/tests`)
- **Générateur de mots de passe** : Outil de génération sécurisée (`/admin/passwords`)

## 🛠️ Technologies

### Backend
- **PHP 8.2+** : Langage de programmation
- **Laminas Framework** : Framework MVC
- **Doctrine ORM** : Mapping objet-relationnel
- **MySQL** : Base de données
- **Composer** : Gestionnaire de dépendances

### Frontend
- **Bootstrap 5** : Framework CSS
- **jQuery** : Bibliothèque JavaScript
- **Video.js** : Lecteur vidéo
- **Chart.js** : Graphiques et visualisations

### Services
- **OVH API** : Gestion des emails et domaines
- **PayPal** : Paiements en ligne
- **OpenAI** : Intégration IA pour le chatbot
- **TCPDF** : Génération de PDF

## 📁 Structure du Projet

```
web/
├── config/                 # Configuration de l'application
├── data/                   # Données et logs
├── module/                 # Modules Laminas
│   └── Application/        # Module principal
│       ├── src/
│       │   ├── Controller/ # Contrôleurs
│       │   ├── Service/    # Services métier
│       │   └── View/       # Helpers de vue
│       ├── view/           # Templates de vue
│       └── config/         # Configuration du module
├── public/                 # Point d'entrée web
├── tests/                  # Fichiers de test et diagnostic
├── tools/                  # Scripts utilitaires
└── vendor/                 # Dépendances Composer
```

## 🔧 Installation

### Prérequis
- PHP 8.2 ou supérieur
- MySQL 5.7 ou supérieur
- Composer
- Apache/Nginx avec mod_rewrite

### Configuration
1. Cloner le repository
2. Installer les dépendances : `composer install`
3. Configurer la base de données dans `config/autoload/local.php`
4. Configurer les variables d'environnement
5. Configurer le serveur web pour pointer vers `public/`

### Variables d'environnement
```env
DB_HOST=localhost
DB_NAME=onphi
DB_USER=onphi
DB_PASS=password
OVH_APP_KEY=your_key
OVH_APP_SECRET=your_secret
PAYPAL_CLIENT_ID=your_id
OPENAI_API_KEY=your_key
```

## 🚨 Problèmes Connus

### Page Blanche
**Symptôme** : Les pages principales (`/fr`, `/fr/accueil`, etc.) affichent un contenu vide (Content-Length: 0).

**Cause identifiée** : Problème dans le système de rendu des vues de Laminas Framework.

**Diagnostic effectué** :
- ✅ MySQL et Doctrine fonctionnent correctement
- ✅ Les traductions fonctionnent
- ✅ Les templates existent et sont accessibles
- ✅ La configuration des helpers de vue est correcte
- ❌ Le système de rendu Laminas retourne 0 caractères

**Solutions tentées** :
- Correction du shutdown handler dans `public/index.php`
- Ajout des templates au `template_map`
- Mise à jour des modules Laminas
- Régénération du dossier `vendor/`

**Solution temporaire** : Utiliser les outils d'administration qui fonctionnent correctement.

## 🔐 Sécurité

### Authentification
- Système de rôles et permissions (RBAC)
- Authentification par session
- Protection CSRF sur les formulaires

### Administration
- Accès restreint aux administrateurs uniquement
- Validation des entrées utilisateur
- Échappement des sorties HTML

### Mots de passe
- Génération cryptographiquement sécurisée avec `random_int()`
- Hachage avec `password_hash()` (PASSWORD_DEFAULT, BCRYPT, ARGON2ID)
- Calcul de l'entropie pour évaluer la force

## 📊 Monitoring

### Logs
- **PHP** : `data/log/php-error.log`
- **Application** : `data/log/application.log`
- **Bot** : Logs des conversations IA

### Outils de diagnostic
- **phpinfo** : `/admin/phpinfo`
- **Tests** : `/admin/tests`
- **OPcache** : `/opcache_reset.php`

## 🤖 IA et Chatbot

### Intégration OpenAI
- Modèle personnalisé `text-onphi-001`
- Gestion des conversations
- Logs des interactions
- Interface d'administration

### Fonctionnalités
- Réponses contextuelles sur la philosophie
- Gestion des sessions utilisateur
- Historique des conversations

## 📧 Communication

### Mailing List
- Gestion via API OVH
- Abonnement/désabonnement
- Interface d'administration

### Notifications
- Flash messages pour les retours utilisateur
- Emails de confirmation
- Notifications système

## 🛡️ Maintenance

### Sauvegarde
- Base de données MySQL
- Fichiers uploadés
- Configuration

### Mise à jour
- `composer update` pour les dépendances
- Migration de base de données si nécessaire
- Tests de régression

## 📞 Support

Pour toute question ou problème :
1. Vérifier les logs dans `data/log/`
2. Utiliser les outils de diagnostic dans `/admin/`
3. Consulter la documentation Laminas
4. Contacter l'équipe de développement

## 📝 Changelog

### Version actuelle
- ✅ Interface d'administration complète
- ✅ Générateur de mots de passe sécurisé
- ✅ Outils de diagnostic et tests
- ✅ Intégration OpenAI
- ✅ Gestion des réservations et cotisations
- ⚠️ Problème de page blanche en cours de résolution

---

**Développé avec ❤️ pour la philosophie non-standard**
