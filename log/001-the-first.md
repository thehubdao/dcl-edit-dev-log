# 001 - The first one
Hello.

This is the first dev log for dcl-edit.
In these dev logs, we will show you, what we've been working on for the last week.
Because this is the first one, there will be more than usual to talk about. 

### Rework Ui Builder
dcl-edit is meant to be a professional tool. To ensure a unique look, across the program, we've made the Ui Builder. 
Its main purpose is to act as an abstraction layer between scripts and the actual UI. When I want to display three texts and a button somewhere,
I don't create that in unity, but I ask the Ui Builder to put tree texts and a button to whrere ever its needed.

The Ui Builder was not really optimized. When ever we asked the Builder to Update the content, it deleted the entire Ui and recreated it.

After the rework, it will detect what needs to be updated and what not. And when an Ui Element needs to be created or deleted, it will use an object pool
for that. That means, when we "delete" an object, it will only be disabled and stored away. When we "create" an object, it will first look for an object,
that can be used, instead of actually creating a new one.

### Save panel size
The dcl-edit beta will feature freely arrangeable panels. This is archived with the Unity Package 
[Dynamic Panels](https://github.com/yasirkula/UnityDynamicPanels) by yasirkula
![grafik](https://user-images.githubusercontent.com/11379989/207691957-021c71aa-cfab-4084-a53b-06eb23ac6338.png)
The arrangement of these panels are now saved on a user level. That means, even when you open two different projects, your personal panel arangement will
be the same in both.

### Input validation
There are many places, where a user can type in a number into a text field. These text fields did not block the user from entering non numbers. That led to 
errors while executing. Now, when ever the input is invalid, it will turn the text field red and inform the underlying system about it.
![grafik](https://user-images.githubusercontent.com/11379989/207696359-c986fc20-76eb-4100-a5f1-9a06ff27e8e7.png)

### Loading animation
When using 3D assets in the scene, we will lazy load those for preview. That means, the assets are only loaded, when they are actually needed, e.g. to be displayed.
But that means, after opening the scene, there will be a short time when the 3D model is not available to be shown. In that time we will show a different object with
a neat little animation.

https://user-images.githubusercontent.com/11379989/207700677-ebd9458c-7710-43e0-81b1-c5690573944d.mp4

### Cap frame rate
dcl-edit is build on the game engine Unity. Being a game engine, it always tries to run as fast as possible. This can lead to high energy consumption
and high usage of processor resources. To prevent that, we've included an option to set a maximum frame rate. That way, the entire editor will update itself less
often and therefore save resources.

### Thumbnail Generator
When organizing 3D assets, we usually want to have a thumbnail, so we can see how a model looks like. In the dcl-edit alpha, we needed to manually add a 
`Thumbnail.png` file. Now that is not needed anymore. When an asset needs to be displayed, but no thumbnail is available, a new one will be generated 
Automatically.

## End of the first one
So, fare well, dear reader. Let your hart be your guide, and it will lead you to great deeds. And remember me who wrote this dev log with blood and tears to
enrich you on your journey.

Peace out
