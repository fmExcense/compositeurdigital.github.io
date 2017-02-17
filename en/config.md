# Advanced configuration
## Metadata
To modify a document's behavior or functionalities, it is possible to write some parameters in a file `_meta.txt`.

In the case of a folder, it must be inside the folder.

In the case of a file, it must be named with the file name followed by the suffix `_meta` with the `txt` extension, and positioned at the same place than the file.

For example, for a file `1 - image.jpg`, the corresponding meta file needs to be named `1 - image_meta.txt`.

In this file, every line (named `meta`) allow to describe a parameter and is written in the form : `metaName = value`

A binary meta (true or false) is then written `metaName = true`. It's default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a comportment to a set of documents, use the `*.` suffix on every line and put the file at the root directory of all the concerned files.

Example : `*.table.hideCommands = true`


### Document configuration :
*Buttons :*
 - `table.hideCommands = true` hides the control buttons of a document. On a slideshow, the buttons Next, Previous and Slides disappear. On a video, the buttons play/pause, mute and the progress bar disappear.
 - `disablePrint = true` hides the print button
 - `disableAnnotation = true` hides the annotation button
 - `disableDuplicate = true` hides the duplicate button
 - `disableSendBehind = true` hides the "send to background" button

*Manipulation :*
 - `table.noRotate = true` inhibits the document rotation
 - `table.noScale = true` inhibits the document resizing
 - `table.noMove = true` inhibits the document moves (it will be opened in the middle of the screen)

*Appearence :*
 - `desiredHeight = 400` sets the default height of the document
 - `desiredWidth = 400` sets the default width of the document
 - `minHeight = 400` sets the minimum height
 - `minWidth = 400` sets the minimum width
 - `maxHeight = 400` sets the maximum height
 - `maxWidth = 400` sets the maximum width
 - `table.hideChrome = true` hides the shadow, the menu and the close button of a document
 - `table.alwaysBehind = true` force the document to stay on the background, behind the other documents
 - `name = toto` change the displayed name of a document
 - `hideLinkLabel = true` hide the name of a document
 - `orientation = 90` rotate the document by the specified angle : `-90` to turn left, `90` to turn right or `180`  pour retourner
 
### Universe parameters
*Appearence*
 - `themeColor = 9c211f` sets the theme color, which is by default computed from the average color of the background

*Buttons :*
 - `disableGoBack = true` hides the back button
 - `disableReset = true` hides the reset button
 - `disableQuit = true` hides the quit button
 - `disableHelp = true` hides the help button
 - `disableContactUs = true` hides the contact button

*Favorites :*
 - `favorites.disableFastShare = true` hides the fast share button on all documents
 - `favorites.disableFavorites = true` disable the document basket/favorites mecanism.

*Paper tools :*
 - `paper.disableBlankSheet = true` hides the blanksheet creation button
 - `paper.disablePostIt = true` hides the note creation button


## Configuration files
Every parameter is written in the form `<param name="parameterName" value="parameterValue, secondOptionalValue, third, etc" />`

*App.xml*

 - `HomePage` by default : Table 
 - `DemoItems` adress of the demo content (by default http://www.compositeurdigital.com/demo/contents/config.json ) Can be the adress of an embedded resource (ex : /Compositeur Digital;component/DemoContent.zip)
 - `ExplicitPlugins` list of dll plugins to use
 - `ResetOnItemLoading` reset the environment on universe loading
 - `KioskMode` set the kiosk mode. Hides all menus and the quit button (except if there is several universes)
 - `AutoResetInterval` in kiosk mode only : delay in minutes between the last user action detected an the automatic reset
 - `FavoritesDestinationPath` folder path where favorites will be saved
 - `DisablePrint` disable print
 - `DisableAnnotation` disable annotations
 - `UseLegacyTouchEvents` if true, force the use of Windows 7 touch events
 - `DisplayOnSecondaryScreen` if true and two screen are detected, use the secondary screen
 - `DisableFastShare` if true hides the fast share button on all documents
 - `DisableFavorites` disable the document basket/favorites mecanism.
 - `DisableBlankSheet` hides the blanksheet creation button
 - `DisablePostIt` hides the note creation button

*Favorites.xml*
 - `FolderName` displayed name. By default : basket
 - `ContactInfos` contains the list of field to display during saving. By default : <br />
    `<contactInfos>
      <contactInfo key="true" label="name" />
      <contactInfo label="email" />
    </contactInfos>`
 - `FavoritesDestinationPath` folder path where favorites document are saved
 - `DisableFastShare` hides the fast share button on all documents
 - `DisableFavorites` disable the document basket/favorites mecanism.

*Page.xml*
 - `DisableDuplicate` hides the duplicate buttons
 - `DisableSendBehind` hides the "send to background" buttons

*Common.xml*
 - `AdditionalRootItemsFolderPaths` list of addional directories where to search universes
 - `CacheDirectory` sets a folder permet de spécifier un répertoire particulier où enregistrer les fichiers de cache 
 

 ## <a name="valueKeys"></a>Shared data between documents
 Some document types allow to share data with other documents (ie get a value previously saved and modify it)
 A common keyword is used to create this link. The values of the default keys can be modified in the Profile panel of the menu.
 The existing keys are :
  - `firstName`
  - `lastName`
  - `email`
  - `phoneNumber`
  - `organization`
  - `finance.budget`

[Back to the menu](home.md)
