# Advanced configuration
## Metadata
To modify a document's behavior or functionalities, it is possible to position specific parameters in a file named `_meta.txt`.

To modify the behavior of a folder, the file must be place inside the folder.

To modify the behavior of a file, it must be named after the file name followed by the suffix `_meta` and the `txt` extension, and positioned at the same location as the file.

For example, for a file `1 - image.jpg`, the corresponding meta file should to be named as follows : `1 - image_meta.txt`.

In the meta file, each line (named `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary meta (true or false) is then written `metaName = true`. It's default value is `false`. The values `1` (true) and `0` (false) can also be used.

To specify a behavior for a set of documents, use the `*.` prefix on the line and place the file in the documents' folder

Example : `*.table.hideCommands = true`


### Document configuration :
*Buttons :*
 - `table.hideCommands = true` hides the control buttons of a document. On a slideshow, the buttons Next, Previous and Slides will disappear. On a video, the buttons play/pause, mute and the progress bar will disappear.
 - `disablePrint = true` hides the print button
 - `disableAnnotation = true` hides the annotation button
 - `disableDuplicate = true` hides the duplicate button
 - `disableSendBehind = true` hides the "send to background" button

*Manipulation :*
 - `table.noRotate = true` inhibits rotation for the document
 - `table.noScale = true` inhibits resizing for the document 
 - `table.noMove = true` inhibits all movements for the document (it will be opened in the middle of the screen)

*Appearence :*
 - `desiredHeight = 400` sets the default height of the document
 - `desiredWidth = 400` sets the default width of the document
 - `minHeight = 400` sets the minimum height
 - `minWidth = 400` sets the minimum width
 - `maxHeight = 400` sets the maximum height
 - `maxWidth = 400` sets the maximum width
 - `table.hideChrome = true` hides the shadow, the menu and the close button of a document
 - `table.alwaysBehind = true` forces the document to stay in background, behind the other documents
 - `name = toto` change the displayed name of a document to "toto" (example)
 - `hideLinkLabel = true` hides the name of the document
 - `orientation = 90` rotates the document using a specified value : `-90` to turn left, `90` to turn right or `180` to flip the document
 
### Environment parameters
*Appearence*
 - `themeColor = 9c211f` sets a specified value for the theme color. By default, the value is set the mean value of the color of the background

*Buttons :*
 - `disableGoBack = true` hides the back button
 - `disableReset = true` hides the reset button
 - `disableQuit = true` hides the quit button
 - `disableHelp = true` hides the help button
 - `disableContactUs = true` hides the contact button

*Favorites :*
 - `favorites.disableFastShare = true` hides the quick share button on all documents
 - `favorites.disableFavorites = true` disables the document basket/favorites feature.

*Paper tools :*
 - `paper.disableBlankSheet = true` hides the blanksheet creation button
 - `paper.disablePostIt = true` hides the note creation button


## Configuration files
Each parameter is written using the following structure : `<param name="parameterName" value="parameterValue, secondOptionalValue, third, etc" />`

*App.xml*

 - `HomePage` by default : Table 
 - `DemoItems` address of the demo content (set by default to http://www.compositeurdigital.com/demo/contents/config.json ). It can also be the address of an embedded resource (ex : /Compositeur Digital;component/DemoContent.zip)
 - `ExplicitPlugins` : list of dll plugins to use
 - `ResetOnItemLoading` resets the environment on loading
 - `KioskMode` activates the kiosk mode : Hides all menus and the quit button (except if there are several environments)
 - `AutoResetInterval` in kiosk mode only : Duration in minutes between the last user action an automatic environment reload
 - `FavoritesDestinationPath` folder path to where favorites will be saved
 - `DisablePrint` disables print feature
 - `DisableAnnotation` disables annotations
 - `UseLegacyTouchEvents` if set to true, forces the use of Windows 7 touch events
 - `DisplayOnSecondaryScreen` if set to true, uses the secondary screen when available
 - `DisableFastShare` if set to true,  hides the quick share button on all documents
 - `DisableFavorites` disables the basket/favorites feature.
 - `DisableBlankSheet` hides the blanksheet creation 
 - `DisablePostIt` hides the note creation button

*Favorites.xml*
 - `FolderName` displayed name for the basket feature. By default, set to "basket"
 - `ContactInfos` contains the list of fields to be stored. By default set to : <br />
    `<contactInfos>
      <contactInfo key="true" label="name" />
      <contactInfo label="email" />
    </contactInfos>`
 - `FavoritesDestinationPath` folder path to which favorites document will be saved
 - `DisableFastShare` hides the quick share button on all documents
 - `DisableFavorites` disable the document basket/favorites feature.

*Page.xml*
 - `DisableDuplicate` hides the duplicate button
 - `DisableSendBehind` hides the "send to background" button

*Common.xml*
 - `AdditionalRootItemsFolderPaths` list of addional directories in which the application will look for new environments 
 - `CacheDirectory` sets a specific folder to store cached files 
 
 ## <a name="valueKeys"></a> Data exchanged between documents
 
 Some document types allow to share data between an other  (e.g get a value previously saved and modify it)
 A common keyword is used to create this link. The values of the default keys can be modified in the Profile panel of the menu.
 Available keys are :
  - `firstName`
  - `lastName`
  - `email`
  - `phoneNumber`
  - `organization`
  - `finance.budget`

[Back to the menu](home.md)
