# Kaufman & Broad : procédure de déploiement du Compositeur Digital

*Cette procédure est valable pour la phase de production à partir de S2 2017*

## Prérequis matériel et réseau
- Ordinateur / tablette tactile, Intel Core i5 ou supérieur, SSD 128 Go minimum.
- Windows 10 (Anniversary update ou supérieur).
- Connexion internet, lors de l'installation, mais aussi lors de l'utilisation pour la mise à jour des contenus.

## Prérequis mode "kiosque"
- Verouillage de l'environnement shell Windows (exemple de logiciel : Frontface Lockdown).
- Logiciel de type watchdog pour surveiller et relancer le Compositeur Digital en cas d'arrêt non prévu (exemple de logiciel : restartoncrash).
- Arrêt/démarrage automatique matin et soir (*heures à déterminer avec K&B*).
- Pas de mise en veille en journée (l'économiseur d'écran est intégré au Compositeur Digital).

## Installation
### 1. Configurer OneDrive
Suivre [odopen://sync?siteId=81e54911-7a51-4381-9a78-ebac847930e0&webId=79131da9-a1ae-47be-ad30-4811761797a9&webTitle=Kaufman%20%26%20Broad&listId=53da5f90-032a-4f3a-a9ce-cbaef89af6db&listTitle=Documents&userEmail=ketb@compositeurdigital.com&webUrl=https://insideso.sharepoint.com/sites/KetB&webLogoUrl=/sites/KetB/_api/GroupService/GetGroupImage%3Fid%3D'b640569c-b521-498d-824c-a5431de92270'%26hash%3D636354440941239942&webTemplate=GROUP&folderUrl=/&scope=OPENLIST](ce lien) et appliquer la configuration par défaut.

**_Remarque : la synchronisation initiale provoque le téléchargement de plusieurs dizaines de Go de données : elle ne doit pas être faite sur site K&B. Seules les mises à jour différentielles sont faites sur site K&B._**

### 2. Installer Compositeur Digital
En ligne à partir de l'adresse [http://www.compositeurdigital.com/deploy/ketb](http://www.compositeurdigital.com/deploy/ketb).

### 3. Configurer démarrage/watchdog
Démarrage automatique du Compositeur Digital et/ou du watchdog à l'ouverture quotidienne de session du PC.

**_Remarque 1 : il est important que le Compositeur Digital démarre 1 fois par jour._**

**_Remarque 2 : le chemin vers l'exécutable principal peut changer lors d'une mise à jour._**

- Processus à surveiller : Compositeur Digital KetB.exe
- Démarrage : utiliser le lien généré lors de l'installation (raccourci dynamique) situé à l'adresse ci-dessous :

"%appdata%\Microsoft\Windows\Start Menu\Programs\EXCENSE\Compositeur Digital\Compositeur Digital KetB.appref-ms"

Utiliser au besoin .bat si le watchdog ne peut démarrer un fichier de type .appref-ms. (nécessaire pour restartoncrash).

## Exploitation
### Arrêt
ALT+F4 ou à travers le gestionnaire des tâches.

### Mise à jour manuelle
Procédure identique à l'installation.

### Version
Sur la page d'accueil en bas à droite.

### Répertoire d'installation
Modèle du chemin vers le répertoire, celui-ci peut varier d'une installation à l'autre et lors d'une mise à jour :

C:\Users\\[USER]\AppData\Local\Apps\2.0\\[F1]\\[F2]\comp..tion_[ID]

### Traces
%appdata%\Compositeur Digital\log app




