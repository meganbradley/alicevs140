---
title: "Edit and Continue Error Message Dialog Box"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f98c91c0-447a-4533-85b6-87170a0dc4c3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Edit and Continue Error Message Dialog Box
This dialog box appears when you are debugging in a language that supports Edit and Continue, but **Edit and Continue** is not available for the type of code changes you have made. The error message inside the box provides a more detailed explanation. Possible reasons for seeing this dialog box include:  
  
-   You tried to edit managed code when unmanaged debugging was enabled. Edit and Continue does not work with mixed-mode debugging.  
  
-   You tried to edit SQL Server code.  
  
-   You tried to edit code while debugging a Dr. Watson dump.  
  
-   You tried to edit code after an unhandled exception occurred and the option "**Unwind the call stack on unhandled exceptions**" was not selected.  
  
-   You tried to edit code while debugging an embedded runtime application.  
  
-   You tried to edit code in a program that you attached to rather than starting from the **Debug** menu.  
  
-   You tried to edit optimized code.  
  
-   You tried to edit managed code when the target is a 64-bit application. If you want to use Edit and Continue, you must set the target to x86. (*Project* **Properties**, **Compile** tab, **Advanced Compiler** setting.).  
  
-   You tried to edit code in an assembly that was modified during debugging and has been reloaded.  
  
-   You tried to edit code in an assembly that has not been loaded.  
  
-   You started debugging an old version of your application (since the new version has build errors).  
  
-   You tried to edit code while it was running.  
  
## UIElement List  
 **OK**  
 Exit the dialog box and cancel the immediately preceding edit attempt.  
  
## See Also  
 [Supported Code Changes](../vs140/Supported-Code-Changes--C---.md)