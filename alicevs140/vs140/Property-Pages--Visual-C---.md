---
title: "Property Pages (Visual C++)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 13ffe3ea-1bc3-4bee-be5e-053a8a99cce4
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property Pages (Visual C++)
By using property pages, you can specify settings for Visual Studio projects. To open the **Property Pages** dialog box for a Visual Studio project, on the **Project** menu, click **Properties**.  
  
 You can specify project settings so that they apply all build configurations, or you can specify different project properties for each build configuration. For example, you can specify certain settings for the Release configuration and other settings for the Debug configuration.  
  
 Not all available pages are necessarily displayed in the **Property Pages** dialog box. Which pages are displayed depends on the file types in the project.  
  
 For more information, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
## Default Properties vs. Modified Properties  
 When you use the **New Project** dialog box to create a project, [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] uses the specified project template to initialize the project properties. Therefore, the property values in the template can be thought of as default values for that project type. In other project types, the properties may have different default values.  
  
 A project property value appears in bold if it is modified. A project property can be modified for the following reasons:  
  
-   The application wizard changes the property because it requires a different property value than the one that is specified in the project template.  
  
-   You specify a different property value in the **New Project** dialog box.  
  
-   You specify a different property value on a project property page.  
  
> [!TIP]
>  To see the final set of property values that MSBuild uses to build your project, examine the preprocessor output file, which you can produce by using this command line: **MSBuild /preprocess:***preprocessor_output_filename*opt*project_filename*opt  
  
## Resetting Properties  
 When you view the **Property Pages** dialog box for a project and the project node is selected in **Solution Explorer**, for many properties, you can select **inherit from parent or project defaults** or modify the value another way.  
  
 When you view the **Property Pages** dialog box for a project and a file is selected in **Solution Explorer**, for many properties, you can select **inherit from parent or project defaults** or modify the value another way. However, if the project contains many files that have property values that differ from the project default values, the project will take longer to build.  
  
> [!TIP]
>  To refresh the **Property Pages** dialog box so that it displays the latest selections, click **Apply**.  
  
 Most project defaults are system (platform) defaults. Some project defaults derive from the style sheets that are applied when you update properties in the **Project Defaults** section of the **General** configuration properties page for the project. For more information, see [General Property Page (Project)](../Topic/General%20Property%20Page%20\(Project\).md).  
  
## Specifying User-Defined Values  
 You must define the value for certain properties. A user-defined value can contain one or more alphanumeric characters or project-file macro names. Some of these properties can take only one user-defined value, but others can take a semicolon-delimited list of multiple values.  
  
 To specify a user-defined value for a property, or a list if the property can take multiple user-defined values, in the column to the right of the property name, perform one of the following actions:  
  
-   Type the value or the list of values.  
  
-   Click the drop-down arrow. If **Edit** is available, click it and then in the text box, type the value or list of values. An alternate way to specify a list is to type each value on a separate line in the text box. On the property page, the values will be displayed as a semicolon-delimited list.  
  
     To insert a project-file macro as a value, click **Macros** and then double-click the macro name.  
  
