# Configuration avancée
## Métadonnées
Pour modifier le comportement ou les fonctionnalités d'un document, il est possible d'utiliser des paramètres dans un fichier `_meta.txt`.

Dans le cas d'un dossier il suffit de le placer à l'intérieur de celui-ci.

Dans le cas d'un fichier il faut alors lui donner le nom du fichier suivi du suffixe `_meta` avec l'extension `txt`, et le placer au même endroit que le fichier.

Par exemple, pour un fichier `1 - image.jpg`, le fichier meta correspondant doit s'appeler `1 - image_meta.txt`.

Dans ce fichier chaque ligne (nommée `meta`) permet de préciser un paramètre. 

Une meta s'écrit sous la forme `nomDeLaMeta = valeur`

Une meta binaire (à valeur vrai ou faux) s'écrit donc : `nomDeLaMeta = true`. Par défaut, elle a pour valeur `false`. Les valeurs `1` (pour true) et `0` (pour false) peuvent également être utilisées.

Pour appliquer un comportement à plusieurs documents en même temps il est possible de spécifier dans un fichier meta à la racine de l'ensemble des documents concernés et d'utiliser le suffixe `*.` pour chaque ligne.

Exemple : `*.table.hideCommands = true`


### Configuration d'un document :
*Boutons :*
 - `table.hideCommands = true` permet de masquer les boutons de contrôle d'un document. Sur un slideshow les boutons précédents, suivant et diapositives disparaissent. Sur une vidéo, les boutons lecture/pause/muet et la barre de progression disparaissent.
 - `disablePrint = true` masque le bouton d'impression
 - `disableAnnotation = true` masque le bouton d'annotation
 - `enableMeasure = true` affiche le bouton de mesure parmi les annotations possibles
 - `disableDuplicate = true` masque le bouton de duplication
 - `disableSendBehind = true` masque le bouton d'envoi à l'arrière plan 

