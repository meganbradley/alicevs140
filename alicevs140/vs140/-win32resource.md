---
title: "-win32resource"
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
H1: /win32resource
ms.assetid: e226946d-19ce-4cc9-91f5-aed24f77aa2b
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -win32resource
Inserts a Win32 resource file in the output file.  
  
## Syntax  
  
```  
/win32resource:filename  
```  
  
## Arguments  
 `filename`  
 The name of the resource file to add to your output file. Enclose the file name in quotation marks (" ") if it contains a space.  
  
## Remarks  
 You can create a Win32 resource file with the Microsoft Windows Resource Compiler (RC).  
  
 A Win32 resource can contain version or bitmap (icon) information that helps identify your application in **File Explorer**. If you do not specify `/win32resource`, the compiler generates version information based on the assembly version. The `/win32resource` and `/win32icon` options are mutually exclusive.  
  
 See [/linkresource (Visual Basic)](../vs140/-linkresource--Visual-Basic-.md) to reference a [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] resource file, or [/resource (Visual Basic)](../Topic/-resource%20\(Visual%20Basic\).md) to attach a [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] resource file.  
  
> [!NOTE]
>  The `/win32resource` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.  
  
## Example  
 The following code compiles `In.vb` and attaches a Win32 resource file, `Rf.res`:  
  
```  
vbc /win32resource:rf.res in.vb  
```  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)