# Quiz

Use this type of content to guide users through a series of questions and store the resulting information.

## Use in Compositeur Digital

You can navigate to the previous and next page using the `<` and `>` arrows on the sides.
Depending on the type of page you can:
 - select an deselect an answer
 - move a slider
 - type in some text
 - open a linked document

## Content management

- Folder extension: `quiz`

The quiz folder contains:

- Optional `_background` image file to customize the quiz appearance
- Optional documents linked in the quiz
- A `_meta` containing all images used in the different pages
- The configuration file: `_questions.xml`

The configuration file describes the quiz itself, page by page. It is formatted in XML: edit it with Notepad or another text editor.


### Configuration file structure

The Quiz file consists of two parts:  `sections` and `pages`.
Organisation générale du fichier :
```xml
<quizz>
    <sections>
        list of sections
    </sections>
    <pages>
        list of pages
    </pages>
</quizz>
```

Pages represent each a question. Sections let you group pagesLes sections permettent de regrouper des pages sous un même nom. 

### Sections
Set the section display name in a `section` tag and use the attribute `id` to set the reference name for the section.

```xml
<section id="intro">1. INTRODUCTION</section>
```

### Pages
You can add different page types to a quiz. All pages have the following in common:
 - a `sectionId` attribute: assign a page to a section. The section name will appear on top of the quiz page.
 - an `id` attribute: optional identifier for referencing the page.
 - a `nextPageId` attribute: optional reference to the page that shoud be displayed next. If not set, the next page in the file will nbe used. 

### 
The first page in the list will always be the first displayed.
The last page will by default be the last displayed page.
To indicate that a page should end the quiz, set the `nextPageId` attribute to the specific value `@end`.

### Page types
#### `questionPage`
This page type lets you create a question with a list of possible answers that must be selected befor being able to go to the next page.

Here are the attributes for `questionPage`:
 - `label`: text of the question. Takes precedence over `visual`.
 - `visual`: name of the question image file (without extension). The file must exist in the `_meta` folder.
 - `allowMultiple`: set to `true` to allow the selection of multiple answer.

The content of the `questionPage` is the list of answer, which can be of to types:
 - text answers, with the tag `answer`:
 ```xml
 <answer>my answer</answer>
 ```
 - visual answers, with the tag `imageAnswer`. Set attribute `visual` to the name of the image (without extension) in the `_meta` folder:
   ```xml
   <imageAnswer visual="image 2"/>
   ```
   optionally you can set a caption:
   ```xml
   <imageAnswer visual="image 2">my caption</imageAnswer>
   ```
It is not possible to mix text answers with visual answers.

Set the `nextPageId` attribute on an answer to jump to a specific page if the user selects that answer and create branches to your quiz:

```xml
<questionPage id="Q1" sectionId="section 2" label="To which aquestion do you wish to answer ?" >
	<answer>The next question</answer>
	<answer nextPageId="Q1">This one again</answer>
	<answer nextPageId="Q3">Skip one please</answer>
</questionPage>

<questionPage id="Q2" sectionId="section 3" label="The next question">
	...
</questionPage>	
	
<questionPage id="Q3" sectionId="section 3" label="The last question">
	...
</questionPage>
```
![questionPage imageAnswer](img/questionpage_imageanswer.jpg)

