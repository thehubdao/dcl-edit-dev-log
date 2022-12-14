# 001 - The first one
Hello.

This is the first dev log for dcl-edit.
In these dev logs, we will show you, what we've been workin on for the last week.
Because this is the first one, there will be more than usual to talk about. 

### Rework Ui Builer
dcl-edit is ment to be a professional tool. To ensure a unique look, across the programm, we've made the Ui Builder. 
It's main purpose is to act as an abstraction layer between scripts and the actual UI. When I want to display three texts and a button somewhere,
I don't create that in unity, but I ask the Ui Builder to put tree texts and a button to whrere ever its needed.

The Ui Builder itself was not realy optimized. When ever we asked the Builder to Update the content, it deleted the entire Ui and recreated it.

After the rework, it will detect what needs to be updatet and what not. And when an Ui Element needs to be created or deleted, it will use an object pool
for that. That means, when we "delete" an object, it will only be disabled and stored away. When we "create" an object, it will first look for an object,
that can be used, instead of actually creating a new one.

### Save panel size
The dcl-edit beta will feature freely arangeable pannels. This is archived with the Unity Package 
[Dynamic Panels](https://github.com/yasirkula/UnityDynamicPanels) by yasirkula
![grafik](https://user-images.githubusercontent.com/11379989/207691957-021c71aa-cfab-4084-a53b-06eb23ac6338.png)
The arangement of these panels are now saved on a user level. That means, even when you open two different projects, your personal panel arangement will
be the same in both.

### Input validation
There are many places, where a user can type in a number into a textfield. These textfields did not block the user from entering non numbers. That led to 
errors while executing. Now, when ever the input is invalid, it will turn the textfield red and inform the underlying system about it.
![grafik](https://user-images.githubusercontent.com/11379989/207696359-c986fc20-76eb-4100-a5f1-9a06ff27e8e7.png)
