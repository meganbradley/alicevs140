---
title: "Symbol Name Restrictions"
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
ms.assetid: 4ae7f695-ca86-4f4b-989a-fe6f89650ff7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Symbol Name Restrictions
The restrictions on symbol names are as follows:  
  
-   All [symbols](../vs140/Symbols--Resource-Identifiers.md) must be unique within the scope of the application. This prevents conflicting symbol definitions in the header files.  
  
-   Valid characters for a symbol name include A-Z, a-z, 0-9, and underscores ( _ ).  
  
-   Symbol names cannot begin with a number and are limited to 247 characters.  
  
-   Symbol names cannot contain spaces.  
  
-   Symbol names are not case sensitive, but the case of the first symbol definition is preserved. The header file that defines the symbols is used by both the resource compiler/editor and C++ program(s) to refer resources defined in a resource file. For two symbol names that differ only in case, the C++ program will see two separate symbols while the resource compiler/editor will see both names as referring to one single symbol.  
  
    > [!NOTE]
    >  If you do not follow the standard symbol name scheme (ID*_[keyword]) outlined below, and your symbol name happens to be the same as a keyword known to the resource script compiler, trying to build the resource script file will result in seemingly random error generation that is difficult to diagnose. To prevent this, adhere to the standard naming scheme.  
  
 Symbol names have descriptive prefixes that indicate the kind of resource or object they represent. These descriptive prefixes begin with the text combination ID. The Microsoft Foundation Class Library (MFC) uses the symbol naming conventions shown in the following table.  
  
|Category|Prefix|Use|  
|--------------|------------|---------|  
|Resources|IDR_ IDD_ IDC_ IDI_ IDB_|Accelerator or menu (and associated or custom resources) Dialog box Cursor Icon Bitmap|  
|Menu items|ID_|Menu item|  
|Commands|ID_|Command|  
|Controls and child windows|IDC_|Control|  
|Strings|IDS_|String in the string table|  
|MFC|AFX_|Reserved for predefined MFC symbols|  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
## Requirements  
 Win32  
  
## See Also  
 [Changing a Symbol or Symbol Name (ID)](../vs140/Changing-a-Symbol-or-Symbol-Name--ID-.md)   
 [Symbol Value Restrictions](../vs140/Symbol-Value-Restrictions.md)   
 [Predefined Symbol IDs](../vs140/Predefined-Symbol-IDs.md)