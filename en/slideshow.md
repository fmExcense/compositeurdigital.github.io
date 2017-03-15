# Slideshow

Use this feature to concatenate a set of images, PPT presentations or PDF documents.

## Interactions in the Compositeur Digital

The slideshow offers the following interactions :

- Navigation to the previous or followin slide using the `<` and `>` arrows
- "Go-to" a specific slide using the `Slides` action in the document menu
- Opening of a linked content
- Annotations
- Printing

### Content Management

- Folder extension : `slideshow`
- Supported extensions in the folder : `jpg`, `png`, `ppt`, `pptx`, `pdf`

### Powerpoint presentations

- Supported extensions : `ppt`, `pptx`, `pdf`

>*Note 1:* If you are using a specific version of Powerpoint that is not supported by the Compositeur Digital, you can still export your presentation in PDF.

>*Note 2:* The Compositeur Digital does not support transition effects or animations contained in the presentation. 

>*Note 3:* You can open any other content from a specific slide using the "link" feature. Please refer to the [Interactivity]  (interactive) section for further details.

### Folder organization 

Example of folder organization for similar document types

![explorer slideshow img](img/explorer_slideshow_img.jpg)

You can also create a single slideshow with a combination of Powerpoint, PDF and image files. Place all files in a folder using the `slideshow` extension.

Example of folder organization :

![explorer slideshow docs](img/explorer_slideshow_docs.jpg)

In this case, the resulting slideshow will display slides in the following sequence : the first image file, the slides from the 2 PDF files and then the last image file.

### <a name="interactive"></a> Interaction between documents

You can create a "hot spot" on a document to open another document when touched . This interaction is created using Powerpoint.

1. If the source document is a PPT file open if using Microsoft PowerPoint. If it's an Image, copy paste is in a blank Powerpoint presentation
2. Create a transparent shape on top of the selected hot spot. The shape should cover entire hot spot area.
	Warning : If the area is the text box. Select the text BOX. Do not not select the TEXT 
3. After selecting you shape, right-click and go to Hypertext link  
4. In the pop-up window define the location of the target document.
	Warning : The target document must be somewhere the folder used for your environment. You can use the hideen folders feature [dossiers cachés](manage_contents#contentFolder) (`content` extension) if you do not with to display the target folder in your environment.
	
6. Save your Powerpoint presentation at the desired location in your environment folder.

![powerpoint slideshow liens](img/powerpoint_slideshow_liens.jpg)

[Back to supported content](content_types.md)