#### `page`
A simple page to display either text or an image:
 - `label`: text to display
 - `visual`: name of the image file to display (no extension, file present in `_meta` folder

```xml
<page sectionId="intro" label="Ceci est un test"/>
```
![page label](img/page_label.jpg)
![page image](img/page_image.jpg)


#### `infoPage`
Display a simple form in which the user can type in some information. Add `info` tags with the `label` attribute.

```xml
<infoPage sectionId="intro" label="Please fill out your identity">
	<info label="Name"/>
	<info label="Surname"/>
</infoPage>
```
![infoPage](img/infopage.jpg)

To share this information with other documents and the profile info, use the `valueKey` attribute on an `info` tag (see [shared data](config#valueKeys)).


#### Le Type `numericSliderPage`
Ce type de page permet d'afficher un curseur à valeur numérique. Vous pouvez le paramétrer à l'aide des attributs suivants :
 - `label` : le titre ou la question à afficher.
 - `visual` : le nom de l'image à afficher en tant que question (sans son extension). Celle-ci doit être placée dans le dossier `_meta` du quiz
 - `min` : la valeur minimale sélectionnable
 - `max` : la valeur maximale sélectionnable
 - `minLabel` : (optionnel) : valeur affichée pour la valeur minimale
 - `maxLabel` : (optionnel) : valeur affichée pour la valeur maximale
 - `default` : (optionnel) la valeur sélectionnée par défaut au chargement de la page
 - `stepSize` : le "pas" de sélection (différence minimale entre deux valeurs du curseur)
 - `format` : permet de changer la manière d'afficher la valeur.

 différentes valeurs possible pour format :
 - `N0` : un entier
 - `C0` : une valeur monétaire entière (sera suivi du symbole € sur un ordinateur français, précédé par un £ sur un ordinateur anglais, etc.)

exemple :
```xml
<numericSliderPage id="apport" sectionId="section 3" label="Votre budget " min="0" max="1000000" stepSize="5000" format="C0" valueKey="finance.budget" />
```
![numericSliderPage](img/quiz_numericsliderpage.jpg)

Afin de partager la valeur du curseur avec d'autres documents, vous pouvez ajouter un attribut `valueKey` à cette page (voir [données partagées](config#valueKeys)).

  #### Le Type `labelSliderPage`
Ce type de page permet d'afficher un curseur avec du texte. Vous pouvez le paramétrer à l'aide des attributs suivants :
- `label` : le titre ou la question à afficher.

Possibilité de gérer les étapes disponibles en rajoutant des `answer`. La première va définir le minimum et la dernière le maximum.
Les réponses proposées doivent donc être classés en ordre croissant (lorsque c'est possible).

exemple :
```xml
<labelSliderPage sectionId="section1" label="Faites vous souvent des achats en ligne ?">
	<answer>Jamais</answer>
	<answer>Parfois</answer>
	<answer>Souvent</answer>
	<answer>Toujours</answer>
</labelSliderPage>
```
![labelSliderPage](img/quiz_labelsliderpage.jpg)


#### Le Type `imageSliderPage`
Ce type de page permet d'afficher un curseur à valeur relative entre deux images : la valeur n'est pas affichée; l'utilisateur choisi juste si il est plus en accord avec l'image de droite ou l'image de gauche en déplaçant le curseur.
Vous pouvez le paramétrer à l'aide des attributs suivants :
 - `label` : le titre ou la question à afficher.
 - `visual` : le nom de l'image à afficher en tant que question (sans son extension). Celle-ci doit être placée dans le dossier `_meta` du quiz
 - `leftVisual` : l'image qui sera affichée à gauche du curseur
 - `rightVisual` : l'image qui sera affichée à droite du curseur
 - `stepQuantity` : le nombre de valeur sélectionnables sur le curseur (une valeur de 10 est conseillée pour meilleur rendu visuel)

exemple :
```xml
<imageSliderPage sectionId="partie 1" label="Vous êtes plutôt :" leftVisual="image1" rightVisual="image2" stepQuantity="10"/>
```
![imageSliderPage label](img/imagesliderlabel.jpg)
![imageSliderPage image](img/imagesliderimage.jpg)


#### Le Type `documentPage`
Cette page permet de lancer l'ouverture d'un document dans le Compositeur Digital.
Vous pouvez le paramétrer avec les attributs :
- `label` : le titre ou la question à afficher.
- `document` : le nom du document à ouvrir. Il faut que le document soit dans le dossier du quiz.

exemple :
```xml
<documentPage label="Vos documents :" document="Documents A"/>
```
![documentPage](img/documentpage.jpg)


#### Le Type `orderPage`
Cette page permet de définir un nombre de réponse minimum dans un questionnaire et de récupérer celles qui sont cochées.
Vous pouvez le paramétrer avec les attributs :
- `label` : le titre ou la question à afficher.
- `answerNumber` : le nombre de réponse minimum à cocher.
- `imageAnswer` : ajoute une image comme réponse.
- `visual` : ajoute une visuel comme réponse.
- `visualChecked` : image remplaçant le visuel lorsqu'il est sélectionné.

exemple :
```xml
<orderPage sectionId="section 1" label="Votre projet ordonnancé" answerNumber="3">
	<answer >Travaux</answer>
    <answer >Première acquisition</answer>
	<answer nextPageId="tousLesBiens">Achat ou revente</answer>
    <answer nextPageId="maisonAppart">Travaux</answer>
    <answer nextPageId="tousLesBiens">Acquisition retraite</answer>
</orderPage>
```
![orderPage empty](img/orderpage_empty.jpg)

ou


```xml
<orderPage sectionId="section 1" label="Votre projet ordonnancé" answerNumber="3">
	<visualAnswer visual="maison" visualChecked="test1">Maison</visualAnswer>
    <visualAnswer visual="appartement" visualChecked="test2">Appartement</visualAnswer>
  </orderPage>
```
![orderPageImage empty](img/orderpageimage_empty.jpg)

### Résultats
Vous pouvez consulter les résultats du quiz dans le dossier `Mes Documents \ Compositeur Digital Quiz`.	
Les fichiers de résultats sont nommés selon leur origine (nom de la déclinaison, arborescence éventuelle, puis nom du quiz). 
Lorsque vous modifiez le fichier `_questions.xml` et si les questions/titres de page ont changé, les enregistrements de résultats se feront dans un nouveau fichier (ajout d'un numéro au nom du fichier) afin de ne pas écraser les anciens résultats.
Une nouvelle ligne de résultat est enregistrée à chaque fois que l'on atteint une page de fin du quiz.


[Revenir au différents Types de contenus](content_types.md)
