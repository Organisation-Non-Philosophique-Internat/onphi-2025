# 🌐 ONPhI - Organisation Non-Philosophique Internationale

<div align="center">

![Version](https://img.shields.io/badge/version-6.0.4-blue.svg)
![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?logo=php)
![Laminas](https://img.shields.io/badge/Laminas-Framework-68B604?logo=laminas)
![License](https://img.shields.io/badge/license-MIT-green.svg)

**Plateforme web dédiée à la promotion et à l'étude de la non-philosophie de François Laruelle**

[Site Web](https://onphi.org) • [Documentation](#-documentation) • [Installation](#-installation) • [Support](#-support)

</div>

---

## 📖 À Propos

L'**Organisation Non-Philosophique Internationale (ONPhI)** est une association qui a pour objet d'encourager la recherche, la pratique, les échanges, l'explication et la diffusion de la non-philosophie, telle quelle a été en particulier définie dans les oeuvres de M. François Laruelle, Professeur de Philosophie à l'Université Paris X (Nanterre, Hauts-de-Seine) ; de réunir toutes personnes qui ont de l'affinité pour ce projet théorique, d'organiser en dernière instance les différents courants de cette école, dans le sens de leur plus grande fécondité.

### 🎯 Mission

Promouvoir et développer la **non-philosophie** de François Laruelle à travers une plateforme web moderne offrant :
- Accès aux textes fondamentaux et aux correspondances philosophiques
- Formation et enseignement via l'École de Non-Philosophie
- Espace communautaire de discussion et d'échange
- Distribution de publications spécialisées

---

## ✨ Fonctionnalités Principales

### 🛒 **Boutique en Ligne**
- Catalogue de publications philosophiques et revues
- Panier moderne avec interface intuitive
- Paiement sécurisé via PayPal
- Gestion complète des commandes et livraisons
- Pré-remplissage automatique des formulaires pour les membres

### 🔐 **Authentification & Sécurité**
- **Connexion locale** : Système traditionnel avec hashage sécurisé
- **Microsoft OAuth 2.0** : Authentification via Microsoft Graph API
- **RBAC** : Système de rôles et permissions granulaires
- **CSRF Protection** : Protection contre les attaques cross-site
- **Sessions sécurisées** : Gestion des sessions avec Laminas

### 🎓 **École de Non-Philosophie**
- **Séminaires et cours** : Système de réservation et gestion
- **Ressources pédagogiques** : Bibliothèque de contenus éducatifs
- **Scriptorium** : Espace de production et travail étudiant
- **Design unifié** : Interface moderne et responsive avec CSS modulaire

### 💬 **Forum Communautaire**
- **Interface modernisée** : Design responsive avec cartes élégantes
- **Support BBCode complet** : Formatage de texte, liens, images, code
- **Système de filtres** : Tri par date, popularité, réponses
- **Pagination optimisée** : Navigation fluide entre les pages
- **125+ messages** : Base de données réelle intégrée

### 🌍 **Multilingue**
- **9 langues supportées** : FR, EN, ES, DE, IT, JA, ZH, PL, RU
- **Traductions dynamiques** : Système de gestion des langues
- **Interface multilingue** : Adaptation complète du contenu

### 📚 **Contenus Philosophiques**
- **Lettres de François Laruelle** : Collection des correspondances
- **Chroniques non-épistémologiques** : Articles et publications
- **Corpus** : Textes organisés par thèmes et auteurs
- **Bibliothèque** : Catalogue complet des textes philosophiques
- **Philo-fictions** : Contenus créatifs et expérimentaux

### 🎥 **Multimédia**
- **Laruelle Sonore** : Enregistrements audio
- **Radio ONPhI** : Diffusion de contenus audio
- **Vidéos** : Conférences et présentations
- **Intégration Zoom** : Réunions virtuelles pour l'École

### 🤖 **Intelligence Artificielle**
- **Chatbot OpenAI** : Assistant conversationnel sur la non-philosophie
- **Génération de texte** : GPT-4o pour création de contenu
- **Génération d'images** : DALL-E 3 intégré
- **Audio TTS** : Conversion texte vers parole (6 voix)
- **Transcription** : Whisper pour speech-to-text
- **Vision AI** : Analyse d'images avec GPT-4 Vision
- **Accès restreint** : Réservé aux membres et étudiants

### ⚙️ **Administration**
- **Tableau de bord complet** : Gestion centralisée
- **Gestion des utilisateurs** : Rôles, permissions, cotisations
- **Gestion du contenu** : Éditoriaux, textes, cours, forum
- **Outils de diagnostic** : phpinfo, tests, générateur de mots de passe
- **Mailing list OVH** : Gestion des abonnements email
- **Statistiques** : Suivi des performances et analytics

---

## 📁 Structure du Projet

```
web/
├── config/                      # Configuration de l'application
│   ├── autoload/               # Configuration auto-chargée
│   │   ├── global.php          # Config globale
│   │   ├── local.php           # Config locale (non versionnée)
│   │   └── *.config.php        # Configs des modules
│   └── application.config.php  # Config principale
│
├── data/                        # Données et fichiers générés
│   ├── cache/                  # Cache de l'application
│   ├── logs/                   # Logs (application, PHP, errors)
│   └── uploads/                # Fichiers uploadés
│
├── docs/                        # 📚 Documentation complète
│   ├── BOUTIQUE_*.md           # Documentation boutique/e-commerce
│   ├── FORUM_*.md              # Documentation forum
│   ├── MICROSOFT_OAUTH_*.md    # Documentation OAuth
│   ├── UNIFORMISATION_*.md     # Documentation design system
│   ├── MODERNISATION_*.md      # Documentation améliorations
│   └── SECURITY.md             # Politique de sécurité
│
├── k8s/                         # ☸️ Déploiement Kubernetes
│   ├── base/                   # Manifests de base
│   ├── overlays/               # Configurations par environnement
│   ├── helm/                   # Charts Helm
│   ├── docker/                 # Dockerfiles
│   ├── scripts/                # Scripts de déploiement
│   ├── ci/                     # CI/CD configuration
│   ├── README.md               # Guide Kubernetes
│   └── DEPLOYMENT.md           # Guide de déploiement
│
├── module/                      # 🔧 Modules Laminas
│   └── Application/
│       ├── config/             # Configuration du module
│       ├── src/
│       │   ├── Controller/     # Contrôleurs MVC
│       │   ├── Service/        # Services métier
│       │   ├── Entity/         # Entités Doctrine
│       │   ├── Repository/     # Repositories Doctrine
│       │   └── View/           # View Helpers
│       └── view/               # Templates .phtml
│           ├── application/    # Vues par contrôleur
│           ├── layout/         # Layouts principaux
│           └── partials/       # Composants réutilisables
│
├── public/                      # 🌐 Point d'entrée web
│   ├── assets/                 # Assets statiques
│   │   ├── css/               # Feuilles de style
│   │   ├── js/                # JavaScript
│   │   ├── images/            # Images
│   │   └── fonts/             # Polices
│   ├── uploads/               # Fichiers uploadés publics
│   ├── index.php              # Point d'entrée principal
│   └── .htaccess              # Configuration Apache
│
├── tests/                       # 🧪 Tests et diagnostic
│   ├── test-*.php             # Scripts de test PHP
│   ├── test-*.sh              # Scripts de test Shell
│   ├── final_summary.md       # Résumé des tests
│   └── index.html             # Interface web des tests
│
├── tools/                       # 🛠️ Scripts utilitaires
│   ├── clear-cache-*.sh       # Scripts de nettoyage cache
│   └── maintenance/           # Scripts de maintenance
│
├── vendor/                      # 📦 Dépendances Composer
│
├── .env                        # Variables d'environnement (non versionné)
├── composer.json               # Dépendances PHP
├── README.md                   # Ce fichier
└── README-*.md                 # READMEs spécifiques (tests, cache, etc.)
```

### 📂 Répertoires Importants

| Répertoire | Description |
|-----------|-------------|
| `config/` | Configuration de l'application et des modules |
| `docs/` | Documentation complète du projet (80+ documents) |
| `k8s/` | Infrastructure Kubernetes pour le déploiement |
| `module/Application/` | Code source principal de l'application |
| `public/` | Fichiers accessibles publiquement via le web |
| `tests/` | Scripts de test et diagnostic |
| `tools/` | Utilitaires de maintenance |

---

## 🛠️ Technologies & Stack

### Backend
| Technologie | Version | Usage |
|------------|---------|-------|
| **PHP** | 8.2+ | Langage principal |
| **Laminas Framework** | 3.x | Framework MVC |
| **Doctrine ORM** | 2.x | Mapping objet-relationnel |
| **MySQL/MariaDB** | 5.7+ / 10.x+ | Base de données |
| **Composer** | 2.x | Gestionnaire de dépendances |

### Frontend
| Technologie | Usage |
|------------|-------|
| **Bootstrap 5** | Framework CSS responsive |
| **jQuery** | Manipulation DOM et AJAX |
| **FontAwesome** | Bibliothèque d'icônes |
| **Video.js** | Lecteur vidéo |
| **Chart.js** | Graphiques et visualisations |
| **CKEditor** | Éditeur WYSIWYG |

### Services & APIs
| Service | Usage |
|---------|-------|
| **OpenAI API** | ChatGPT, DALL-E, Whisper, TTS |
| **Microsoft Graph API** | Authentification OAuth 2.0 |
| **PayPal API** | Paiements en ligne |
| **OVH API** | Gestion emails et domaines |
| **Zoom SDK** | Réunions virtuelles |
| **TCPDF** | Génération de documents PDF |

### Infrastructure & DevOps
| Technologie | Usage |
|------------|-------|
| **Kubernetes** | Orchestration de conteneurs |
| **Docker** | Conteneurisation |
| **Nginx** | Serveur web / Reverse proxy |
| **PHP-FPM** | Gestionnaire de processus PHP |
| **Apache** | Serveur web (alternative) |
| **Redis** | Cache et sessions (optionnel) |

---

## 📚 Documentation Complète

### 🛒 **Boutique & E-commerce**

#### Fonctionnalités
- [🛍️ Boutique Fonctionnelle](docs/BOUTIQUE_FONCTIONNELLE.md) - Vue d'ensemble du système
- [🚀 Quick Start Shop](docs/QUICK_START_SHOP.md) - Démarrage rapide
- [📋 Implémentation Finale](docs/IMPLEMENTATION_FINALE.md) - Détails d'implémentation
- [📊 Comparatif Boutique](docs/COMPARATIF_BOUTIQUE.md) - Analyse comparative

#### Améliorations & Corrections
- [🛒 Amélioration du Formulaire de Commande](docs/AMELIORATION_FORMULAIRE_COMMANDE.md)
- [📦 Corrections Finales du Panier](docs/CORRECTIONS_FINALES_PANIER.md)
- [🎨 Panier Moderne Complet](docs/PANIER_MODERNE_COMPLETE.md)
- [🖼️ Résolution des Images Produits](docs/IMAGES_PRODUITS_RESOLUES.md)
- [🔴 Corrections des Boutons](docs/BOUTON_AJOUT_PANIER_CORRIGE.md)
- [🎨 Suppression des Bordures d'Icônes](docs/BORDURES_ICONES_SUPPRIMEES.md)

#### Tests & Résolution de Problèmes
- [🧪 Tests du Shop](docs/TEST_SHOP.md)
- [🔧 Résolution des Problèmes](docs/PROBLEMES_PANIER_RESOLUS.md)
- [✅ Résolution Finale](docs/RESOLUTION_FINALE.md)

### 💬 **Forum Communautaire**

- [🎨 Modernisation du Forum](docs/MODERNISATION_FORUM.md) - Refonte complète
- [📝 Résumé Modernisation Forum](docs/RESUME_MODERNISATION_FORUM.md)
- [❌ Erreur 500 Forum - Résolution](docs/ERREUR_500_FORUM_RESOLUTION.md)
- Documents racine :
  - [FORUM-IMPROVEMENTS.md](FORUM-IMPROVEMENTS.md) - Améliorations interface
  - [FORUM-REPLIES-FIX.md](FORUM-REPLIES-FIX.md) - Correction système de réponses
  - [FORUM-FIXES.md](FORUM-FIXES.md) - Corrections générales
  - [FORUM-TEST-RESULTS.md](FORUM-TEST-RESULTS.md) - Résultats des tests

### 🔐 **Authentification & Sécurité**

#### Microsoft OAuth
- [🔐 Microsoft OAuth README](docs/MICROSOFT_OAUTH_README.md) - Guide complet
- [📝 Résumé Final Microsoft](docs/RESUME_FINAL_MICROSOFT.md)
- [👤 Correction Client Public Microsoft](docs/CORRECTION_CLIENT_PUBLIC_MICROSOFT.md)
- [📄 Fichiers Test Microsoft](docs/README_FICHIERS_TEST_MICROSOFT.md)
- [📊 Rapport d'Analyse Redirection Microsoft](docs/rapport_analyse_microsoft_redirection.md)

#### Sécurité Générale
- [🛡️ Security Policy](docs/SECURITY.md)
- [🔐 Login CSRF Fix](LOGIN-CSRF-FIX.md)

### 🎓 **École de Non-Philosophie**

#### Design & Interface
- [🎨 Amélioration École](AMELIORATION-ECOLE.md) - Refonte complète
- [🎨 School Resources Style Abrégé](SCHOOL-RESOURCES-STYLE-ABREGE.md)
- [🎨 School Seminars Style Abrégé](SCHOOL-SEMINARS-STYLE-ABREGE.md)
- [🔧 School Seminars Header Fix](SCHOOL-SEMINARS-HEADER-FIX.md)
- [📝 School Seminars Update](SCHOOL-SEMINARS-UPDATE.md)
- [🔄 School Resources Restoration](SCHOOL-RESOURCES-RESTORATION.md)
- [📖 Resources Readability Improvements](RESOURCES-READABILITY-IMPROVEMENTS.md)

#### Pages Unifiées
- [🎨 School Pages Unified Headers](SCHOOL-PAGES-UNIFIED-HEADERS.md)
- [🚀 Quick Access Improvements](QUICK-ACCESS-IMPROVEMENTS.md)

### 🎨 **Design System & Interface**

#### Uniformisation
- [🎨 Uniformisation Pages Complète](docs/UNIFORMISATION_PAGES_COMPLETE.md)
- [🔗 Uniformisation URLs Menu](docs/UNIFORMISATION_URLS_MENU_RESUME.md)
- [✅ Uniformisation URLs Final](docs/UNIFORMISATION_URLS_FINAL.md)

#### Optimisations
- [⚡ CSS Optimization](CSS-OPTIMIZATION.md) - Optimisation des styles
- [📱 Responsive Improvements](public/RESPONSIVE_IMPROVEMENTS.md)
- [🎨 Homepage Image Responsive](HOMEPAGE-IMAGE-RESPONSIVE.md)

#### Corrections Interface
- [🔧 Sidebar Dropdown Solution](SIDEBAR-DROPDOWN-SOLUTION.md)
- [🔧 Sidebar Dropdown Final Fix](SIDEBAR-DROPDOWN-FINAL-FIX.md)
- [🔧 Sidebar JS Solution](SIDEBAR-JS-SOLUTION.md)
- [📊 Sidebar Dropdown Diagnostic Final](SIDEBAR-DROPDOWN-DIAGNOSTIC-FINAL.md)

### 🤖 **Intelligence Artificielle**

- [🤖 OpenAI Improvements](OPENAI-IMPROVEMENTS.md) - Intégrations IA complètes
- [📚 LogService README](docs/LOGSERVICE_README.md) - Logging des conversations IA

### 🎥 **Intégrations Multimédia**

- [🎥 Zoom Integration Improvements](ZOOM-INTEGRATION-IMPROVEMENTS.md)
- [📹 Video App READMEs](public/tests/video-app/) - Tests vidéo

### 🧪 **Tests & Qualité**

- [📁 Organisation Tests](ORGANISATION-TESTS.md) - Structure des tests
- [📝 Post Admin Fix](POST-ADMIN-FIX.md)
- [🌍 Translation Fixes](TRANSLATION-FIXES.md)

### 📊 **Rapports & Analyses**

- [📊 Rapport Vérification Admin](docs/rapport_verification_admin.md)
- [📝 Résumé Corrections Complètes](RESUME-CORRECTIONS-COMPLETE.md)
- [✅ Corrections Finales](CORRECTIONS-FINALES.md)
- [💳 Cart Paiement Fix](CART-PAIEMENT-FIX.md)

### ☸️ **Déploiement & Infrastructure**

- [☸️ Kubernetes README](k8s/README.md) - Guide complet Kubernetes
- [🚀 Deployment Guide](k8s/DEPLOYMENT.md) - Guide de déploiement détaillé
- [📦 README Cache Scripts](README-cache-scripts.md) - Scripts de cache

---

## 🧪 Tests & Diagnostic

Le projet dispose d'une suite complète de tests et d'outils de diagnostic.

### 📊 **Interface Web des Tests**

Accédez à l'interface web des tests : `/tests/index.html`

### 🛒 **Tests de la Boutique**

```bash
# Tests du panier
php tests/test-cart-final.php          # Test complet du panier
php tests/test-cart-modern.php         # Test interface moderne
php tests/test-cart-images.php         # Test des images produits

# Tests des boutons et interactions
php tests/test-add-to-cart.php         # Test ajout au panier
php tests/test-cart-back-button.php    # Test bouton retour
php tests/test-cart-red-colors.php     # Test couleurs ONPhI

# Tests du formulaire de commande
php tests/test-form-pre-fill.php       # Test pré-remplissage
```

### 💬 **Tests du Forum**

```bash
# Tests du forum modernisé
php tests/test-forum-controller.php    # Test contrôleur
php tests/test-forum-modern.php        # Test interface moderne
php tests/test-forum-simple.php        # Test version simple
php tests/test-forum-diagnosis.php     # Diagnostic complet
php tests/test-forum-debug2.php        # Debug avancé
php tests/test-forum-error.php         # Test gestion erreurs
php tests/test-forum-sql.php           # Test requêtes SQL
```

### 🔐 **Tests d'Authentification**

```bash
# Tests Microsoft OAuth
php tests/test-microsoft-oauth.php
php tests/test-microsoft-redirect.php
php tests/test-microsoft-callback.php
php tests/test-microsoft-graph.php

# Tests de connexion
php tests/test-login-local.php
php tests/test-login-session.php
php tests/test-authentication-rbac.php
```

### 🎓 **Tests de l'École**

```bash
# Tests des pages de l'école
php tests/test-school-index.php
php tests/test-school-seminars.php
php tests/test-school-resources.php
php tests/test-school-registration.php
```

### 🌍 **Tests Généraux & Pages**

```bash
# Tests de toutes les pages
php tests/test-all-pages.php                    # Test complet du site
php tests/test-pages-status.php                 # Vérification HTTP status
php tests/test-all-pages-uniformisation.php     # Test uniformisation design

# Tests de traductions
php tests/check-translations.php        # Vérification traductions
php tests/fix-translations.php          # Correction traductions

# Tests de performance
php tests/test-performance.php          # Tests de performance
php tests/test-database-queries.php     # Optimisation requêtes
```

### 🛠️ **Scripts de Cache**

```bash
# Nettoyage du cache
./clear-cache-final.sh                  # Script complet avec PHP-FPM restart
./clear-cache-simple.sh                 # Version simplifiée
php clear-opcache.php                   # Nettoyage OPcache

# Tests de cache
./tests/test-web-opcache.sh             # Test cache web
php tests/clear-opcache.php             # Test nettoyage
```

### 🔧 **Outils d'Administration**

Accessibles via l'interface d'administration :

- **phpinfo** : `/admin/phpinfo` - Informations PHP
- **Tests** : `/admin/tests` - Exécution des tests
- **Cache** : `/admin/cache` - Gestion du cache
- **Passwords** : `/admin/passwords` - Générateur de mots de passe
- **Logs** : `/admin/logs` - Consultation des logs

---

## 💾 Installation

### 📋 **Prérequis**

#### Système
- **OS** : Linux (Ubuntu 20.04+, Debian 11+) ou similaire
- **PHP** : 8.2 ou supérieur
- **MySQL/MariaDB** : 5.7+ / 10.3+
- **Serveur Web** : Apache 2.4+ ou Nginx 1.18+
- **Composer** : 2.x
- **Node.js** : 14+ (pour les assets frontend, optionnel)

#### Extensions PHP Requises
```bash
# Extensions essentielles
php-cli php-fpm php-mysql php-mbstring php-xml php-curl
php-gd php-intl php-zip php-json php-opcache

# Extensions recommandées
php-redis php-imagick php-bcmath
```

### 🚀 **Installation Standard**

#### 1. Cloner le Repository
```bash
git clone https://github.com/onphi/web.git
cd web
```

#### 2. Installer les Dépendances
```bash
# Installer les dépendances PHP
composer install

# Pour le développement
composer install --dev

# Pour la production
composer install --no-dev --optimize-autoloader
```

#### 3. Configuration de la Base de Données

```bash
# Créer la base de données
mysql -u root -p
CREATE DATABASE onphi CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'onphi'@'localhost' IDENTIFIED BY 'votre_mot_de_passe';
GRANT ALL PRIVILEGES ON onphi.* TO 'onphi'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

#### 4. Configuration de l'Application

```bash
# Copier le fichier de configuration local
cp config/autoload/local.php.dist config/autoload/local.php

# Éditer la configuration
nano config/autoload/local.php
```

**Paramètres dans `local.php` :**
```php
return [
    'db' => [
        'driver'   => 'Pdo',
        'dsn'      => 'mysql:dbname=onphi;host=localhost;charset=utf8mb4',
        'username' => 'onphi',
        'password' => 'votre_mot_de_passe',
    ],
];
```

#### 5. Variables d'Environnement

```bash
# Créer le fichier .env
cp .env.example .env

# Éditer les variables
nano .env
```

**Variables essentielles dans `.env` :**
```env
# Database
DB_HOST=localhost
DB_NAME=onphi
DB_USER=onphi
DB_PASS=votre_mot_de_passe

# Microsoft OAuth
CLIENT_ID=votre_client_id
TENANT_ID=votre_tenant_id
CLIENT_SECRET=votre_client_secret
REDIRECT_URL=https://votre-domaine.com/login
GRAPH_USER_SCOPES='User.Read', 'Mail.ReadWrite'

# OpenAI
OPENAI_API_KEY=votre_cle_api_openai

# PayPal
PAYPAL_CLIENT_ID=votre_paypal_client_id
PAYPAL_CLIENT_SECRET=votre_paypal_secret

# OVH API
OVH_APP_KEY=votre_cle_ovh
OVH_APP_SECRET=votre_secret_ovh
OVH_CONSUMER_KEY=votre_consumer_key

# Application
APP_ENV=production
APP_DEBUG=false
APP_URL=https://votre-domaine.com
```

#### 6. Migrations de Base de Données

```bash
# Exécuter les migrations Doctrine
vendor/bin/doctrine-migrations migrations:migrate

# Ou si vous utilisez un autre système
php bin/migrations.php
```

#### 7. Permissions

```bash
# Définir les permissions appropriées
sudo chown -R www-data:www-data .
sudo chmod -R 755 public/
sudo chmod -R 775 data/
sudo chmod -R 775 data/cache/
sudo chmod -R 775 data/logs/
```

### 🌐 **Configuration du Serveur Web**

#### Apache

```apache
<VirtualHost *:80>
    ServerName onphi.org
    ServerAlias www.onphi.org
    DocumentRoot /var/www/onphi.org/web/public
    
    <Directory /var/www/onphi.org/web/public>
        DirectoryIndex index.php
        AllowOverride All
        Require all granted
        
        # Réécriture d'URL
        <IfModule mod_rewrite.c>
            RewriteEngine On
            RewriteCond %{REQUEST_FILENAME} !-f
            RewriteRule ^ index.php [L]
        </IfModule>
    </Directory>
    
    # Logs
    ErrorLog ${APACHE_LOG_DIR}/onphi-error.log
    CustomLog ${APACHE_LOG_DIR}/onphi-access.log combined
</VirtualHost>

# Activer les modules nécessaires
# a2enmod rewrite
# a2enmod headers
# systemctl restart apache2
```

#### Nginx

```nginx
server {
    listen 80;
    server_name onphi.org www.onphi.org;
    root /var/www/onphi.org/web/public;
    index index.php;
    
    # Logs
    access_log /var/log/nginx/onphi-access.log;
    error_log /var/log/nginx/onphi-error.log;
    
    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }
    
    location ~ \.php$ {
        fastcgi_pass unix:/var/run/php/php8.2-fpm.sock;
        fastcgi_index index.php;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        include fastcgi_params;
    }
    
    location ~ /\.ht {
        deny all;
    }
    
    # Assets statiques
    location ~* \.(jpg|jpeg|png|gif|ico|css|js|svg|woff|woff2|ttf|eot)$ {
        expires 1y;
        add_header Cache-Control "public, immutable";
    }
}
```

### 🔧 **Configuration Microsoft OAuth**

Voir la documentation détaillée : [docs/MICROSOFT_OAUTH_README.md](docs/MICROSOFT_OAUTH_README.md)

**Étapes rapides :**
1. Créer une application dans Azure Portal
2. Configurer les URI de redirection
3. Générer un client secret
4. Copier les credentials dans `.env`
5. Configurer les scopes requis

### 🤖 **Configuration OpenAI**

1. Obtenir une clé API sur [platform.openai.com](https://platform.openai.com)
2. Ajouter la clé dans `.env` : `OPENAI_API_KEY=sk-...`
3. Configurer les permissions RBAC pour les utilisateurs autorisés

### 💳 **Configuration PayPal**

1. Créer une application sur [developer.paypal.com](https://developer.paypal.com)
2. Obtenir les credentials (Client ID et Secret)
3. Ajouter dans `.env` :
   ```env
   PAYPAL_CLIENT_ID=votre_client_id
   PAYPAL_CLIENT_SECRET=votre_secret
   PAYPAL_MODE=sandbox  # ou 'live' en production
   ```

### 📧 **Configuration OVH Mailing List**

1. Créer une application sur [eu.api.ovh.com](https://eu.api.ovh.com/createApp/)
2. Obtenir les clés (Application Key, Application Secret, Consumer Key)
3. Configurer dans `.env`

---

## 🚀 Déploiement

### 🖥️ **Déploiement Traditionnel (Serveur Dédié/VPS)**

#### 1. Préparation pour la Production

```bash
# Optimiser l'autoloader
composer install --no-dev --optimize-autoloader

# Activer le mode production
# Éditer .env
APP_ENV=production
APP_DEBUG=false

# Vider tous les caches
./clear-cache-final.sh

# Ou manuellement
rm -rf data/cache/*
php clear-opcache.php
sudo systemctl restart php8.2-fpm
```

#### 2. Optimisations PHP

**Configuration `php.ini` pour la production :**
```ini
; Performances
opcache.enable=1
opcache.memory_consumption=256
opcache.max_accelerated_files=20000
opcache.validate_timestamps=0

; Sécurité
expose_php=Off
display_errors=Off
log_errors=On
error_log=/var/log/php/error.log

; Limites
memory_limit=512M
upload_max_filesize=20M
post_max_size=25M
max_execution_time=300
```

#### 3. Optimisations MySQL

```sql
-- Indexation des tables critiques
ALTER TABLE users ADD INDEX idx_email (email);
ALTER TABLE forum_posts ADD INDEX idx_date (date);
ALTER TABLE shop_products ADD INDEX idx_active (active);

-- Optimisation des tables
OPTIMIZE TABLE users, forum_posts, shop_products;
```

#### 4. SSL/TLS avec Let's Encrypt

```bash
# Installer Certbot
sudo apt install certbot python3-certbot-nginx

# Obtenir un certificat SSL
sudo certbot --nginx -d onphi.org -d www.onphi.org

# Renouvellement automatique
sudo certbot renew --dry-run
```

#### 5. Permissions Finales

```bash
# Propriétaire
sudo chown -R www-data:www-data /var/www/onphi.org/web

# Permissions
find . -type d -exec chmod 755 {} \;
find . -type f -exec chmod 644 {} \;
chmod -R 775 data/
chmod -R 775 public/uploads/
chmod +x clear-cache-final.sh
```

### ☸️ **Déploiement Kubernetes**

Pour un déploiement sur Kubernetes, consultez la documentation complète :
- [📘 Guide Kubernetes](k8s/README.md)
- [🚀 Guide de Déploiement](k8s/DEPLOYMENT.md)

#### Déploiement Rapide

```bash
# Avec Kustomize
kubectl apply -k k8s/overlays/production

# Avec Helm
helm install onphi k8s/helm/onphi \
  -f k8s/helm/onphi/values-production.yaml \
  -n onphi-prod \
  --create-namespace

# Vérifier le déploiement
kubectl get all -n onphi-prod
kubectl logs -f deployment/onphi-app -n onphi-prod
```

#### Caractéristiques du Déploiement K8s

- **Auto-scaling** : HPA configuré (3-10 replicas)
- **Haute disponibilité** : Multi-replicas
- **Stockage persistant** : PVC ou S3
- **Load balancing** : Via Ingress Controller
- **TLS automatique** : cert-manager intégré
- **Monitoring** : Prometheus/Grafana ready

### 🐳 **Déploiement Docker (Development)**

```bash
# Build des images
cd k8s/docker
docker-compose up -d

# Ou avec les scripts
./k8s/scripts/build-images.sh dev false
```

### 🔄 **CI/CD avec GitHub Actions**

Le projet inclut des workflows CI/CD pour :
- **Tests automatisés** sur chaque push
- **Build Docker** automatique
- **Déploiement automatique** par environnement
- **Checks de sécurité** et qualité de code

Voir : `k8s/ci/github-actions.yml`

### 🔐 **Sécurité en Production**

#### Checklist de Sécurité

- [ ] **HTTPS** : SSL/TLS actif
- [ ] **Secrets** : Fichier `.env` sécurisé (chmod 600)
- [ ] **Firewall** : UFW/iptables configuré
- [ ] **Fail2Ban** : Protection contre brute-force
- [ ] **Backups** : Sauvegarde automatique BDD
- [ ] **Updates** : Système et packages à jour
- [ ] **Monitoring** : Logs et alertes actifs
- [ ] **WAF** : Web Application Firewall (optionnel)

#### Configuration Fail2Ban

```bash
# Installer Fail2Ban
sudo apt install fail2ban

# Configuration pour l'application
sudo nano /etc/fail2ban/jail.local
```

```ini
[onphi-auth]
enabled = true
port = http,https
filter = onphi-auth
logpath = /var/www/onphi.org/web/data/logs/application.log
maxretry = 5
bantime = 3600
```

---

## 📊 Monitoring & Logs

### 📝 **Logs de l'Application**

#### Emplacements des Logs

| Type de Log | Emplacement | Description |
|------------|-------------|-------------|
| **Application** | `data/logs/application.log` | Logs applicatifs Laminas |
| **PHP Errors** | `data/logs/php-error.log` | Erreurs PHP |
| **Access** | `/var/log/nginx/onphi-access.log` | Accès HTTP (Nginx) |
| **Error** | `/var/log/nginx/onphi-error.log` | Erreurs HTTP (Nginx) |
| **Bot/IA** | `data/logs/bot.log` | Conversations OpenAI |
| **Auth** | `data/logs/auth.log` | Authentification |

#### Rotation des Logs

```bash
# Configuration logrotate
sudo nano /etc/logrotate.d/onphi
```

```
/var/www/onphi.org/web/data/logs/*.log {
    daily
    missingok
    rotate 14
    compress
    delaycompress
    notifempty
    create 0640 www-data www-data
    sharedscripts
}
```

### 📈 **Monitoring & Performance**

#### Scripts de Monitoring

```bash
# Monitoring général
php tests/test-all-pages.php           # Test toutes les pages
php tests/test-pages-status.php        # Vérification HTTP status
php tests/test-performance.php         # Test de performance

# Monitoring spécifique
php tests/test-authentication-*.php    # Tests d'authentification
php tests/test-database-queries.php    # Optimisation requêtes DB
```

#### Métriques à Surveiller

- **Temps de réponse** : < 200ms pour les pages statiques
- **Requêtes BDD** : < 50 queries par page
- **Mémoire PHP** : < 128MB par requête
- **OPcache Hit Rate** : > 95%
- **Erreurs 500** : 0 par jour
- **Uptime** : > 99.9%

#### Tools de Monitoring Recommandés

- **Prometheus + Grafana** : Métriques et dashboards
- **New Relic** : APM complet
- **Sentry** : Tracking d'erreurs
- **UptimeRobot** : Monitoring uptime
- **Google Analytics** : Analytics web

### 🔍 **Outils de Diagnostic**

#### Interface Web

Accessible via l'administration : `/admin/`

- **phpinfo** : `/admin/phpinfo` - Configuration PHP
- **Tests** : `/admin/tests` - Exécution des tests
- **Cache** : `/admin/cache` - Gestion du cache
- **Logs** : Consultation en temps réel

#### Ligne de Commande

```bash
# Status des services
sudo systemctl status php8.2-fpm
sudo systemctl status nginx
sudo systemctl status mysql

# Monitoring des ressources
htop                          # Processus et ressources
iotop                        # I/O disque
mysqladmin -u root -p status # Status MySQL

# Logs en temps réel
tail -f data/logs/application.log
tail -f /var/log/nginx/onphi-error.log
```

### 📊 **Dashboards Personnalisés**

#### Grafana Dashboard (exemple)

```yaml
# Métriques principales
- Requêtes/sec
- Temps de réponse moyen
- Erreurs 4xx/5xx
- Utilisation CPU/RAM
- Connexions BDD actives
- Cache hit rate
- Utilisateurs actifs
```

---

## 🔧 Maintenance

### 🔄 **Tâches Régulières**

#### Quotidien
```bash
# Vérifier les logs d'erreurs
tail -n 100 data/logs/application.log | grep ERROR

# Vérifier l'espace disque
df -h

# Vérifier les processus
ps aux | grep php-fpm
```

#### Hebdomadaire
```bash
# Optimiser la base de données
mysql -u root -p onphi -e "OPTIMIZE TABLE users, forum_posts, shop_products"

# Nettoyer les logs anciens
find data/logs/ -name "*.log" -mtime +30 -delete

# Vérifier les sauvegardes
ls -lah /backup/onphi/

# Mettre à jour les dépendances
composer update --with-dependencies
```

#### Mensuel
```bash
# Analyser les performances
php tests/test-performance.php > reports/perf-$(date +%Y%m).txt

# Vérifier la sécurité
composer audit

# Mettre à jour le système
sudo apt update && sudo apt upgrade

# Analyser les logs
awstats /etc/awstats/onphi.org.conf
```

### 💾 **Sauvegardes**

#### Script de Sauvegarde Automatique

```bash
#!/bin/bash
# /var/www/onphi.org/backup.sh

DATE=$(date +%Y%m%d_%H%M%S)
BACKUP_DIR="/backup/onphi"
WEB_DIR="/var/www/onphi.org/web"

# Créer le répertoire de sauvegarde
mkdir -p $BACKUP_DIR

# Sauvegarde de la base de données
mysqldump -u onphi -p'password' onphi | gzip > $BACKUP_DIR/db_$DATE.sql.gz

# Sauvegarde des fichiers
tar -czf $BACKUP_DIR/files_$DATE.tar.gz \
  -C $WEB_DIR \
  --exclude='data/cache/*' \
  --exclude='data/logs/*' \
  --exclude='vendor' \
  .

# Sauvegarde des uploads
tar -czf $BACKUP_DIR/uploads_$DATE.tar.gz \
  -C $WEB_DIR/public \
  uploads/

# Nettoyer les anciennes sauvegardes (> 30 jours)
find $BACKUP_DIR -name "*.gz" -mtime +30 -delete

echo "Backup completed: $DATE"
```

#### Cron pour Sauvegardes Automatiques

```bash
# Éditer le crontab
crontab -e

# Sauvegarde quotidienne à 2h du matin
0 2 * * * /var/www/onphi.org/backup.sh >> /var/log/backup.log 2>&1
```

#### Restauration

```bash
# Restaurer la base de données
gunzip < /backup/onphi/db_20250122_020000.sql.gz | mysql -u onphi -p onphi

# Restaurer les fichiers
tar -xzf /backup/onphi/files_20250122_020000.tar.gz -C /var/www/onphi.org/web/

# Restaurer les uploads
tar -xzf /backup/onphi/uploads_20250122_020000.tar.gz -C /var/www/onphi.org/web/public/
```

### 🔄 **Mises à Jour**

#### Mise à Jour de l'Application

```bash
# 1. Sauvegarder
./backup.sh

# 2. Mode maintenance
touch public/maintenance.flag

# 3. Récupérer les changements
git pull origin main

# 4. Mettre à jour les dépendances
composer install --no-dev --optimize-autoloader

# 5. Migrations de BDD
vendor/bin/doctrine-migrations migrations:migrate

# 6. Vider le cache
./clear-cache-final.sh

# 7. Désactiver le mode maintenance
rm public/maintenance.flag

# 8. Vérifier
php tests/test-all-pages.php
```

#### Mise à Jour des Dépendances

```bash
# Vérifier les updates disponibles
composer outdated

# Mettre à jour (avec précaution)
composer update

# Tester après mise à jour
php tests/test-all-pages.php
```

### ⚠️ **Troubleshooting**

#### Problèmes Courants

**1. Erreur 500 - Internal Server Error**
```bash
# Vérifier les logs
tail -n 50 data/logs/application.log
tail -n 50 /var/log/nginx/onphi-error.log

# Vérifier les permissions
ls -la public/
ls -la data/

# Vider le cache
./clear-cache-final.sh
```

**2. Page Blanche**
```bash
# Activer le mode debug
# Dans .env : APP_DEBUG=true

# Vérifier PHP-FPM
sudo systemctl status php8.2-fpm
sudo tail -f /var/log/php8.2-fpm.log
```

**3. Erreurs de Base de Données**
```bash
# Tester la connexion
mysql -u onphi -p onphi

# Vérifier les connexions actives
mysql -u root -p -e "SHOW PROCESSLIST;"

# Redémarrer MySQL
sudo systemctl restart mysql
```

**4. Problèmes de Performance**
```bash
# Vérifier OPcache
php -i | grep opcache

# Réinitialiser OPcache
php clear-opcache.php

# Vérifier les ressources
htop
```

---

## 🤝 Contribution

Nous accueillons les contributions de la communauté ! Voici comment participer au développement du projet.

### 📋 **Workflow de Contribution**

#### 1. Préparer l'Environnement

```bash
# Forker le repository sur GitHub

# Cloner votre fork
git clone https://github.com/votre-username/web.git
cd web

# Ajouter le repository upstream
git remote add upstream https://github.com/onphi/web.git

# Créer une branche pour votre fonctionnalité
git checkout -b feature/ma-nouvelle-fonctionnalite
```

#### 2. Développer

```bash
# Faire vos modifications
# ...

# Tester localement
php tests/test-all-pages.php
composer test  # Si configuré

# Vérifier le code style
composer phpcs  # Si configuré
```

#### 3. Commit & Push

```bash
# Ajouter vos changements
git add .

# Commit avec un message descriptif
git commit -m "feat: ajout de la fonctionnalité X

- Description détaillée
- Points importants
- Fixes #123"

# Push vers votre fork
git push origin feature/ma-nouvelle-fonctionnalite
```

#### 4. Pull Request

1. Aller sur GitHub
2. Créer une Pull Request vers `main`
3. Décrire vos changements
4. Attendre la review
5. Apporter les modifications demandées

### 📝 **Standards de Code**

#### PHP
- **Standard** : PSR-12
- **Documentation** : PHPDoc pour toutes les méthodes publiques
- **Type Hinting** : Utiliser les types stricts
- **Namespaces** : Suivre la structure PSR-4

```php
<?php

declare(strict_types=1);

namespace Application\Controller;

use Laminas\Mvc\Controller\AbstractActionController;
use Laminas\View\Model\ViewModel;

/**
 * Contrôleur pour la gestion des exemples
 */
class ExempleController extends AbstractActionController
{
    /**
     * Action d'index
     * 
     * @return ViewModel
     */
    public function indexAction(): ViewModel
    {
        return new ViewModel([
            'data' => $this->getData(),
        ]);
    }
}
```

#### JavaScript
- **Standard** : ES6+
- **Format** : Prettier
- **Linter** : ESLint
- **Documentation** : JSDoc

```javascript
/**
 * Initialise le module forum
 * @param {Object} options - Options de configuration
 * @returns {void}
 */
function initForum(options) {
    const defaults = {
        autoLoad: true,
        perPage: 10
    };
    
    const config = { ...defaults, ...options };
    // ...
}
```

#### CSS
- **Méthodologie** : BEM (Block Element Modifier)
- **Variables** : Utiliser les CSS custom properties
- **Responsive** : Mobile-first
- **Organisation** : Fichiers modulaires

```css
/* Block */
.forum-post { }

/* Element */
.forum-post__title { }
.forum-post__content { }

/* Modifier */
.forum-post--featured { }
.forum-post--archived { }
```

#### Templates (phtml)
- **Indentation** : 4 espaces
- **Échappement** : Toujours échapper les variables
- **Helpers** : Utiliser les view helpers Laminas

```php
<?php
$this->headTitle($this->translate('Page Title'));
?>

<div class="onphi-content-section">
    <h1><?= $this->escapeHtml($title) ?></h1>
    <p><?= $this->escapeHtml($description) ?></p>
    
    <?php if ($items): ?>
        <ul class="onphi-list">
            <?php foreach ($items as $item): ?>
                <li><?= $this->escapeHtml($item) ?></li>
            <?php endforeach; ?>
        </ul>
    <?php endif; ?>
</div>
```

### 🧪 **Tests**

#### Écrire des Tests

```bash
# Créer un nouveau fichier de test
touch tests/test-ma-fonctionnalite.php
```

```php
<?php
/**
 * Test de la nouvelle fonctionnalité
 */

require_once __DIR__ . '/../vendor/autoload.php';

// Test 1: Vérifier que...
echo "Test 1: Fonctionnalité X... ";
$result = testFonctionnaliteX();
echo $result ? "✅ PASS\n" : "❌ FAIL\n";

// Test 2: Vérifier que...
echo "Test 2: Fonctionnalité Y... ";
$result = testFonctionnaliteY();
echo $result ? "✅ PASS\n" : "❌ FAIL\n";

echo "\n✅ Tous les tests sont passés!\n";
```

#### Exécuter les Tests

```bash
# Tests individuels
php tests/test-ma-fonctionnalite.php

# Suite complète
php tests/test-all-pages.php

# Tests spécifiques
php tests/test-forum-*.php
php tests/test-shop-*.php
```

### 📚 **Documentation**

#### Documenter les Changements

- **Code** : Commentaires et PHPDoc
- **README** : Mettre à jour si nécessaire
- **Docs** : Créer un fichier `.md` dans `docs/`
- **CHANGELOG** : Ajouter une entrée

#### Format des Documents

```markdown
# Titre de la Fonctionnalité

## Description

Brève description de la fonctionnalité.

## Utilisation

### Exemple 1
\```php
// Code exemple
\```

### Exemple 2
\```php
// Code exemple
\```

## Configuration

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `option1` | `string` | `'default'` | Description |

## Tests

\```bash
php tests/test-fonctionnalite.php
\```

## Notes

- Point important 1
- Point important 2
```

### 🐛 **Rapporter des Bugs**

#### Template d'Issue

```markdown
### Description
Description claire du bug

### Étapes pour Reproduire
1. Aller à...
2. Cliquer sur...
3. Voir l'erreur

### Comportement Attendu
Ce qui devrait se passer

### Comportement Actuel
Ce qui se passe réellement

### Environnement
- OS: Ubuntu 22.04
- PHP: 8.2.10
- Navigateur: Chrome 120

### Logs
\```
[Logs pertinents]
\```

### Screenshots
[Si applicable]
```

### 💡 **Proposer des Fonctionnalités**

#### Template de Feature Request

```markdown
### Problème à Résoudre
Description du besoin

### Solution Proposée
Description de la solution

### Alternatives Considérées
Autres approches possibles

### Contexte Additionnel
Informations supplémentaires
```

### 🏆 **Contributeurs**

Merci à tous les contributeurs qui ont participé au développement de ce projet !

<!-- 
Ajoutez votre nom ici après votre première contribution :
- [Votre Nom](https://github.com/username) - Description
-->

---

## 📞 Support & Contact

### 📚 **Ressources**

| Ressource | Lien | Description |
|-----------|------|-------------|
| **Documentation** | [`docs/`](docs/) | 80+ documents techniques |
| **Tests** | [`tests/`](tests/) | Scripts de test et diagnostic |
| **Issues** | [GitHub Issues](#) | Rapporter des bugs |
| **Discussions** | [GitHub Discussions](#) | Questions et discussions |
| **Wiki** | [GitHub Wiki](#) | Guides et tutoriels |

### 💬 **Obtenir de l'Aide**

#### 1. Consulter la Documentation
- Parcourir le dossier [`docs/`](docs/)
- Lire les guides spécifiques à votre problème
- Vérifier les fichiers `README-*.md` à la racine

#### 2. Utiliser les Outils de Diagnostic
```bash
# Tests généraux
php tests/test-all-pages.php

# Tests spécifiques
php tests/test-forum-diagnosis.php
php tests/test-shop-*.php

# Vérifier les logs
tail -f data/logs/application.log
```

#### 3. Rechercher dans les Issues
- Vérifier si le problème est déjà reporté
- Consulter les issues fermées pour les solutions

#### 4. Poser une Question
- Ouvrir une **Discussion** pour les questions générales
- Ouvrir une **Issue** pour les bugs
- Fournir le maximum d'informations (logs, environnement, étapes)

### 📧 **Contact Direct**

| Contact | Usage |
|---------|-------|
| **Email** | [contact@onphi.org](mailto:contact@onphi.org) |
| **Site Web** | [https://onphi.org](https://onphi.org) |
| **Admin** | Via interface `/admin/` |

### 🆘 **Support d'Urgence**

Pour les problèmes critiques en production :
1. Consulter les logs : `data/logs/application.log`
2. Activer le mode maintenance si nécessaire
3. Contacter l'équipe technique : [tech@onphi.org](mailto:tech@onphi.org)
4. Restaurer depuis backup si nécessaire

---

## 📄 Licence

Ce projet est sous licence **MIT**.

```
MIT License

Copyright (c) 2025 Organisation Non-Philosophique Internationale (ONPhI)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

Voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 🎯 Statut du Projet

### 📊 **Vue d'Ensemble**

![GitHub last commit](https://img.shields.io/github/last-commit/onphi/web)
![GitHub issues](https://img.shields.io/github/issues/onphi/web)
![GitHub pull requests](https://img.shields.io/github/issues-pr/onphi/web)

**Version Actuelle** : `2.0.0`  
**Statut** : 🟢 Production Active  
**Dernière MAJ** : Janvier 2025

### ✅ **Fonctionnalités Complètes**

#### Core Application
- [x] **Framework Laminas** : Architecture MVC complète
- [x] **Doctrine ORM** : Mapping objet-relationnel
- [x] **Multilingue** : 9 langues supportées
- [x] **RBAC** : Système de permissions granulaires
- [x] **Sessions sécurisées** : Gestion des utilisateurs

#### Modules Fonctionnels
- [x] **Boutique en ligne** : Catalogue, panier, paiement PayPal
- [x] **Forum modernisé** : 125+ posts, BBCode, filtres
- [x] **École de Non-Philosophie** : Séminaires, ressources, inscriptions
- [x] **Authentification OAuth** : Microsoft Graph API
- [x] **Contenus philosophiques** : Lettres, chroniques, corpus, bibliothèque
- [x] **Multimédia** : Audio (Laruelle Sonore), vidéo, radio

#### Intelligence Artificielle
- [x] **ChatGPT** : Chatbot conversationnel
- [x] **DALL-E 3** : Génération d'images
- [x] **Whisper** : Transcription audio
- [x] **TTS** : Text-to-Speech (6 voix)
- [x] **GPT-4 Vision** : Analyse d'images

#### Interface & Design
- [x] **Design System unifié** : Classes CSS `onphi-*`
- [x] **Responsive** : Mobile, tablet, desktop
- [x] **Bootstrap 5** : Framework CSS moderne
- [x] **FontAwesome** : Bibliothèque d'icônes
- [x] **CSS optimisé** : 70% de réduction de taille

#### Administration
- [x] **Dashboard complet** : Gestion centralisée
- [x] **Gestion utilisateurs** : Membres, rôles, cotisations
- [x] **Gestion contenu** : CMS complet
- [x] **Outils diagnostic** : phpinfo, tests, logs
- [x] **Mailing list** : Intégration OVH API

#### DevOps & Infrastructure
- [x] **Kubernetes** : Manifests complets (base + overlays)
- [x] **Helm Charts** : Déploiement automatisé
- [x] **Docker** : Conteneurisation
- [x] **CI/CD** : GitHub Actions
- [x] **Monitoring** : Logs et métriques

#### Documentation
- [x] **80+ documents** : Documentation exhaustive
- [x] **Guides techniques** : Installation, déploiement, maintenance
- [x] **Tests** : 100+ scripts de test
- [x] **README complet** : Ce fichier

### 🔄 **En Cours de Développement**

#### Performance
- [ ] **Cache Redis** : Implémentation du cache distribué
- [ ] **CDN** : Intégration CDN pour les assets
- [ ] **Lazy Loading** : Optimisation chargement images
- [ ] **Service Workers** : PWA capabilities

#### Fonctionnalités
- [ ] **Sora Video** : Génération vidéo (quand disponible)
- [ ] **API REST** : Documentation OpenAPI/Swagger
- [ ] **Webhooks** : Notifications temps réel
- [ ] **Search** : Recherche full-text Elasticsearch

#### Tests & Qualité
- [ ] **Tests unitaires** : PHPUnit complet
- [ ] **Tests d'intégration** : Behat/Codeception
- [ ] **Tests E2E** : Cypress/Playwright
- [ ] **Coverage** : > 80% de couverture de code

#### Sécurité
- [ ] **2FA** : Authentification à deux facteurs
- [ ] **WAF** : Web Application Firewall
- [ ] **Rate Limiting** : Protection contre les abus
- [ ] **Security Headers** : CSP, HSTS, etc.

### 🔮 **Roadmap Future**

#### Q1 2025
- [ ] **API REST v1** : Endpoints publics documentés
- [ ] **Application mobile** : Version React Native
- [ ] **Analytics avancées** : Dashboard personnalisé
- [ ] **Notifications push** : Web Push API

#### Q2 2025
- [ ] **Intégration Stripe** : Alternative à PayPal
- [ ] **Système de tickets** : Support client
- [ ] **Newsletter** : Intégration Mailchimp/SendGrid
- [ ] **Forum avancé** : Markdown, réactions, mentions

#### Q3 2025
- [ ] **Marketplace** : Vente de contenus tiers
- [ ] **Live Streaming** : Conférences en direct
- [ ] **Gamification** : Badges, niveaux, récompenses
- [ ] **Social Features** : Profils, followers, feed

#### Q4 2025
- [ ] **Machine Learning** : Recommandations personnalisées
- [ ] **Blockchain** : NFTs pour contenus exclusifs
- [ ] **VR/AR** : Expériences immersives
- [ ] **Voice Interface** : Assistant vocal

### 📈 **Métriques du Projet**

| Métrique | Valeur |
|----------|--------|
| **Lignes de Code** | ~150,000+ |
| **Fichiers PHP** | 500+ |
| **Templates** | 200+ |
| **Documents** | 80+ |
| **Scripts de Test** | 100+ |
| **Routes** | 150+ |
| **Contrôleurs** | 50+ |
| **Entités Doctrine** | 30+ |
| **Services** | 40+ |
| **Commits** | 1000+ |

### 🏆 **Réalisations**

- ✅ **Refonte complète** du forum (Interface moderne)
- ✅ **Uniformisation** du design system (Classes CSS unifiées)
- ✅ **Intégration IA** complète (OpenAI API)
- ✅ **Infrastructure K8s** complète (Production-ready)
- ✅ **Documentation exhaustive** (80+ docs)
- ✅ **Optimisation CSS** (70% de réduction)
- ✅ **Tests automatisés** (100+ scripts)
- ✅ **Multilingue** (9 langues)

---

## 📌 Informations Complémentaires

### 🔗 **Liens Utiles**

- **Site Web** : [https://onphi.org](https://onphi.org)
- **Documentation** : [docs/](docs/)
- **Tests** : [tests/](tests/)
- **Kubernetes** : [k8s/](k8s/)
- **Repository** : [GitHub](https://github.com/onphi/web)

### 🎓 **À Propos de la Non-Philosophie**

La **non-philosophie** est un courant de pensée développé par **François Laruelle** qui propose une alternative radicale à la philosophie traditionnelle. Elle cherche à penser depuis le réel plutôt que depuis les concepts philosophiques.

**Ressources** :
- [Lettres de François Laruelle](https://onphi.org/fr/lettres)
- [Chroniques non-épistémologiques](https://onphi.org/fr/chroniques)
- [École de Non-Philosophie](https://onphi.org/fr/school)

### 👥 **Équipe**

**Organisation Non-Philosophique Internationale (ONPhI)**
- Fondateur : François Laruelle
- Développement web : Équipe technique ONPhI
- Contributeurs : Voir [CONTRIBUTORS.md](CONTRIBUTORS.md)

---

<div align="center">

**🌐 ONPhI - Organisation Non-Philosophique Internationale**

*Promouvoir et développer la non-philosophie à travers le monde*

[![Website](https://img.shields.io/badge/Website-onphi.org-blue)](https://onphi.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?logo=php)](https://php.net)
[![Laminas](https://img.shields.io/badge/Laminas-Framework-68B604)](https://getlaminas.org)

**Dernière mise à jour** : Novembre 2025 | **Version** : 6.0.4

*Développé avec ❤️ pour la philosophie non-standard*

</div>
