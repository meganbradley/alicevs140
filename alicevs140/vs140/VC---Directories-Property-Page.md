---
title: "VC++ Directories Property Page"
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
ms.assetid: 428eeef6-f127-4271-b3ea-0ae6f2c3d624
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VC++ Directories Property Page
Specifies the directories that you want Visual Studio to use to build a project. To access this property page, in **Solution Explorer**, open the shortcut menu for the project and choose **Properties**, and then in the left pane of the **Property Pages** dialog box, expand **Configuration Properties** and select **VC++ Directories**.  
  
 When you use Visual Studio to create a project, it inherits certain directories. Many of these are given as macros. To examine the current value of a macro, in the right pane of the **VC++ Directories** page, select a row—for example, **Include Directories**—choose the down-arrow button on the right, choose **Edit**, and then in the dialog box that appears, choose the **Macros** button. For more information, see these blog posts: [VC++ Directories](http://blogs.msdn.com/b/vsproject/archive/2009/07/07/vc-directories.aspx), [Inherited Properties and Property Sheets](http://blogs.msdn.com/b/vsproject/archive/2009/06/23/inherited-properties-and-property-sheets.aspx), and [Visual Studio 2010 C++ Project Upgrade Guide](http://blogs.msdn.com/b/vcblog/archive/2010/03/02/visual-studio-2010-c-project-upgrade-guide.aspx).  
  
## Directory Types  
 You can also specify other directories, as follows.  
  
 **Executable Directories**  
 Directories in which to search for executable files. Corresponds to the **PATH** environment variable.  
  
 **Include Directories**  
 Directories in which to search for include files that are referenced in the source code. Corresponds to the **INCLUDE** environment variable.  
  
 **Reference Directories**  
 Directories in which to search for assembly and module (metadata) files that are referenced in the source code by the [#using](../vs140/#using-Directive--C---.md) directive. Corresponds to the **LIBPATH** environment variable.  
  
 **Library Directories**  
 Directories in which to search for libraries (.lib) files; this includes run-time libraries. Corresponds to the **LIB** environment variable. This setting does not apply to .obj files; to link to an .obj file, on the [Linker](../Topic/Linker%20Property%20Pages.md)**General** property page, select **Additional Library Dependencies** and then specify the relative path of the file.  
  
 **Source Directories**  
 Directories in which to search for source files to use for IntelliSense.  
  
 **Exclude Directories**  
 Directories not to search when checking for build dependencies.  
  
#### To specify or modify directory settings  
  
1.  In **Solution Explorer**, open the shortcut menu for the project you want to change and then choose **Properties**.  
  
2.  In the left pane of the **Property Pages** dialog box, expand **Configuration Properties** and then select **VC++ Directories**.  
  
3.  To modify one of the directory lists, select it, choose the down-arrow button on the right, and then choose **Edit**.  
  
     In the box in the dialog box that appears, you can add or remove values, and you can rearrange the order in which the values appear. You can also change whether the project inherits any settings by selecting or clearing **Inherit from parent or project defaults**.  
  
## Sharing the Settings  
 You can share project properties with other users or across multiple computers. For more information, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
## See Also  
 [Working with Project Properties](../vs140/Working-with-Project-Properties.md)