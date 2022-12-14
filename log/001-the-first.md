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


I hope you will enjoy reading it, because I did not enjoy writing it.
