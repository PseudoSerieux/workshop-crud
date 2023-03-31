# Installation

Le projet utilise la dernière version de WORDPRESS (6.2)

## Landing Page de présentation

Lien d'accès à la Landing Page : https://pseudoserieux.github.io/workshop-crud.github.io/

## Pré-requis

Avant toute chose, vous devez installer une instance Wordpress. La plupart des hébergeurs proposent des solutions automatiques. Sinon il vous est possible de l'installer en téléchargeant les fichiers depuis le site officiel ou avec docker.

- Installer Wordpress avec la méthode de votre choix.

(Téléchargez les fichiers, Docker compose)

- Installer un système de base de données

(MySQL)

- Lancer le site

- Suivez les indications d'installation (Les réglages sont à faire en fonction de votre projet)

## Extension - Jetpack CRM

Voici les instructions quant à l'installation du plugin Jetpack CRM sur wordpress. Pour ceci, vous devez avoir une installation complète et un Wordpress qui est lancé.

Pour Wordpress, ne prenez que des extensions de confiance ! Ou mis à jour récemment pour éviter des failles de sécurités

- Pour installer l'extension, rendez vous dans l'administration puis "Extensions > Ajouter" et rechercher Jetpack CRM (à ne pas confondre avec l'extension Jetpack tout court)

- Ensuite, cliquez sur "Installer maintenant". Attendez quelques instants puis le bouton affichera "Activer", cliquez alors dessus une nouvelle fois pour l'activer sur le Wordpress

## Installation - Jetpack CRM

Une fois le plugin activé, une nouvelle page s'ouvre pour lancer la configuration d'installation du plugin.

- L'étape "Essentials" est à configurer en fonction de votre client. Le seul point à réfléchir est le "Menu Style", à vous de voir si vous préférez n'avoir que les options du CRM ("Jetpack CRM Override"), un item de menu Jetpack ("Jetpack CRM Slimline") ou tous les items de menu aux mêmes niveaux ("Jetpack CRM & Wordpress"). Le plus simple, pour un client qui n'a pas besoin de site front-end (vitrine), mais juste du CRM c'est de prendre "Jetpack CRM Override". Une fois finis, cliquez sur "Next".

- L'étape "Your Contats" permet de connecter votre CRM vers d'autres systèmes pour importer des contact. Si pas besoin, vous pouvez cliquer sur "Next".

- L'étape "Wich Extensions?" vous laisse le choix d'activer des extensions supplémentaire, toujours en fonction des besoins de votre client. A-t-il besoin de gérer des devis, des factures ou mettre en relation avec WooCommerce. Une fois les choix faits, cliquez sur "Next".

- L'étape "Finish" est optionnelle, enlevez les informations pré-remplies si vous ne voulez pas être abonné aux informations mail de Jetpack CRM. Cliquez sur "Next".

## Configuration - Jetpack CRM

Lorsque le plugin est installé, il reste des réglages à mettre en place pour être sûr que tout fonctionne correctement.

- Dans le menu d'administration : "Jetpack CRM > CRM Settings"

---

- Tous les paramètres sont à changer en fonction des besoins de votre client. Les étapes, suivantes sont dans le cadre d'un client qui ne souhaite qu'un CRM et pas de front-end client

- Dans la partie "WordPress Override Mode" :

- Cochez "Override WordPress"

- Cochez "Override WordPress (For All WP Users)"

- Modifiez le "Login Logo Override" avec l'image du client

- Vous pouvez re-modifier le nom si besoin avec "Custom CRM Header"

- Cochez "Disable Front-End", cela va enlever l'aspect vitrine de Wordpress pour n'avoir qu'une page de connexion disponible

- Décochez "Show admin credits" pour épurer l'interface

---

- Lors de l'ajoute d'un Contacts, sur le formulaire, si vous souhaitez lier avec une entreprise pour la première fois, vous ne pourrez pas sans une petite configuration

- Dans le formulaire d'ajout, sur le bloc "Company", un message en rouge s'affiche "You are using Plain Permalinks. Please set your permalinks to %postname% by visiting here", cliquez sur le "here"

- Dans la page qui s'ouvre, sélectionner "Structure personalisée" et ajouter dans le champ texte : %postname%

- Cliquez sur enregistrer les modifications

- Revenez à l'ajout d'un contact, normalement, vous pouvez lier avec une entreprise

## Design

De nombreux plugin existe pour modifier l'aspect graphique de l'interface. À vous de choisir celui qui vous correspond le mieux.

- Rendez-vous sur le lien /wp-admin/plugin-install.php de votre wordpress, il s'agit de la page d'installation des plugins

- Prenons en exemple le plugin "Zephyr Admin Theme", chercher le puis "Installer maintenant" et "Activer"

- Une fois activer vous êtes redirigé vers la liste de vos extensions, sur la ligne Zephyr Admin Theme, cliquer sur "Customization Settings"

- Sur la page de réglage, vous aurez le choix des couleurs, de la police, des images. Chaque plugin va offrir plus ou moins de paramètres. Pour aller plus loin, vous pouvez développer un plugin de personnalisation

## Traduction

Mon interface est en anglais ! Que faire ?

Si vous souhaitez traduire votre interface, vous pouvez suivre ce point rapide sur l'installation d'un plugin de traduction. Jetpack CRM n'est pas encore traduit à 100% en FR. La traduction est open-source et peut donc être complété par la communauté.

- Rendez-vous sur le lien /wp-admin/plugin-install.php de votre Wordpress, il s'agit de la page d'installation des plugins

- Recherchez "Loco Translate", puis "Installer maintenant" et "Activer"

- Etape non obligatoire : Répétez l'action pour l'extension "Automatic Translate Addon For Loco Translate". Non obligatoire car "Loco Translate" propose des solutions de traduction automatique mais payant (ou essai gratuit). Celui-ci propose une solution gratuite mais peu fiable

- Un item a été ajouté dans le menu d'administration. Pour traduire : "Loco Translate > Extensions > Jetpack CRM > Nouvelle langue". Sélectionner le Français et laissez par défaut le reste

- Un tableau va s'ouvrir dans lequel vous pouvez traduire tous les textes du plugin

### Conseils

- Gardez votre Wordpress et vos extensions à jour

- Attention aux extensions que vous installez. Plus vous avez d'extensions, plus le risque de faille est grand

- Installez des plugins de sécurité (pour changer le lien de la page de login, bloquer les tentatives de connexion, ajouter la double auth)

- Installez un système de backup pour pouvoir récupérer votre site
