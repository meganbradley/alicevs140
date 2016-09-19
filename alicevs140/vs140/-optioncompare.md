---
title: "-optioncompare"
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
H1: /optioncompare
ms.assetid: 7237b766-b44d-4cc5-9a3c-885348a7d9e4
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -optioncompare
Specifies how string comparisons are made.  
  
## Syntax  
  
```  
/optioncompare:{binary | text}  
```  
  
## Remarks  
 You can specify `/optioncompare` in one of two forms: `/optioncompare:binary` to use binary string comparisons, and `/optioncompare:text` to use text string comparisons. By default, the compiler uses `/optioncompare:binary`.  
  
 In Microsoft Windows, the code page being used determines the binary sort order. A typical binary sort order is as follows:  
  
 `A < B < E < Z < a < b < e < z < À < Ê < Ø < à < ê < ø`  
  
 Text-based string comparisons are based on a case-insensitive text sort order determined by your system's locale. A typical text sort order is as follows:  
  
 `(A = a) < (À = à) < (B=b) < (E=e) < (Ê = ê) < (Z=z) < (Ø = ø)`  
  
### To set /optioncompare in the Visual Studio IDE  
  
1.  Have a project selected in **Solution Explorer**. On the **Project** menu, click **Properties**. For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).  
  
2.  Click the **Compile** tab.  
  
3.  Modify the value in the **Option Compare** box.  
  
### To set /optioncompare programmatically  
  
-   See [Option Compare Statement](../Topic/Option%20Compare%20Statement.md).  
  
## Example  
 The following code compiles P`rojFile.vb` and uses binary string comparisons.  
  
```  
vbc /optioncompare:binary projFile.vb  
```  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [/optionexplicit](../vs140/-optionexplicit.md)   
 [/optionstrict](../vs140/-optionstrict.md)   
 [/optioninfer](../vs140/-optioninfer.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [Option Compare Statement](../Topic/Option%20Compare%20Statement.md)   
 [Visual Basic Defaults, Projects, Options Dialog Box](../vs140/Visual-Basic-Defaults--Projects--Options-Dialog-Box.md)