# Content management

Compositeur Digital reads documents stored on your computer. Those documents can to be organized in folders to facilite the presentation

## Required skills and resources

The preparation of an environnement is done using the Windows built-in file explorer.

You should be confortable with : 

- Organizing folders 
- Renaming files and folder
- That's all :)

### File extensions

The Compositeur Digital uses the file extension to setup the various elements of an environment.  The * file extension*, is usually consisting of 3 or 4 characters after the dot in the file name indicating the type of document:

- Images : photo1.jpg, photo2.png
- Presentation : pres1.pptx, pres2.pdf
- Text file : table of content.txt

By default the Windows File explorer application hides file extensions. We strongly recommend to change this setting:

![show extensions](img/show_extensions.jpg)

## Environment

The Compositeur Digital can be use for multiple purposes

Real estate

![univers 1](img/univers1.jpg)

Banking services

![univers 2](img/univers2.jpg)

Technically  an environment is a specific folder on your computer. By default the Compositeur Digital will look for folders located in   `Documents\Compositeur Digital`

![Environement view using the built-in Window file explorer](img/explorer_univers.jpg)

To create your own environment , you can start by dublicating an exisiting one in the default location :  `Documents\Compositeur Digital`.

## Background

You can customize your environment by changing the background image. To do so, simply add an image file named `_background` with the environment folder as described below:

![universe background](img/explorer_background.jpg)

## Folders

In an environment, you can organize your documents in folders and sub-folders.

The first level of folder-view is displayed in the Compositeur Digital in the dock located at the bottom of the screen : 

![explorer root folders](img/explorer_root_folders.jpg)

![root folders](img/root_folders.jpg)

>### <a name="contentFolder"></a> Hidden folders
>
>Folders using a '.content' extension will not be seen in Compositeur Digital. 
>See [interactive slideshow](slideshow#interactive) to see the common use of this feature.

## Documents

Simply drag and drop your documents in the folders and sub-folders to populate your environment.

Check [Supported content](content_types.md) for an exhaustive list of supported file types.

## Display order

Compositeur Digital will display all items in folders using an alphabetical order. You can however force a specific order for documents and folders by prefixing the names with a number. The Compositeur Digital will not display the numbers but will arrange the items accordingly.

>If you need to display a file with a name starting with a number (e.g. `3D render`), see the [Advanced configuration](config#configuration_dun_document) section.

## Thumbnails 

Compositeur Digital will generate thumbnails for all documents. You can also customize the thumbnail for any document or folder for cases.

### Folder thumbnails

With no specified thumbnail for a folder, Compositeur Digital will use the thumbnail of the first item in ths folder:

![explorer no preview folder](img/explorer_nopreview_folder.jpg)

![no preview folder](img/nopreview_folder.jpg) 

Add an image file named `_preview` (png or jpg) directly in the folder:

![explorer no preview folder](img/explorer_preview_folder.jpg)

![no preview folder](img/preview_folder.jpg) 

### Document thumbnail

To customize the thumbnail for a document, place an image file with the same name suffixed with `_preview` in the same folder:

![explorer preview file](img/explorer_preview_file.jpg)

## Standby video

When in Kiosk mode Compositeur Digital can play a fullscreen video after a period of inactivity. The video will then loop until the screen is touched.

Place a supported video file named `_standby` in the universe folder:

![standby](img/explorer_standby.jpg) 

All [supported video types](video.md) are suitable for use as a standby video.
