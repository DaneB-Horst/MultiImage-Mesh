# Image2Mesh – Blender Batch Image Importer

A lightweight Python script for Blender that allows you to import multiple images and automatically convert them into individual textured mesh planes.

Image2Mesh is designed to speed up workflows where large numbers of images need to be imported into Blender as separate 3D objects.

## Features

- **Batch Image Import:** Select and import multiple images simultaneously.
- **Multiple Formats:** Supports PNG, JPG, JPEG, TIFF, BMP and WebP.
- **Automatic Mesh Creation:** Each imported image becomes an individual mesh plane.
- **Aspect Ratio Preservation:** Automatically calculates the correct dimensions to maintain the original image proportions.
- **Automatic Materials:** Creates a dedicated material for each image.
- **Transparency Support:** Connects image alpha channels to the material transparency input.
- **Grid Layout:** Automatically arranges imported images into a clean grid.
- **Customisable Spacing:** Control the distance between image planes.
- **Collection Organisation:** Places all imported objects inside a collection called `Imported Image Meshes`.
- **Automatic Naming:** Uses the original image filename for the mesh object and material.

## Requirements

- Blender 4.x or newer
- Blender 5.x compatible

## Installation

1. Download or clone this repository.
2. Download the `Image2Mesh.py` script.
3. Open Blender.
4. Switch to the **Scripting** workspace.
5. Create a new text block.
6. Open and paste the contents of `Image2Mesh.py`.
7. Click **Run Script**.

Once executed, the importer will be available under:

`File → Import → Multiple Images as Meshes`

## How to Use

1. Navigate to **File → Import → Multiple Images as Meshes**.
2. Browse to the folder containing your images.
3. Select multiple images using `Shift` or `Ctrl`.
4. Adjust the import settings.
5. Click **Import**.

Image2Mesh will automatically create a mesh plane for each image, assign its material and arrange the objects in a grid.

## Import Settings

| Setting | Default | Description |
|---|---:|---|
| Columns | 5 | Number of images per row |
| Maximum Image Size | 2.5 | Maximum width or height of each plane |
| Spacing | 3.5 | Distance between image planes |

## Supported Image Formats

| Format | Supported |
|---|---|
| PNG | Yes |
| JPG / JPEG | Yes |
| TIFF | Yes |
| BMP | Yes |
| WebP | Yes |

**Note:** Animated WebP files are imported as still images, not animated sequences.

## Collection Structure

All imported objects are organised into:

`Imported Image Meshes`

Each image receives:
- An individual mesh object.
- An individual material.
- An image texture connected to the material.
- Automatically generated UV coordinates.

## Transparency

Image2Mesh connects the image texture's alpha channel to the Principled BSDF shader.

Transparent PNG and WebP images can therefore retain their transparency when rendered, subject to the material and render settings.

## Use Cases

Image2Mesh is useful for:

- Motion graphics workflows.
- Product image layouts.
- Reference image collections.
- Texture and image galleries.
- Game asset preparation.
- Automated image-to-plane workflows.
- Importing large batches of visual assets.

## Known Limitations

- Animated WebP files are not imported as animations.
- Each image is imported as a flat plane.
- Images are arranged in a grid rather than individually positioned.
- Image dimensions are preserved, but the maximum image size is controlled by the import settings.

## Future Improvements

Potential features for future versions:

- Custom plane orientation (XY, XZ and YZ).
- Randomised image placement.
- Automatic image alignment.
- Individual image scaling.
- Material configuration options.
- Improved collection management.
- Native Blender add-on installation.

## License

This project is open source. See the repository's LICENSE file for usage and distribution terms.

---

**Image2Mesh – Batch Image Importer for Blender**

A simple tool to make importing multiple images into Blender faster and easier.
