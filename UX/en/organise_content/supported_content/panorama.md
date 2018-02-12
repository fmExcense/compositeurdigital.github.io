# Documentation

## Panorama : 360° view

This content type allows you to display a 360° view of a scene (e.g. landscapes, interior views...) using specific images.

### Action within Compositeur Digital UX

- [X] Enable / Disable navigation mode.
- [X] In navigation mode, sliding your finder on the item rotates the camera inside the scene.
- [X] Make a copy of your panorama using the `Duplicate` action.
- [X] Make a capture (i.e. create an image of the current view) using the `Capture` action.
- [X] Add the panorama to your favorites, using the `Add to favorites` action.
- [X] Remove the panorama from your favorites, using the `Remove from favorites` action.

### Content extension

To use a panorama, put the images to render in a folder, and add the extension `.panorama` at the end of the name of your folder.
Inside your panorama, only use files that end with `.jpeg`, `.jpg`, `.png`.

### Create a panorama

1. In your universe folder, create a folder named `<Name of your panorama>.panorama` (e.g. `My Panorama.panorama`).
2. Drag and drop all the files which are composing your panorama in this folder.

### Projection types

Two types of projection are supported.

#### Spherical projection

Place a single image with the spherical projection of the scene in the folder. 

**Important** : Do not place any other images in this folder (except `_preview` files).

#### Cube projection

Place 6 images, corresponding to the six faces of your cube in the folder.

**Naming** : your files should respect the following conventions:
   * *up* : named "u" or matches "\_u\_" (e.g. "u.jpg", "bl_u_bl.jpg")
   * *down* : named "d" or matches "\_d\_" (e.g. "d.jpg", "bl_d_bl.jpg")
   * *front* : named "f" or matches "\_f\_" (e.g. "f.jpg", "bl_f_bl.jpg")
   * *back* : named "b" or matches "\_b\_" (e.g. "b.jpg", "bl_b_bl.jpg")
   * *left* : named "l" or matches "\_l\_" (e.g. "l.jpg", "bl_l_bl.jpg")
   * *right* : named "r" or matches "\_r\_" (e.g. "r.jpg", "bl_r_bl.jpg")

**Important** : Do not place any other images in this folder (except `_preview` files).

[Back to Supported Content](index.md)

