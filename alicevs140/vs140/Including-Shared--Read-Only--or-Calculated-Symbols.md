---
title: "Including Shared (Read-Only) or Calculated Symbols"
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
ms.assetid: 32b77faf-a066-4371-a072-9a5b84c0766d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Including Shared (Read-Only) or Calculated Symbols
The first time the development environment reads a resource file created by another application, it marks all included header files as read-only. Subsequently, you can use the [Resource Includes dialog box](../vs140/Resource-Includes-Dialog-Box.md) to add additional read-only symbol header files.  
  
 One reason you may want to use read-only symbol definitions is for symbol files that you plan to share among several projects.  
  
 You can also use included symbol files when you have existing resources with symbol definitions that use expressions rather than simple integers to define the symbol value. For example:  
  
```  
#define   IDC_CONTROL1 2100  
#define   IDC_CONTROL2 (IDC_CONTROL1+1)  
```  
  
 The environment will correctly interpret these calculated symbols as long as:  
  
-   The calculated symbols are placed in a read-only symbols file.  
  
-   Your resource file contains resources to which these calculated symbols are already assigned.  
  
-   A numeric expression is expected.  
  
> [!NOTE]
>  If a string or a numeric expression is expected, then the expression is not evaluated.  
  
### To include shared (read-only) symbols in your resource file  
  
1.  In [Resource View](../vs140/Resource-View-Window.md), right-click your .rc file and choose [Resource Includes](../vs140/Resource-Includes-Dialog-Box.md) from the shortcut menu.  
  
    > [!NOTE]
    >  If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../vs140/How-to--Create-a-Resource-Script-File.md).  
  
2.  In the **Read-only symbol directives** box, use the **#include** compiler directive to specify the file where you want the read-only symbols to be kept.  
  
     Do not call the file Resource.h, since that is the filename normally used by the main symbol header file.  
  
    > [!NOTE]
    >  **Important** What you type in the Read-Only symbol directives box is included in the resource file exactly as you type it. Make sure what you type does not contain any spelling or syntax errors.  
  
     Use the **Read-only symbol directives** box to include files with symbol definitions only. Do not include resource definitions; otherwise, duplicate resource definitions will be created when the file is saved.  
  
3.  Place the symbols in the file you specified.  
  
     The symbols in files included in this way are evaluated each time you open your resource file, but they are not replaced on the disk when you save your file.  
  
4.  Click **OK**.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 Requirements  
  
 Win32  
  
## See Also  
 [Symbol Name Restrictions](../vs140/Symbol-Name-Restrictions.md)   
 [Symbol Value Restrictions](../vs140/Symbol-Value-Restrictions.md)   
 [Predefined Symbol IDs](../vs140/Predefined-Symbol-IDs.md)   
 [Symbols: Resource Identifiers](../vs140/Symbols--Resource-Identifiers.md)