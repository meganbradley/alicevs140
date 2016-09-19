---
title: "Editing a String in a Version Information Resource"
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
ms.assetid: d3a7d4e4-7d31-47c2-902c-f50b8404ba4f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Editing a String in a Version Information Resource
### To edit a string in a version information resource  
  
1.  Click the item once to select it, then again to begin editing it. Make the changes directly in the Version Information table or in the [Properties window](../vs140/Properties-Window.md). The changes you make will be reflected in both places.  
  
     **Note** When editing the **FILEFLAGS** key in the Version Information editor, you'll notice you cannot set the **Debug**, **Private Build**, or **Special Build** properties (in the Properties window) for .rc files:  
  
    -   The Version Information editor sets the **Debug** property with a #ifdef in the resource script, based on the **_DEBUG** build flag.  
  
    -   If the **Private Build** key has a **Value** set in the Version Information table, the corresponding **Private Build** property (in the Properties window) for the **FILEFLAGS** key will be **True**. If the **Value** is empty, the property will be **False**. Likewise, the **Special Build** key (in the Version Information table) is tied to the **Special Build** property for the **FILEFLAGS** key.  
  
 You can sort the information sequence of the string block by clicking either the Key or the Value column headings. These headings automatically rearrange the information into the selected sequence.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 **Requirements**  
  
 Win32  
  
## See Also  
 [Version Information Editor](../vs140/Version-Information-Editor.md)   
 [Version Information (Windows)](https://msdn.microsoft.com/library/windows/desktop/ms646981.aspx)