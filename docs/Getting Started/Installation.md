# Installation

You need to make sure that your project is either a C++ project if you're starting fresh, or you have added a C++ class to 
get access to a Source Folder & Visual Studio Solution.


If you are downloading the raw plugin, then you simply need to make sure that the project folder structure looks like:

```
 - Project Folder
   - Plugins
     - ClueSystemPlugin
```

Then right click on the UProject file, and select GenerateVisualStudioFiles to get a VS Solution with the new plugin. Build the 
project again by opening the project normally. You should be prompted to rebuild certain modules, including the 2 modules in this plugin. 
Select Yes and it will rebuild the project and when the project eventually opens, the plugin should be working. 