# 002 - Happy New Year

After a short holiday, we are back with the weekly dev log. Despite the holiday, we've continued our work on dcl-edit. 

## UI Test suit

dcl-edit contains a lot of UI. From input fields in the Inspector to the context menu when right-clicking on stuff.
For that, we have developed a UI Builder, whose purpose it is to make it easy to add new UI. But that UI Builder needs to be 
tested. For that, we created the UI Test Suite. It's a semi-automated test, that will show some UI to a tester (a person)
and prompt the tester with a task or a question. That way, we can quickly see, if the UI still works as intended.

![grafik](https://user-images.githubusercontent.com/11379989/211175391-d87cf4de-a2d6-472b-8cf1-66037bdbf10c.png)

![grafik](https://user-images.githubusercontent.com/11379989/211175336-199b3b4e-8fed-4dc2-b79f-84f654fc219f.png)

## Problems with gizmo tools and transforms

The gizmo tools are meant to act as a handle for the user to manipulate entities in the scene, like moving or rotating
them. These need to be displayed on the entity, they are meant to modify. This was not the case, because of a bug with
how the transform of child entities was calculated. This was fixed, and now the tools show exactly, where they're supposed to show.

Also related to the transform, there was a bug, where the scale "flickered" when it was pushed below -1 with the
scaling gizmo tool. This was fixed, too.

## Removing components

When inspecting an entity, we see all the components on that entity. We also want to be able to remove them. This is
now possible by clicking the red "X".

![grafik](https://user-images.githubusercontent.com/11379989/211175843-53c6a7db-17fc-43e6-bf23-bdd1152c25c2.png)

## Zoom when in context menu

In some cases, like right-clicking some objects, a context menu will pop up. This can theoretically be so big, that it
needs to show a scroll bar and the user needs to scroll in it with the mouse wheel. But when scrolling in the context 
menu while the mouse is also over the scene view, the main scene camera would also scroll in or out. This should not
happen and is now fixed.

## Menu bar

Many applications have a menu bar at the top of the window. Now, dcl-edit has one, too. The first options in there are
related to opening and saving scenes. A scene can now be opened from everywhere. 

![grafik](https://user-images.githubusercontent.com/11379989/211176793-10eec849-dad4-450e-b299-ba8c8e58a1f5.png)

## Settings

There were three settings added.

### UI scale

The user can now specify a scaling factor, that is applied to the entire UI.

![grafik](https://user-images.githubusercontent.com/11379989/211176907-62a29222-d7a0-41d7-a4b9-c4d8bc01424b.png)


### Input sensitivity

The user can now set the sensitivity of the mouse, when navigating the scene view. 

### Gizmo size

The user can now change the size of the gizmo tool. This can be nice, when the tool obscures too much of the scene.

