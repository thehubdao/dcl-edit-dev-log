# 004 Launch

Hey dcl-edit community,

Sorry for the radio silence on our dev-logs lately! We've been heads down working on launching dcl-edit and it's been a wild ride. But don't worry, we're here to give you the lowdown on what's been happening since our last update.

We've made some serious progress on improving the dcl-edit experience for you all. Our team has been working tirelessly to bring you some exciting new features and improvements, and we can't wait to share them with you.

Thanks for your patience and support as we continue to make dcl-edit the best scene editor for Decentraland. Let's get into it!

## Asset property
One of the new features we've been working on is the addition of asset properties to dcl-edit. Previously, a property could only be a simple text or number, but now it can also be an asset such as a 3D model or another scene. With this new feature, changing an asset property is as easy as clicking on the asset button next to it. This will open up the asset browser, where the user can select a new asset to replace the current one. The asset browser is intuitive and easy to use, making it simple to find the perfect asset for your scene. 

![grafik](https://user-images.githubusercontent.com/11379989/226687687-5613acaa-a5e6-4978-a1c0-52b4239d0b06.png)

## Context menu in hierarchy
We have recently implemented a new feature that allows users to interact with items in the hierarchy using right-click. Now, by right-clicking on an item in the hierarchy or on the empty space under it, a context menu will appear with several options. These options include adding a new entity, deleting an existing entity, and duplicating an entity. Additionally, users can also change the hierarchy order of an entity, like moving it up or down in the list. This feature provides a way to manage items in the hierarchy, without having to use drag and drop.

![grafik](https://user-images.githubusercontent.com/11379989/226688152-b2185695-034c-43a9-bb1b-8dc7db613b9d.png)

## Menu bar
We've recently added a menu bar to dcl-edit, which is a bar that sits at the top of the window and provides easy access to various functions. When clicking on a point in the menu bar, a sub-menu will appear with additional options. The "File" menu point contains options to create a new scene, open an existing scene, save a scene, save a scene with a new name, and exit the application. The "Edit" menu point provides the ability to undo and redo actions, which can be especially useful during the scene creation process. The menu bar is a great way to quickly access common functions, which can save time and make scene creation more efficient.

![grafik](https://user-images.githubusercontent.com/11379989/226687893-0f1d638b-f677-4926-9a64-e9f7f55edc8d.png)

## Buttons in scene view
In dcl-edit, the buttons in the top left of the scene view have been added to provide users with more control and functionality. The first three buttons allow users to quickly switch between transform, rotate, and scale tools for editing their scene. The next two buttons enable users to switch between local and global editing modes, providing more precise control over the position, rotation, and scale of objects. Finally, the last button toggles tool snapping, which can be useful for aligning objects and making precise adjustments. 

![grafik](https://user-images.githubusercontent.com/11379989/226687938-291672a8-6a4b-4624-8ab9-aed04e202f3a.png)

## Scenes in scenes
A significant development in dcl-edit is the addition of scene nesting. This means that users can now create scenes within scenes, providing a way to create more complex and interactive experiences. The scene nesting feature can be accessed by adding the "Scene" component to an entity in the scene. This component allows users to reference a separate scene file and embed it within the parent scene. It's important to note that circular dependencies are not allowed, so users must be mindful of the hierarchy of their scenes to avoid any issues.

## Generate with assets
We've added asset support into the typescript generation process. This means that the typescript that's generated from the scene will now contain references to the assets, allowing the scene to load them properly when it's being rendered in Decentraland. To ensure that only the necessary assets are included in the build files, we have implemented a system that copies the assets as needed, leaving the unnecessary assets out.

## Reopen last opened scene
One of the recent improvements we've made to dcl-edit is the ability to automatically open the last opened scene on startup. This feature is a time-saver for users who are frequently working on the same scene and don't want to waste time searching for it every time they open the editor. Now, when users launch dcl-edit, the last opened scene will be loaded automatically, making the start-up process more efficient.

## Hierarchy order
We have made significant improvements to the hierarchy system in dcl-edit. Users can now freely sort the hierarchy list by dragging and dropping the items or by using the right-click options. This makes it easier to organize the scene and manage large amounts of items. In addition, entities can now be parented within the hierarchy, allowing users to group related objects and control their behavior as a unit.

## Comma as decimal separator
In response to user feedback, we have added a new feature to dcl-edit that allows users to use commas as a decimal separator in addition to the period. Previously, only the period was accepted as a decimal separator, which could be problematic for users with non-English numpads that have a comma as the default separator.

## Many bug fixes
We've fixed many bugs in dcl-edit, most of which were minor issues that affected the user experience. We addressed some problems with the gizmo and with undoing actions. These fixes represent a significant improvement for the editor, and we're continuing to make improvements.


##

That's all for now, folks! We've been working hard to improve the dcl-edit experience for our users, and we hope you enjoy these new features and improvements. We'll continue to work on fixing bugs and adding new functionality, so stay tuned for future updates. Thank you for your support!
