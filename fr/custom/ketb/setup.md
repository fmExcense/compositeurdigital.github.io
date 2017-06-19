
# Kaufman & Broad : procédure de déploiement du Compositeur Digital

*Cette procédure est valable pour la phase de production à partir de S2 2017*

## Prérequis matériel et réseau
- Ordinateur / tablette tactile, Intel Core i5 ou supérieur, SSD 128 Go minimum.
- Windows 10 (Anniversary update ou supérieur).
- Connexion internet, lors de l'installation, mais aussi lors de l'utilisation pour la mise à jour des contenus.

## Prérequis mode "kiosque"
- verouillage de l'environnement shell Windows (exemple de logiciel : Frontface Lockdown).
- logiciel de type watchdog pour surveiller et relancer le Compositeur Digital en cas d'arrêt non prévu (exemple de logiciel : restartoncrash).
- Arrêt/démarrage automatique matin et soir (*heures à déterminer avec K&B*).


## Installation
### 1. Configurer OneDrive
Compte `ketb@compositeurdigital.com`. Utiliser la configuration par défaut.

**_Remarque : la synchronisation initiale provoque le téléchargement de plusieurs dizaines de Go de données : elle ne doit pas être faite sur site K&B. Seules les mises à jour différentielles sont faites sur site K&B._**

### 2. Installer Compositeur Digital
En ligne à partir de l'adresse [http://www.compositeurdigital.com/deploy/ketb](http://www.compositeurdigital.com/deploy/ketb).

### 3. Configurer démarrage/watchdog
Démarrage automatique du Compositeur Digital et/ou du watchdog à l'ouverture de session du PC.

**_Remarque il est important que le Compositeur Digital redémarre 1 fois par jour._**

#### Configuration Watchdog/démarrage

**_Remarque : le chemin vers l'exécutable principal peut changer lors d'une mise à jour._**

- Processus à surveiller : Compositeur Digital KetB.exe
- Démarrage : utiliser le lien généré lors de l'installation (raccourci dynamique) situé à l'adresse ci-dessous :

"%appdata%\Microsoft\Windows\Start Menu\Programs\EXCENSE\Compositeur Digital\Compositeur Digital KetB.appref-ms"

Utiliser au besoin .bat si le watchdog ne peut démarrer un fichier de type .appref-ms. (nécessaire pour restartoncrash).

## Exploitation
### Arrêt du Compositeur Digital
ALT+F4 ou à travers le gestionnaire des tâches.

### Mise à jour manuelle Compositeur Digital
Procédure identique à l'installation.

### Version du Compositeur Digital
Sur la page d'accueil en bas à droite.

### Répertoire d'installation du Compositeur Digital
C:\Users\[USER]\AppData\Local\Apps\2.0\[F1]\[F2]\comp..tion_[ID]

### Traces
%appdata%\Compositeur Digital\log app




