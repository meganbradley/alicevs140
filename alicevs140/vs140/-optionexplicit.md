---
title: "-optionexplicit"
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
H1: /optionexplicit
ms.assetid: 5d296ab3-bafe-4c4d-9887-78f162ed86c7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -optionexplicit
Causes the compiler to report errors if variables are not declared before they are used.  
  
## Syntax  
  
```  
/optionexplicit[+ | -]  
```  
  
## Arguments  
 `+` &#124; `-`  
 Optional. Specify `/optionexplicit+` to require explicit declaration of variables. The `/optionexplicit+` option is the default and is the same as `/optionexplicit`. The `/optionexplicit-` option enables implicit declaration of variables.  
  
## Remarks  
 If the source code file contains an [Option Explicit Statement (Visual Basic)](../vs140/Option-Explicit-Statement--Visual-Basic-.md), the statement overrides the `/optionexplicit` command-line compiler setting.  
  
### To set /optionexplicit in the Visual Studio IDE  
  
1.  Have a project selected in **Solution Explorer**. On the **Project** menu, click **Properties**. For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).  
  
2.  Click the **Compile** tab.  
  
3.  Modify the value in the **Option Explicit** box.  
  
## Example  
 The following code compiles when `/optionexplicit-` is used.  
  
 [!CODE [VbVbalrCompiler#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#5)]  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [/optioncompare](../vs140/-optioncompare.md)   
 [/optionstrict](../vs140/-optionstrict.md)   
 [/optioninfer](../vs140/-optioninfer.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [Option Explicit Statement](../vs140/Option-Explicit-Statement--Visual-Basic-.md)   
 [Visual Basic Defaults, Projects, Options Dialog Box](../vs140/Visual-Basic-Defaults--Projects--Options-Dialog-Box.md)