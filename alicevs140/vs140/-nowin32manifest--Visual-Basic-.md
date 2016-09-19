---
title: "-nowin32manifest (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
H1: /nowin32manifest (Visual Basic)
ms.assetid: c0528aae-83b3-4425-99f0-19448e9843e3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -nowin32manifest (Visual Basic)
Instructs the compiler not to embed any application manifest into the executable file.  
  
## Syntax  
  
```  
/nowin32manifest  
```  
  
## Remarks  
 When this option is used, the application will be subject to virtualization on Windows Vista unless you provide an application manifest in a Win32 Resource file or during a later build step. For more information about virtualization, see [ClickOnce Deployment on Windows Vista](../vs140/ClickOnce-Deployment-on-Windows-Vista.md).  
  
 For more information about manifest creation, see [/win32manifest (Visual Basic)](../vs140/-win32manifest--Visual-Basic-.md).  
  
## See Also  
 [Visual Basic Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [Application Page, Project Designer (Visual Basic)](../Topic/Application%20Page,%20Project%20Designer%20\(Visual%20Basic\).md)