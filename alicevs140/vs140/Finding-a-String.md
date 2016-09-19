---
title: "Finding a String"
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
ms.assetid: c2497173-f356-4f77-97d6-f0ac41782510
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Finding a String
You can search for one or more strings in the string table, and use [regular expressions](../vs140/Using-Regular-Expressions-in-Visual-Studio.md) with the **Find in Files** command (**Edit** menu) to locate all instances of strings that match a pattern.  
  
### To find a string in the string table  
  
1.  Open the string table by double-clicking its icon in [Resource View](../vs140/Resource-View-Window.md).  
  
    > [!NOTE]
    >  If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../vs140/How-to--Create-a-Resource-Script-File.md).  
  
2.  On the **Edit** menu, click **Find and Replace**, then choose **Find**.  
  
3.  In the **Find What** box, select a previous search string from the drop-down list or type the caption text or resource identifier of the string you want to find.  
  
4.  Select any of the **Find** options.  
  
5.  Click **Find Next**.  
  
    > [!TIP]
    >  To use regular expressions when searching files, use the **Find in Files** command. Type a regular expression to match a pattern or click the button to the right of the **Find What** box to display a list of regular search expressions. When you select an expression from this list, it is substituted as the search text in the **Find What** box. If you use regular expressions, be sure the **Use: Regular Expressions** check box is selected.  
  
 For information on adding resources to managed projects (those that target the common language runtime), please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 **Requirements**  
  
 Win32  
  
## See Also  
 [String Editor](../vs140/String-Editor.md)   
 [Strings](_win32_Strings)   
 [About Strings](_win32_About_Strings_cpp)