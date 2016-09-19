---
title: "Assigning Access Keys to Menu Commands"
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
ms.assetid: fbcf1a00-af6a-4171-805a-0ac01d4e8b0d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Assigning Access Keys to Menu Commands
You can assign an access key (a mnemonic that allows the user to select the menu with the keyboard) to your menus and menu commands.  
  
### To assign an access (shortcut) key to a menu command  
  
1.  Type an ampersand (**&**) in front of a letter in the menu name or command name to specify that letter as the corresponding access key. For example "&File" sets ALT+F as the shortcut key for the File menu in applications written for Microsoft Windows.  
  
     The menu item will provide a visible cue that one of the letters has a shortcut key assigned to it. The letter following the ampersand will appear underlined (contingent on the operating system).  
  
    > [!NOTE]
    >  Make sure all the access keys on a menu are unique by right-clicking your menu and choosing **Check Mnemonics** from the shortcut menu.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 Requirements  
  
 Win32  
  
## See Also  
 [Menu Editor](../vs140/Menu-Editor.md)