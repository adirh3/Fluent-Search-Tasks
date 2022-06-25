# Fluent-Search-Tasks
Shared Fluent Search Task Projects to boost your productivity

<img width="745" alt="image" src="https://user-images.githubusercontent.com/27368554/175789605-17419dba-2f1c-4438-ba7d-094026078dc1.png">

## What can you find here?

You can find here Task projects shared by the community that can do various things.  
Each Task project has its own folder, with an explanation.

## How to import Tasks?

To import a Task project, simply download the `.yaml` file and drag and drop it into Fluent Search Tasks window.

## What are Tasks?

Using Tasks you can extend and automate Fluent Search functionality.  
Using Tasks you can automate all of Fluent Search features easily by chaining triggers and operations.

## What is an Operation?
Operation is a way to trigger any Fluent Search functionality. It can do anything, like opening a file, invoking a search result, and more.  
Operations can be connected to each other and will execute in sequential order - only after the last operation is executed.  
Each operation has its own settings and may produce an output (more about that below).

## What is a trigger?
A Trigger is a special kind of Operation that initiates the execution of the Operations chain.  
A Trigger can invoke when a user inputs a search, or when a hotkey is pressed.

## What is a Task project?
A Task project is a set of "operations" that are connected to each other, when one of the Triggers is activated, then all cool stuff begins.

Here is a very simple example -
![Image showing Task project, Hotkey Ctrl+Alt+M connected to Youtube Music, and hotkey Ctrl+Alt+Y connected to Youtube app](https://user-images.githubusercontent.com/27368554/175789729-c49e2e9b-1e71-42ea-934b-bafebb1447f4.png)

The triggers here are two hotkeys, Ctrl+Alt+M and Ctrl+Alt+Y, when invoked the next operation (connected through line) will trigger.    
In this case, it's either the YouTube or YouTube Music apps.

## Inputs
Each operation is configured through settings in its editor window.  

![Image showing inputs window](https://user-images.githubusercontent.com/27368554/175789796-f23b07c1-092d-490f-8b53-77d9180dc18f.png)

For example, here the operation is a search (which is also a trigger), the settings are, as expected, search-related settings.  
For this Trigger, you can configure it to trigger when the user invokes a specific search, depending on the search text, tag, and more.

## Outputs and variables
Operations may have an output, when they do you will have the "Output" tab in the editor window.  
The output can be transformed into Variables, variables are a set of objects that can be accessed through the entire operation chain.  
![Image showing outputs window](https://user-images.githubusercontent.com/27368554/175789817-abe997e3-98ea-4099-89ed-61e3c51525f2.png)  
For example, here the outputs for search are the search text and the search tag.  
Configuring a variable value is done through text, the most simple variable value would be "" which would mean it just tasks the result of the operation.  
For more advanced cases you can get nested values, as for the search trigger, the result is split into two variables "searchText", which is value is "result.SearchedText" and "searchTag"'s value is "result.SearchedTag".

## Variable execution
Variables values are configured through text, but this text is actually based on C#, so any valid C# based syntax should work.  
For example, "{searchText.First()}" would get the first letter of the searchText.
