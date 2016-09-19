---
title: "-optioninfer"
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
H1: /optioninfer
ms.assetid: f6c09db1-0553-464a-abe3-d4510c61d6ed
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -optioninfer
Enables the use of local type inference in variable declarations.  
  
## Syntax  
  
```  
/optioninfer[+ | -]  
```  
  
## Arguments  
  
|||  
|-|-|  
|Term|Definition|  
|`+` &#124; `-`|Optional. Specify `/optioninfer+` to enable local type inference, or `/optioninfer-` to block it. The `/optioninfer` option, with no value specified, is the same as `/optioninfer+`. The default value when the `/optioninfer` switch is not present is also `/optioninfer+`. The default value is set in the Vbc.rsp response file.|  
  
> [!NOTE]
>  You can use the `/noconfig` option to retain the compiler's internal defaults instead of those specified in vbc.rsp. The compiler default for this option is `/optioninfer-`.  
  
## Remarks  
 If the source code file contains an [Option Infer Statement](../vs140/Option-Infer-Statement.md), the statement overrides the `/optioninfer` command-line compiler setting.  
  
### To set /optioninfer in the Visual Studio IDE  
  
1.  Select a project in **Solution Explorer**. On the **Project** menu, click **Properties**. For more information, see [NIB: Managing Project Properties with the Project Designer](assetId:///983f3c18-832f-4666-afec-74b716ff3e0e).  
  
2.  On the **Compile** tab, modify the value in the **Option infer** box.  
  
## Example  
 The following code compiles `test.vb` with local type inference enabled.  
  
```  
vbc /optioninfer+ test.vb  
```  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [/optioncompare](../vs140/-optioncompare.md)   
 [/optionexplicit](../vs140/-optionexplicit.md)   
 [/optionstrict](../vs140/-optionstrict.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [Option Infer Statement](../vs140/Option-Infer-Statement.md)   
 [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md)   
 [Visual Basic Defaults, Projects, Options Dialog Box](../vs140/Visual-Basic-Defaults--Projects--Options-Dialog-Box.md)   
 [Compile Page, Project Designer (Visual Basic)](../vs140/Compile-Page--Project-Designer--Visual-Basic-.md)   
 [/noconfig](../vs140/-noconfig.md)   
 [Building from the Command Line (Visual Basic)](../vs140/Building-from-the-Command-Line--Visual-Basic-.md)