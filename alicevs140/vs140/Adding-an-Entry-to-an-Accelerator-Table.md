---
title: "Adding an Entry to an Accelerator Table"
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
ms.assetid: 559c2415-8323-4339-9447-6966665f8288
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding an Entry to an Accelerator Table
### To add an entry to an accelerator table  
  
1.  Open the accelerator table by double-clicking its icon in [Resource View](../vs140/Resource-View-Window.md).  
  
    > [!NOTE]
    >  If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../vs140/How-to--Create-a-Resource-Script-File.md).  
  
2.  Right-click within the accelerator table and choose **New Accelerator** from the shortcut menu, or click on the empty row entry at the bottom of the table.  
  
3.  Select an ID from the drop-down list in the [ID](../vs140/ID-Property.md) box or type a new ID in the **ID** box.  
  
4.  Type the [Key](../vs140/Accelerator-Key-Property.md) you want to use as an accelerator or right-click and choose **Next Key Typed** from the shortcut menu to set a key combination (the **Next Key Typed** command is also available from the **Edit** menu).  
  
5.  Change the [Modifier](../vs140/Accelerator-Modifier-Property.md) and [Type](../vs140/Accelerator-Type-Property.md), if necessary.  
  
6.  Press **ENTER**.  
  
    > [!NOTE]
    >  Make sure all accelerators you define are unique. You can have several key combinations assigned to the same ID with no ill effect, for example, CTRL + P and F8 can both be assigned to ID_PRINT. However, having a key combination assigned to more than one ID will not work well, for example, CTRL + Z assigned to both ID_SPELL_CHECK and ID_THESAURUS.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 **Requirements**  
  
 Win32  
  
## See Also  
 [Editing Accelerator Tables](../vs140/Editing-Accelerator-Tables.md)   
 [Accelerator Editor](../vs140/Accelerator-Editor.md)