Organisation du projet avec Trello
Pour gérer efficacement le projet EcoRide, j’ai utilisé l’outil de gestion de tâches Trello. Il m’a permis de suivre l’évolution du développement
et de mieux organiser les différentes étapes du projet. Trello fonctionne selon la méthode Kanban, avec des listes et des cartes.
Il aide à visualiser l’avancement du projet, permet de prioriser les tâches à faire
Donne une vision claire des étapes restantes, favorise une meilleure gestion du temps et du rendu final.

Diagramme réalisé avec draw.io
Pour modéliser les fonctionnalités principales de la plateforme EcoRide, un diagramme de cas d’utilisation a été réalisé à l’aide de l’outil draw.io.
Ce diagramme permet de visualiser les interactions entre les différents acteurs du système et les cas d’usage associés.
Visiteur : peut consulter les covoiturages disponibles via les filtres, accéder au détail d’un trajet, et s’inscrire pour devenir utilisateur.
Utilisateur : peut proposer un trajet, participer à un trajet, consulter les détails, gérer ses crédits, etc.
Employé : responsable de la validation et/ou refus des trajets proposer ainsi que avis etc..
Administrateur : peut consulter des graphiques statistiques (crédit et covoiturage), créer et gérer des comptes employés et utilisateur.
Navigation via le menu principal et le formulaire de recherche.
Connexion / inscription, avec distinction entre compte chauffeur et participant.
Interaction autour de la participation, validation, mise à jour des crédits, envoi ou annulation d’e-mails.
Gestion de l’information de covoiturage tout au long du trajet (démarrer, arriver à destination, etc.).

Conception des wireframes avec Balsamiq
Dans le cadre du projet EcoRide, j’ai utilisé Balsamiq Wireframes pour concevoir les premières versions des interfaces du site. 
Il s'agit de wireframes, c’est-à-dire des schémas simples permettant de visualiser rapidement la structure des pages avant la phase de développement.
Objectifs des wireframes
Structurer l’interface utilisateur, Définir le parcours utilisateur
Identifier les zones fonctionnelles principales (recherche, formulaire, tableau, etc.)
Valider l’ergonomie avec un rendu rapide et épuré

Les wireframes créés avec Balsamiq incluent :
Page d’accueil, recherche de trajets, détail d’un trajet
c'est un interface simple à utiliser, même sans compétence en design
Représentation visuelle rapide des idées
Idéal pour la phase de réflexion UX/UI
Permet d’éviter les erreurs de conception en amont

Utilisation de Figma pour les mockups.
Pour concevoir l’interface utilisateur du projet EcoRide, j’ai utilisé Figma, un outil de design collaboratif en ligne. Cela m’a permis de :
Créer des maquettes visuelles précises avant le développement, facilitant la planification et l’organisation du contenu.
Expérimenter différents layouts, couleurs et styles pour améliorer l’ergonomie et l’expérience utilisateur.
Obtenir un aperçu clair du rendu final attendu, ce qui a guidé la réalisation des pages en HTML et CSS.
Cette étape a été essentielle pour assurer une interface cohérente et professionnelle, tout en optimisant le temps de développement.

Front-end
Validation des formulaires via HTML5 :
Utilisation des attributs natifs comme required, type="email".
Cette validation côté client permet d’éviter les erreurs simples sans charger le serveur inutilement.
Les données affichées sont échappées côté PHP pour éviter toute injection de code malveillant.
Design et ergonomie :.
HTML et CSS ont été employés pour traduire ce design en pages web responsives et accessibles.
Organisation du front :
Structure des dossiers claire avec séparation des fichiers HTML, CSS, images, facilitant la maintenance et la compréhension du projet.

Back-End
PHP (PDO) : pour la gestion sécurisée de la base de données avec MySQL, évitant les injections SQL grâce aux requêtes préparées.
MySQL / MariaDB : base de données relationnelle robuste, hébergée sur Alwaysdata.
FTP (FileZilla) : outil de transfert des fichiers vers le serveur de production Alwaysdata.
Serveur Alwaysdata : hébergement web performant avec accès à une base de données distante.
Gestion des erreurs avec try-catch pour éviter la divulgation d’informations sensibles.
Stockage des fichiers de configuration (ex : db.php) dans un dossier non accessible directement par URL.

Justification des choix :
PHP est largement supporté, simple à mettre en œuvre, et compatible avec de nombreux hébergeurs. PDO assure la sécurité des requêtes SQL.
HTML/CSS sont standards du web, garantissant la compatibilité entre navigateurs. Alwaysdata est une solution facile pour déployer une application web avec base distante.

Mise en place de l’environnement de travail:
Local : installation de XAMPP pour simuler un environnement serveur local avec Apache, PHP et MySQL, permettant tests et développement sans connexion internet.
Production : hébergement sur Alwaysdata, transfert des fichiers via FTP et gestion de la base via phpMyAdmin.

Organisation : séparation claire des dossiers front-end (ex : /EcoRide) et back-end (ex : /EcoRide/back) pour faciliter la maintenance et renforcer la sécurité.

Justification :
Le double environnement garantit un développement efficace et un déploiement fiable. Le découpage des dossiers permet de protéger les fichiers sensibles et d’organiser le projet.

Informations complémentaires
En raison d’un manque de temps, je n’ai pas pu intégrer de JavaScript dans ce projet, ce qui limite certaines interactions dynamiques côté front-end. De plus,
il me manque encore quelques petits détails fonctionnels et techniques qui étaient spécifiés dans les User Stories (US). Ces points pourront être améliorés et complétés dans 
une future évolution du projet.

lien deploiement : https://ecoride-jodie.alwaysdata.net/EcoRide/

Informations de déploiement :
Le site EcoRide a été déployé avec succès sur l’hébergement Alwaysdata.
La base de données (ecoride-jodie_sql) a été importée sur le serveur et est disponible via phpMyAdmin.
Limitation actuelle : la connexion entre l’application PHP et la base distante ne fonctionne pas encore (erreur de connexion PDO), donc les fonctionnalités dynamiques dépendantes
de la BDD sont inactives. En revanche, la partie HTML/CSS du site est pleinement accessible en ligne et permet de visualiser l’interface utilisateur.
Une correction de la configuration PDO (hôte, identifiants MySQL, droits, etc.) est planifiée dans une prochaine mise à jour.
