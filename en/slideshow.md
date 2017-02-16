# Slideshow

Use this type of content to display a slideshow of images, or a presentation in PDF or Powerpoint.

## Usage

With a slideshow you can :

- Navigate to the previous and next slide with the `<` and `>` arrows
- Navigate to a specific slide with the `Slides` action in the document menu
- Open attached content
- Annotate
- Print

## Content management

A slideshow is created from a single PDF or Powerpoint file, or from a set of images or a combination of those documents.

### Powerpoint & PDF documents

- Supported extensions : `ppt`, `pptx`, `pdf`

>*Note 1:* som complex documents may no display properly. You may change the document format (e.g. save a Powerpoint presentation as a PDF) to try and circumvent the problem.

>*Note 2:* Compositeur Digital will not play transittion effects and animations: each slide is a fixed image. You can however add touch "buttons" to open other documents (see [Interactivity](interactive)).

### Image set folder

- Folder extension : `slideshow`, `ppt`, `pptx`, `pdf`
- Supported extensions in the folder : `jpg`, `png`

Sample slideshow file hierarchy:

![explorer slideshow img](img/explorer_slideshow_img.jpg)

### Document set folder

You can create a single slideshw with a combination of Powerpoint, PDF and image files. Place all files the same folder with the extension `slideshow`.

Sample slideshow file hierarchy:

![explorer slideshow docs](img/explorer_slideshow_docs.jpg)

In this case, the resulting slideshow will display slides in this order: the fisrt image, the slides from the 2 PDF files and then the last image.

### <a name="interactive"></a> Interactivity

You can create a touch area on a slide of a Powerpoint presentation to opend content in Compositeur Digital.

1. Ouvrez votre présentation avec Microsoft PowerPoint.
2. Sélectionnez l'image ou l'objet sur lequel vous souhaitez créer un lien. Il est conseillé de choisir un élément qui invite l'utilisateur à le toucher pour déclencher l'ouverture du contenu.
	Attention : l'opération ne fonctionnera pas si vous sélectionnez le texte contenu dans une forme, c'est la forme elle-même qu'il faut sélectionner.
3. Allez dans l'onglet `INSERTION` de PowerPoint.
4. Cliquez sur le bouton `Lien hypertexte` du menu correspondant.
5. Dans la fenêtre qui apparaît, parcourez vos fichiers pour choisir le contenu que le lien devra ouvrir.
	Attention : vous devez obligatoirement choisir un contenu présent quelque part dans votre univers.
	Vous pouvez utiliser des [dossiers cachés](manage_contents#contentFolder) (extension de dossier `content`) s'ils ne doivent apparaître que dans le diaporama interactif.
	
6. Cliquez sur `Ouvrir`, puis sauvegardez votre présentation PowerPoint.

![powerpoint slideshow liens](img/powerpoint_slideshow_liens.jpg)

[Back to supported content](content_types.md)
