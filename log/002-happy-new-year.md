# 002 - Happy New Year

After a short holiday, we are back with the weekly dev log. Despite the holiday, we've continued our work on dcl-edit. 

## UI Test suit

dcl-edit contains a lot of UI. From input fields in the inspector to the context menu when right-clicking on stuff.
For that, we have developed a UI Builder, which purpose it is, to make it easier to add new UI. But it needs to be 
tested. For that, we created the UI Test suit. It's a semi-automated test, that will show some UI to a tester (a person)
and prompt the tester with a task or a question. That way, we can quickly see, if the UI still works as intended.

![grafik](https://user-images.githubusercontent.com/11379989/211175391-d87cf4de-a2d6-472b-8cf1-66037bdbf10c.png)

![grafik](https://user-images.githubusercontent.com/11379989/211175336-199b3b4e-8fed-4dc2-b79f-84f654fc219f.png)

## Problems with gizmos tools and transforms

The gizmo tools are meant to act as a handle for the user to manipulate entities in the scene, like moving or rotating them. These need to be displayed on the entity, they are meant to modify. This was not the case, because of a bug with how the transform of child entities was calculated. This was fixed, and now the tools show exactly, where they're supposed to show.

Also related to the transform, there was a bug, where the scale "flickered" when it was pushed below -1 with the scaling gizmo tool. This was fixed, too.

## Removing components

When inspecting an entity, we see all the components on that entity. We also want to be able to remove them. This is now possible by clicking the red "X".

![grafik](https://user-images.githubusercontent.com/11379989/211175843-53c6a7db-17fc-43e6-bf23-bdd1152c25c2.png)

## Zoom when in context menu

In some cases, like right-clicking some objects, a context menu will pop up. This can technical be so big, that it needs to show a scroll bar and the user needs to scroll in it with the mouse wheel. But when scrolling in the context menu, while the mouse is also over the scene view, the main scene camera will also scroll in or out. This should not happen and is now fixed.
