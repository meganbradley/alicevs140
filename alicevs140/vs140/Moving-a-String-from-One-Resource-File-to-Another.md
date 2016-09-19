---
title: "Moving a String from One Resource File to Another"
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
ms.assetid: 94f8ee81-9b4c-4788-ba95-68c58db38029
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Moving a String from One Resource File to Another
### To move a string from one resource script file to another  
  
1.  Open the string tables in both .rc files. (For more information, see [Viewing Resources in a Resource Script File Outside of a Project](../vs140/How-to--Open-a-Resource-Script-File-Outside-of-a-Project--Standalone-.md).)  
  
    > [!NOTE]
    >  If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../vs140/How-to--Create-a-Resource-Script-File.md).  
  
2.  Right-click the string you want to move and choose **Cut** from the shortcut menu.  
  
3.  Place the cursor in the target **String Editor** window.  
  
4.  In the .rc file to which you want to move the string, right-click and choose **Paste** from the shortcut menu.  
  
    > [!NOTE]
    >  If the **ID** or **value** of the moved string conflicts with an existing **ID** or **value** in the destination file, either the **ID** or the **value** of the moved string changes. If a string exists with the same **ID**, the **ID** of the moved string changes. If a string exists with the same **value**, the **value** of the moved string changes.  
  
 For information on adding resources to managed projects (those that target the common language runtime), please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 **Requirements**  
  
 Win32  
  
## See Also  
 [String Editor](../vs140/String-Editor.md)   
 [Resource Files](../vs140/Resource-Files--Visual-Studio-.md)   
 [Customizing window layouts](../vs140/Customizing-window-layouts-in-Visual-Studio.md)   
 [Strings](_win32_Strings)   
 [About Strings](_win32_About_Strings_cpp)