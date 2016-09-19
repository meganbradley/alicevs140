---
title: "-optionstrict"
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
H1: /optionstrict
ms.assetid: c7b10086-0fa4-49db-b3c8-4ae0db5957da
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -optionstrict
Enforces strict type semantics to restrict implicit type conversions.  
  
## Syntax  
  
```  
/optionstrict[+ | -]  
/optionstrict[:custom]  
```  
  
## Arguments  
 `+` &#124; `-`  
 Optional. The `/optionstrict+` option restricts implicit type conversion. The default for this option is `/optionstrict-`. The `/optionstrict+` option is the same as `/optionstrict`. You can use both for permissive type semantics.  
  
 `custom`  
 Required. Warn when strict language semantics are not respected.  
  
## Remarks  
 When `/optionstrict+` is in effect, only widening type conversions can be made implicitly. Implicit narrowing type conversions, such as assigning a `Decimal` type object to an integer type object, are reported as errors.  
  
 To generate warnings for implicit narrowing type conversions, use `/optionstrict:custom`. Use `/nowarn:numberlist` to ignore particular warnings and `/warnaserror:numberlist` to treat particular warnings as errors.  
  
### To set /optionstrict in the Visual Studio IDE  
  
1.  Have a project selected in **Solution Explorer**. On the **Project** menu, click **Properties.** For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).  
  
2.  Click the **Compile** tab.  
  
3.  Modify the value in the **Option Strict** box.  
  
### To set /optionstrict programmatically  
  
-   See [Option Strict Statement](../vs140/Option-Strict-Statement.md).  
  
## Example  
 The following code compiles `Test.vb` using strict type semantics.  
  
```  
vbc /optionstrict+ test.vb  
```  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [/optioncompare](../vs140/-optioncompare.md)   
 [/optionexplicit](../vs140/-optionexplicit.md)   
 [/optioninfer](../vs140/-optioninfer.md)   
 [/nowarn](../vs140/-nowarn.md)   
 [/warnaserror (Visual Basic)](../vs140/-warnaserror--Visual-Basic-.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [Visual Basic Defaults, Projects, Options Dialog Box](../vs140/Visual-Basic-Defaults--Projects--Options-Dialog-Box.md)