-   Click the drop-down arrow. If **Browse** is available, click it and then select one or more values.  
  
 For a multi-valued property, the **inherit from parent or project defaults** option is available when you click the drop-down arrow in the column to the right of the property name and then click **Edit**. By default, the option is selected.  
  
 Notice that a property page only displays the settings at the current level for a multi-valued property that inherits from another level. For example, if a file is selected in **Solution Explorer** and you select the C/C++ **Preprocessor Definitions** property, file-level definitions are displayed but inherited project-level definitions are not displayed. To view both current-level and inherited values, click the drop-down arrow in the column to the right of the property name and then click **Edit**. If you use the [Visual C++ project model](assetId:///06c1bbd9-4c79-4f97-ad6d-2b1dea8ecd1f), this behavior is also in effect for the objects on files and projects. That is, when you query for the values on a property at the file level, you will not get the values for that same property at the project level. You must explicitly get the values of the property at the project level. Also, some inherited values of a property may come from a style sheet, which is not accessible programmatically.  
  
## In This Section  
  
1.  [NIB: Add Reference Search Path Dialog Box](assetId:///4520d80d-aa9f-4d11-b92b-2f64a1fd5cb2)  
  
2.  [Advanced, Manifest Tool, Configuration Properties, <Projectname\> Property Pages Dialog Box](../vs140/Advanced--Manifest-Tool--Configuration-Properties---Projectname--Property-Pages-Dialog-Box.md)  
  
3.  [Command Line Property Pages](../vs140/Command-Line-Property-Pages.md)  
  
4.  [Custom Build Step Property Page: General](../vs140/Custom-Build-Step-Property-Page--General.md)  
  
5.  [Framework and References, Common Properties, <Projectname\> Property Pages Dialog Box](../vs140/Adding-references-in-Visual-C---projects.md)  
  
6.  [General Property Page (File)](../Topic/General%20Property%20Page%20\(File\).md)  
  
7.  [General Property Page (Project)](../Topic/General%20Property%20Page%20\(Project\).md)  
  
8.  [General, Manifest Tool, Configuration Properties, <Projectname\> Property Pages Dialog Box](../vs140/General--Manifest-Tool--Configuration-Properties---Projectname--Property-Pages-Dialog-Box.md)  
  
9. [HLSL Property Pages](../vs140/HLSL-Property-Pages.md)  
  
10. [HLSL Property Pages: Advanced](../vs140/HLSL-Property-Pages--Advanced.md)  
  
11. [HLSL Property Pages: General](../vs140/HLSL-Property-Pages--General.md)  
  
12. [HLSL Property Pages: Output Files](../vs140/HLSL-Property-Pages--Output-Files.md)  
  
13. [Input and Output, Manifest Tool, Configuration Properties, <Projectname\> Property Pages Dialog Box](../vs140/Input-and-Output--Manifest-Tool--Configuration-Properties---Projectname--Property-Pages-Dialog-Box.md)  
  
14. [Isolated COM, Manifest Tool, Configuration Properties, <Projectname\> Property Pages Dialog Box](../vs140/Isolated-COM--Manifest-Tool--Configuration-Properties---Projectname--Property-Pages-Dialog-Box.md)  
  
15. [Linker Property Pages](../Topic/Linker%20Property%20Pages.md)  
  
16. [Managed Resources Property Page](../vs140/Managed-Resources-Property-Page.md)  
  
17. [Manifest Tool Property Pages](../vs140/Manifest-Tool-Property-Pages.md)  
  
18. [MIDL Property Pages](../vs140/MIDL-Property-Pages.md)  
  
19. [MIDL Property Pages: Advanced](../vs140/MIDL-Property-Pages--Advanced.md)  
  
20. [MIDL Property Pages: General](../vs140/MIDL-Property-Pages--General.md)  
  
21. [MIDL Property Pages: Output](../Topic/MIDL%20Property%20Pages:%20Output.md)  
  
22. [NMake Property Page](../Topic/NMake%20Property%20Page.md)  
  
23. [Resources Property Pages](../Topic/Resources%20Property%20Pages.md)  
  
24. [VC++ Directories Property Page](../vs140/VC---Directories-Property-Page.md)  
  
25. [Web References Property Page](../vs140/Web-References-Property-Page.md)  
  
26. [XML Data Generator Tool Property Page](../vs140/XML-Data-Generator-Tool-Property-Page.md)  
  
27. [XML Document Generator Tool Property Pages](../vs140/XML-Document-Generator-Tool-Property-Pages.md)  
  
## See Also  
 [How to: Create and Remove Project Dependencies](../vs140/How-to--Create-and-Remove-Project-Dependencies.md)   
 [How to: Create and Edit Configurations](../vs140/How-to--Create-and-Edit-Configurations.md)   
 [Deploying Applications](assetId:///4ff8881d-0daf-47e7-bfe7-774c625031b4)