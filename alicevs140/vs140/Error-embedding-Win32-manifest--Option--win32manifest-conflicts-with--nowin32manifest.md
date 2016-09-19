---
title: "Error embedding Win32 manifest: Option -win32manifest conflicts with -nowin32manifest"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: Error embedding Win32 manifest: Option /win32manifest conflicts with /nowin32manifest
ms.assetid: e921b34a-1ab3-4ba0-81b3-e45c62de4718
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error embedding Win32 manifest: Option -win32manifest conflicts with -nowin32manifest
The Visual Basic compiler has been passed both a `/win32manifest` compiler option and a `/nowin32manifest` compiler option. Only one of these options can be passed to the Visual Basic compiler.  
  
 **Error ID:** BC2033  
  
### To correct this error  
  
1.  Remove either the `/win32manifest` compiler option or the `/nowin32manifest` compiler option.  
  
## See Also  
 [/win32manifest (Visual Basic)](../vs140/-win32manifest--Visual-Basic-.md)   
 [/nowin32manifest (Visual Basic)](../vs140/-nowin32manifest--Visual-Basic-.md)   
 [Visual Basic Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)