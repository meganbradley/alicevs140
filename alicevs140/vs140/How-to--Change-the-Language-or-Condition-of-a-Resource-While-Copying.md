---
title: "How to: Change the Language or Condition of a Resource While Copying"
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
ms.assetid: 8f622ab0-bac2-468f-ae70-78911afc4759
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Change the Language or Condition of a Resource While Copying
While copying in a resource, you can change its language property or condition property, or both.  
  
-   The language of the resource identifies just that, the language for the resource. This is used by [FindResource](http://msdn.microsoft.com/library/windows/desktop/ms648042) to help identify the resource for which you're looking. (However, resources can have differences for each language that aren't related to text, for example, accelerators that might only work on a Japanese keyboard or a bitmap that would only be appropriate for Chinese localized builds, etc.)  
  
-   The condition of a resource is a defined symbol that identifies a condition under which this particular copy of the resource is to be used.  
  
 The language and condition of a resource are shown in parentheses after the name of the resource in the Workspace window. In this example the resource named IDD_AboutBox is using Finnish as its language and its condition is XX33.  
  
```  
IDD_AboutBox (Finnish – XX33)  
```  
  
### To copy an existing resource and change its language or condition  
  
1.  In the .rc file or in the [Resource View](../vs140/Resource-View-Window.md) window, right-click the resource you want to copy.  
  
2.  Choose **Insert Copy** from the shortcut menu.  
  
3.  In the **Insert Resource Copy** dialog box:  
  
    -   For the **Language** list box, select the language.  
  
    -   In the **Condition** box, type the condition.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 Requirements  
  
 Win32  
  
## See Also  
 [How to: Copy Resources](../vs140/How-to--Copy-Resources.md)   
 [Resource Files](../vs140/Resource-Files--Visual-Studio-.md)   
 [Resource Editors](../vs140/Resource-Editors.md)