*Manipulation :*
 - `table.noRotate = true` empêche l'élément d'être tourné
 - `table.noScale = true` empêche l'élément d'être redimensionné
 - `table.noMove = true` empêche l'élément d'être déplacé (dans ce cas, il sera positionné au milieu de l'écran)

*Apparence :*
 - `Height = 400` fixe la hauteur du document
 - `Width = 400` fixe la largeur du document
 - `desiredHeight = 400` fixe la hauteur souhaitée du document
 - `desiredWidth = 400` fixe la largeur souhaitée du document
 - `minHeight = 400` fixe la hauteur minimale du document
 - `minWidth = 400` fixe la largeur minimale du document
 - `maxHeight = 400` fixe la hauteur maximale du document
 - `maxWidth = 400` fixe la largeur maximale du document
 - `table.hideChrome = true` supprime l'ombre du document et masque son menu et le bouton fermer
 - `table.alwaysBehind = true` force le document à rester à l'arrière-plan, derrière les autres documents
 - `name = toto` permet de modifier le nom du document qui sera affiché
 - `hideLinkLabel = true` masque le nom partout où il doit être affiché
 - `orientation = 90` fait pivoter le document de l'angle spécifié. `-90`  pour pivoter à gauche, `90` pour pivoter à droite ou `180` pour retourner
 
### Paramètres de déclinaison
*Apparence*
 - `themeColor = 9c211f` force la couleur du thème, qui est par défaut calculée en moyennant la couleur de l'image d'arrière-plan

*Boutons de la barre de menu :*
 - `disableGoBack = true` masque le bouton de retour
 - `disableReset = true` masque le bouton de réinitialisation
 - `disableQuit = true` masque le bouton quitter
 - `disableHelp = true` masque le bouton d'aide
 - `disableContactUs = true` masque le bouton de contact

*Favoris :*
 - `favorites.disableFastShare = true` masque le bouton de partage rapide sur les documents
 - `favorites.disableFavorites = true` désactive le mécanisme de favoris/panier : masque le bouton d'ouverture des favoris dans la barre de menu et les boutons d'ajout/suppression des documents

*Outils Papiers :*
 - `paper.disableBlankSheet = true` masque le bouton de création d'une nouvelle feuille blanche
 - `paper.disablePostIt = true` masque le bouton de création d'un nouveau post-it


## <a name="configFiles"></a>Fichiers de configuration
Chaque paramètre s'écrit sous la forme `<param name="nomDuParamètre" value="valeurDuParamètre, deuxièmeValeurFacultative, troisième, etc" />`

*App.xml*

 - `HomePage` par défaut : Table 
 - `DemoItems` adresse vers les fichiers de démonstration à télécharger (par défaut http://www.compositeurdigital.com/demo/contents/config.json ) Peut être une adresse vers une resource embarquée (ex : /Compositeur Digital;component/DemoContent.zip)
 - `ExplicitPlugins` liste des dll de plugins à utiliser
 - `ResetOnItemLoading` réinitialise au chargement d'une déclinaison
 - `ExtraButtons` boutons à afficher dans le sous menu "plus". Par défaut : GoBack, Reset, Quit, Help, ContactUs
 - `KioskMode` passe en mode kiosque si est à true : désactive tous les extrabuttons (sauf GoBack si il y a plusieurs déclinaisons)
 - `AutoResetInterval` en mode kiosque seulement : intervalle en minutes entre la dernière action utilisateur détectée et la réinitialisation automatique
 - `FavoritesDestinationPath` chemin du dossier où enregistrer les favoris
 - `DisablePrint` désactive l'impression si est à true
 - `DisableAnnotation` désactive l'annotation si est à true
 - `UseLegacyTouchEvents` force l'utilisation des évènements tactiles Windows 7 si est à "true"
 - `DisplayOnSecondaryScreen` quand vaut "true" : si deux écrans sont détéctés, ouvre le compositeur digital sur l'écran secondaire
 - `DisableBlankSheet` si est à "true", masque le bouton de partage rapide sur les documents
 - `DisablePostIt` si est à "true", désactive le mécanisme de favoris/panier : masque le bouton d'ouverture des favoris dans la barre de menu et les boutons d'ajout/suppression des documents
 - `DisableFastShare` si est à "true", masque le bouton de création d'une nouvelle feuille blanche
 - `DisableFavorites` si est à "true", masque le bouton de création d'un nouveau post-it

*Favorites.xml*
 - `FolderName` par défaut : panier
 - `ContactInfos` contient la liste des champs à afficher lors de la sauvegarde des favoris. Par défaut : <br />
    `<contactInfos><br />
      <contactInfo key="true" label="nom" /><br />
      <contactInfo label="email" /><br />
    </contactInfos><br />`
 - `FavoritesDestinationPath` chemin du dossier où enregistrer les favoris
 - `DisableFastShare` désactive le bouton de partage rapide si est à true
 - `DisableFavorites` désactive le mécanisme de favoris/panier si est à true : masque le bouton d'ouverture des favoris dans la barre de menu et les boutons d'ajout/suppression des documents

*Page.xml*
 - `EnableMeasure` affiche le bouton de mesure parmi les annotations possibles si est à true
 - `DisableDuplicate` masque le bouton de duplication si est à true
 - `DisableSendBehind` masque le bouton d'envoi à l'arrière-plan si est à true

*Common.xml*
 - `AdditionalRootItemsFolderPaths` liste de répertoires supplémentaires dans lesquels le Compositeur Digital chargera des déclinaisons
 - `CacheDirectory` permet de spécifier un répertoire particulier où enregistrer les fichiers de cache 
 

 ## <a name="valueKeys"></a>Données partagées entre les documents
 Certains types de documents permettent dans leur configuration de partager une donnée avec d'autres documents (c'est à dire de récupérer la valeur précédemment renseignée et de la modifier).
 Un mot clé commun renseigné pour un champ "valueKey" permettra de créer ce lien. Les clés par défaut sont modifiables dans l'onglet Profil du menu.
 Les clés déjà existantes sont :
  - `firstName`
  - `lastName`
  - `email`
  - `phoneNumber`
  - `organization`
  - `finance.budget`

[Revenir au menu](home.md)