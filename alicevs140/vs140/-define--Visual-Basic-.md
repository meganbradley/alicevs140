---
title: "-define (Visual Basic)"
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
H1: /define (Visual Basic)
ms.assetid: f735c57d-1cf9-4f2f-a26f-0de630fd4077
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -define (Visual Basic)
Defines conditional compiler constants.  
  
## Syntax  
  
```  
/define:["]symbol[=value][,symbol[=value]]["]  
' -or-  
/d:["]symbol[=value][,symbol[=value]]["]  
```  
  
## Arguments  
  
|||  
|-|-|  
|Term|Definition|  
|`symbol`|Required. The symbol to define.|  
|`value`|Optional. The value to assign `symbol`. If `value` is a string, it must be surrounded by backslash/quotation-mark sequences (\\") instead of quotation marks. If no value is specified, then it is taken to be True.|  
  
## Remarks  
 The `/define` option has an effect  similar to using a `#Const` preprocessor directive in your source file, except that constants defined with `/define` are public and apply to all files in the project.  
  
 You can use symbols created by this option with the `#If`...`Then`...`#Else` directive to compile source files conditionally.  
  
 `/d` is the short form of `/define`.  
  
 You can define multiple symbols with `/define` by using a comma to separate symbol definitions.  
  
||  
|-|  
|To set /define in the Visual Studio integrated development environment|  
|1.  Have a project selected in **Solution Explorer**. On the **Project** menu, click **Properties**. For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).<br />2.  Click the **Compile** tab.<br />3.  Click **Advanced**.<br />4.  Modify the value in the **Custom Constants** box.|  
  
## Example  
 The following code defines and then uses two conditional compiler constants.  
  
 [!CODE [VbVbalrCompiler#45](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#45)]  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [#If...Then...#Else Directives](../vs140/#If...Then...#Else-Directives.md)   
 [#Const Directive](../vs140/#Const-Directive.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)