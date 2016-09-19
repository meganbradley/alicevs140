---
title: "Option Explicit Statement (Visual Basic)"
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
ms.assetid: e82ac1ad-2cd3-49b2-b985-8bcf016f3fcc
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Explicit Statement (Visual Basic)
Forces explicit declaration of all variables in a file, or allows implicit declarations of variables.  
  
## Syntax  
  
```  
Option Explicit { On | Off }  
```  
  
## Parts  
 `On`  
 Optional. Enables `Option Explicit` checking. If `On` or `Off` is not specified, the default is `On`.  
  
 `Off`  
 Optional. Disables `Option Explicit` checking.  
  
## Remarks  
 When `Option Explicit On` or `Option Explicit` appears in a file, you must explicitly declare all variables by using the `Dim` or `ReDim` statements. If you try to use an undeclared variable name, an error occurs at compile time. The `Option Explicit Off` statement allows implicit declaration of variables.  
  
 If used, the `Option Explicit` statement must appear in a file before any other source code statements.  
  
> [!NOTE]
>  Setting `Option Explicit` to `Off` is generally not a good practice. You could misspell a variable name in one or more locations, which would cause unexpected results when the program is run.  
  
## When an Option Explicit Statement Is Not Present  
 If the source code does not contain an `Option Explicit` statement, the **Option Explicit** setting on the [Compile Page, Project Designer (Visual Basic)](../vs140/Compile-Page--Project-Designer--Visual-Basic-.md) is used. If the command-line compiler is used, the [/optionexplicit](../vs140/-optionexplicit.md) compiler option is used.  
  
#### To set Option Explicit in the IDE  
  
1.  In **Solution Explorer**, select a project. On the **Project** menu, click **Properties**. For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).  
  
2.  Click the **Compile** tab.  
  
3.  Set the value in the **Option Explicit** box.  
  
 When you create a new project, the **Option Explicit** setting on the **Compile** tab is set to the **Option Explicit** setting in the **VB Defaults** dialog box. To access the **VB Defaults** dialog box, on the **Tools** menu, click **Options**. In the **Options** dialog box, expand **Projects and Solutions**, and then click **VB Defaults**. The initial default setting in **VB Defaults** is `On`.  
  
#### To set Option Explicit on the command line  
  
-   Include the [/optionexplicit](../vs140/-optionexplicit.md) compiler option in the **vbc** command.  
  
## Example  
 The following example uses the `Option Explicit` statement to force explicit declaration of all variables. Attempting to use an undeclared variable causes an error at compile time.  
  
 [!CODE [VbVbalrStatements#47](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#47)]  
  
 [!CODE [VbVbalrStatements#48](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#48)]  
  
## See Also  
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [ReDim Statement](../vs140/ReDim-Statement--Visual-Basic-.md)   
 [Option Compare Statement](../Topic/Option%20Compare%20Statement.md)   
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [/optioncompare](../vs140/-optioncompare.md)   
 [/optionexplicit](../vs140/-optionexplicit.md)   
 [/optionstrict](../vs140/-optionstrict.md)   
 [Visual Basic Defaults, Projects, Options Dialog Box](../vs140/Visual-Basic-Defaults--Projects--Options-Dialog-Box.md)