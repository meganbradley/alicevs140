---
title: "Symbols: Resource Identifiers"
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
ms.assetid: 8fccc09a-0237-4a65-b9c4-57d60c59e324
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Symbols: Resource Identifiers
A symbol is a resource identifier (ID) that consists of two parts: a text string (symbol name) mapped to an integer value (symbol value). For example:  
  
```  
IDC_EDITNAME = 5100  
```  
  
 Symbol names are most often referred to as identifiers.  
  
 Symbols provide a descriptive way of referring to resources and user-interface objects, both in your source code and while you're working with them in the resource editors. You can view and manipulate symbols in one convenient place using the [Resource Symbols dialog box](../vs140/Viewing-Resource-Symbols.md).  
  
 When you create a new resource or resource object, the [resource editors](../vs140/Resource-Editors.md) provide a default name for the resource, for example, `IDC_RADIO1`, and assign a value to it. The name-plus-value definition is stored in the Resource.h file.  
  
> [!NOTE]
>  When you are copying resources or resource objects from one .rc file to another, Visual C++ may change the transferred resource's symbol value, or symbol name and value, to avoid conflicts with symbol names or values in the existing file.  
  
 As your application grows in size and sophistication, so does its number of resources and symbols. Tracking large numbers of symbols scattered throughout several files can be difficult. The [Resource Symbols dialog box](../vs140/Resource-Symbols-Dialog-Box.md) simplifies symbol management by offering a central tool through which you can:  
  
-   [View Resource Symbols](../vs140/Viewing-Resource-Symbols.md)  
  
-   [Create New Symbols](../vs140/Creating-New-Symbols.md)  
  
-   [Change Unassigned Symbols](../vs140/Changing-Unassigned-Symbols.md)  
  
-   [Delete Unassigned Symbols](../vs140/Deleting-Unassigned-Symbols.md)  
  
-   [Open the Resource Editor for a Given Symbol](../vs140/Opening-the-Resource-Editor-for-a-Given-Symbol.md)  
  
-   [Change a Symbol or Symbol Name (ID)](../vs140/Changing-a-Symbol-or-Symbol-Name--ID-.md)  
  
-   [Change a Symbol's Numeric Value](../vs140/Changing-a-Symbol-s-Numeric-Value.md)  
  
-   [Change the Names of Symbol Header Files](../vs140/Changing-the-Names-of-Symbol-Header-Files.md)  
  
-   [Include Shared (Read-Only) or Calculated Symbols](../vs140/Including-Shared--Read-Only--or-Calculated-Symbols.md)  
  
-   [View Predefined Symbol IDs](../vs140/Predefined-Symbol-IDs.md)  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
## Requirements  
 Win32  
  
## See Also  
 [How to: Search for Symbols in Resources](../vs140/How-to--Search-for-Symbols-in-Resources.md)   
 [Resource Editors](../vs140/Resource-Editors.md)   
 [Resource Files](../vs140/Resource-Files--Visual-Studio-.md)