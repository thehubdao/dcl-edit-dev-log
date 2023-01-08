# 002 - Happy New Year

After a short holiday, we are back with the weekly dev log. Despite the holiday, we've continued our work on dcl-edit. 

## UI Test suit

dcl-edit contains a lot of UI. From input fields in the inspector to the context menu when right-clicking on stuff.
For that, we have developed a UI Builder, which purpose it is, to make it easier to add new UI. But it needs to be 
tested. For that, we created the UI Test suit. It's a semi-automated test, that will show some UI to a tester (a person)
and prompt the tester with a task or a question. That way, we can quickly see, if the UI still works as intended.

![grafik](https://user-images.githubusercontent.com/11379989/211175391-d87cf4de-a2d6-472b-8cf1-66037bdbf10c.png)

![grafik](https://user-images.githubusercontent.com/11379989/211175336-199b3b4e-8fed-4dc2-b79f-84f654fc219f.png)

## Gizmo rotation on scaled parents

The gizmos are meant to act as a handle for the user to manipulate entities in the scene, like moving or rotating them. These need to be displayed on the entity, they are meant to modify. This was not the case, because of a bug with how the transform of child entities was calculated. This was fixed, and now the gizmos show exactly, where they're supposed to show.
