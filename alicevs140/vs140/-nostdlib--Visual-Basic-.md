---
title: "-nostdlib (Visual Basic)"
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
H1: /nostdlib (Visual Basic)
ms.assetid: 140381b8-dc96-4ad5-ae11-792c9ed0be4d
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -nostdlib (Visual Basic)
Causes the compiler not to automatically reference the standard libraries.  
  
## Syntax  
  
```  
/nostdlib  
```  
  
## Remarks  
 The `/nostdlib` option removes the automatic reference to the System.dll assembly and prevents the compiler from reading the Vbc.rsp file. The Vbc.rsp file—which is located in the same directory as the Vbc.exe file—references the commonly used [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] assemblies and imports the `System` and `Microsoft.VisualBasic` namespaces.  
  
> [!NOTE]
>  The Mscorlib.dll and Microsoft.VisualBasic.dll assemblies are always referenced.  
  
> [!NOTE]
>  The `/nostdlib` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.  
  
## Example  
 The following code compiles `T2.vb` without referencing the standard libraries. You must set the `_MYTYPE` conditional-compilation constant to the string "Empty" to remove the `My` object.  
  
```  
vbc /nostdlib /define:_MYTYPE=\"Empty\" T2.vb  
```  
  
## See Also  
 [/noconfig](../vs140/-noconfig.md)   
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [Customizing Which Objects are Available in My](../vs140/Customizing-Which-Objects-are-Available-in-My--Visual-Basic-.md)