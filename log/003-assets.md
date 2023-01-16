# 003 Assets

We are thrilled to announce that the asset browser is finally ready and merged! It has taken us multiple months of hard work.
Although it has taken a while, we are proud of the results and are excited to see how it will be used.

## Asset Browser

The asset browser is a tool used to manage assets in a project. It allows users to easily access, view, and organize
assets in a convenient way. With the asset browser, users can quickly find the assets they need.

![grafik](https://user-images.githubusercontent.com/11379989/212622213-fd1be6cc-f42e-459d-b2cf-f4efdac766b9.png)

### Usage

The asset browser allows users to browse assets and easily add them to their scene. They can either drag and drop the
asset or click on it to add it to their scene. The asset will then be added as a gltf shape on an entity.

### Assets from the project

The asset browser supports different asset sources. Currently, assets from the file system need to be in the project
files, and they need to be in a folder called 'assets'. In the future, we plan to expand the asset browser so that it
can use any folder as an asset source, even outside of the project. This will make it easier to exchange assets between
projects.

### Builder assets

Another asset source supported by the asset browser is assets from the legacy builder. All assets available in the 
legacy builder are now accessible through the asset browser. However, smart items do not work with dcl-edit.

![grafik](https://user-images.githubusercontent.com/11379989/212622399-10b41d02-9312-4e0e-8f2b-647f7e31bc9e.png)

## Other updates

Besides the asset browser, we have also been working on other updates.

### Make object duplicates

The user can now duplicate objects by pressing ctrl+d. This is a huge time saver, when creating scenes. This also works
with child entities.

### Fix: Wrong input field selected

When clicking on an input field, the wrong input field was sometimes selected. This was due to a bug in the code, where the 
UI Visuals updated, when there should not update. This was fixed, and now the correct input field stays selected.

### Startup sequence rework

The startup sequence was changed, so that it can handle different cases. This includes cases where dcl-edit needs to open
a new scene or convert a scene from V1 to V2.

### Show available lands in blue

In the scene.json file, there is a list of parcels, that are available to build on. These are now shown in blue in the 
scene view, so that the user can quickly see where to build.

![grafik](https://user-images.githubusercontent.com/11379989/212622510-d30bfed9-9597-40b0-82ed-7699560483ef.png)
