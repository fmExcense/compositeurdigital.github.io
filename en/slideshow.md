# Slideshow

Use this feature to concatenate a set of images, PPT presentations or PDF documents.

## Interactions in the Compositeur Digital

The slideshow has the following interactions available :

- Navigation to the previous or followin slide using the `<` and `>` arrows
- "Go-to" a specific slide using the `Slides` action in the document menu
- Opening of an attached content
- Annotations
- Printing

## Content management

A slideshow can be created from a set of images, PPT presentations or PDF documents regardless of the numbers of pages.

### Powerpoint & PDF documents

- Supported extensions : `ppt`, `pptx`, `pdf`

>*Note 1:* If you are using a specific version of Powerpoint that is not supported by the Compositeur Digital, you can still export your presentation in PDF.

>*Note 2:* The Compositeur Digital does not support transition effects or animations contained in the presentation. 

>*Note 3:* You can open any other content from a specific slide using the "link" feature. Please refer to the [Interactivity]section (interactive)) for further details.

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
