---
title: "How to: Create a Resource"
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
ms.assetid: aad44914-9145-45a3-a7d8-9de89b366716
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a Resource
> [!NOTE]
>  Resource View is not supported in Express editions.  
  
### To create a new resource in Resource View  
  
1.  With focus on your .rc file in [Resource View](../vs140/Resource-View-Window.md), click the **Edit** menu and choose **Add Resource** (or right-click the .rc file in Resource View and choose **Add Resource** from the shortcut menu).  
  
     **Note** If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../vs140/How-to--Create-a-Resource-Script-File.md).  
  
2.  In the [Add Resource dialog box](../vs140/Add-Resource-Dialog-Box.md), choose the type of resource you'd like to add to your project.  
  
### To create a new resource in Solution Explorer  
  
1.  In **Solution Explorer**, right-click the project folder and choose **Add**, then click **Add Resource** on the shortcut menu.  
  
     If you do not already have an .rc file in your project, this step will create one. You can then repeat this step to add specific resource types to the new .rc file.  
  
2.  In the [Add Resource dialog box](../vs140/Add-Resource-Dialog-Box.md), choose the type of resource you'd like to add to your project.  
  
### To create a new resource in Class View  
  
1.  In [Class View](assetId:///8d7430a9-3e33-454c-a9e1-a85e3d2db925), right-click your class and choose **Add**, then click **Add Resource** from the shortcut menu.  
  
2.  In the [Add Resource dialog box](../vs140/Add-Resource-Dialog-Box.md), choose the type of resource you'd like to add to your project.  
  
### To create a new resource from the Project menu  
  
1.  From the **Project** menu, choose **Add Resource**.  
  
 When you create a new resource, Visual C++ assigns a unique name to it, for example, IDD_Dialog1. You can customize this resource ID by editing the properties for the resource either in the associated resource editor or in the [Properties Window](../vs140/Properties-Window.md).  
  
 You can create a resource as a new default resource (a resource that is not based on a template) or as a resource patterned after a [template](../vs140/How-to--Use-Resource-Templates.md).  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.*  
  
 **Requirements**  
  
 Win32  
  
## See Also  
 [Resource Files](../vs140/Resource-Files--Visual-Studio-.md)   
 [Resource Editors](../vs140/Resource-Editors.md)   
 [Add Resource Dialog Box](../vs140/Add-Resource-Dialog-Box.md)