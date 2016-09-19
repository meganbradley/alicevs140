---
title: "The project type is not supported by this installation"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 50e92aff-3ce9-4600-94af-4a16e9dffc90
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# The project type is not supported by this installation
This error occurs when you try to open a type of project that requires a software development kit (SDK) that's not installed with Visual Studio. For example, this error occurs if you open Visual Studio on a computer that doesn't have the Visual Studio SDK installed and then try to open a project file for that SDK, such as a VSIX project. (For more information about the Visual Studio SDK, see [Extending Visual Studio](http://go.microsoft.com/fwlink/?LinkID=64968).)  
  
## Workaround  
 You must verify that you have the correct SDK installed for the type of project that you are trying to open.  
  
#### To verify whether you already have the SDK installed  
  
1.  On the menu bar, choose **File**, **New**, **Project**.  
  
2.  In the **New Project** dialog box, expand the **Installed** node, expand the **Templates** node, and then choose the **Other Project Types** node.  
  
3.  Review the available project types to determine whether the project that you're trying to open is available.  
  
 If you can't find the type of project that you're trying to open, you don't have the associated SDK installed. You must locate and install the associated SDK to open the project type.  
  
## See Also  
 [What's New in Visual Studio 2013](../Topic/What's%20New%20in%20Visual%20Studio%202015.md)   
 [Visual Studio Compatibility](../vs140/Porting--Migrating--and-Upgrading-Visual-Studio-Projects.md)