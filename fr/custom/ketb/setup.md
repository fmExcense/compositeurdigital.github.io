# Kaufman & Broad : procédure de déploiement du Compositeur Digital

*Cette procédure est valable pour la phase de production à partir de S2 2017*

## Prérequis matériel et réseau
- Ordinateur / tablette tactile sous Windows 10 (Anniversary update ou supérieur).
- Connexion internet, lors de l'installation, mais aussi lors de l'utilisation pour la mise à jour des contenus.

## Prérequis mode "kiosque"
- verouillage de l'environnement shell Windows (exemple de logiciel : Frontface Lockdown).
- logiciel de type watchdog pour surveiller et relancer le Compositeur Digital en cas d'arrêt non prévu (exemple de logiciel : restartoncrash).
- Arrêt/démarrage automatique matin et soir (*heures à déterminer avec K&B*).



## Installation
1. Configurer OneDrive avec le compte `ketb@compositeurdigital.com`. Utiliser la configuration par défaut.
2. Installation en ligne à partir de l'adresse [http://www.compositeurdigital.com/deploy/ketb](http://www.compositeurdigital.com/deploy/ketb).
3. Configurer le démarrage automatique du Compositeur Digital et/ou du watchdog au démarrage du PC.
4. Après la synchronisation initiale des contenus OneDrive, redémarrer le PC et vérifier le bon fonctionnement du Compositeur Digital.

Remarques :
- la synchronisation initiale comprend plusieurs dizaines de Go de données : elle ne doit pas être faite sur site K&B. Seules les mises à jour différentielles sont faites sur site K&B.
- il est important que le Compositeur Digital redémarre 1 fois par jour.
- configuration du watchdog et du démarrage : le chemin vers l'exécutable principal peut changer lors d'une mise à jour. Utiliser le lien généré lors de l'installation (raccourci dynamique) ou un script recherchant la dernière version de l'exécutable.

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




