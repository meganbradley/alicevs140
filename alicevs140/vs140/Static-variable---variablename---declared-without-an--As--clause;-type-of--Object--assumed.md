---
title: "Static variable &#39;&lt;variablename&gt;&#39; declared without an &#39;As&#39; clause; type of &#39;Object&#39; assumed"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ca6b625c-21a5-45f7-ac67-282f6993a724
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Static variable &#39;&lt;variablename&gt;&#39; declared without an &#39;As&#39; clause; type of &#39;Object&#39; assumed
The compiler does not infer the data type of static local variables. In the following example, with `Option Strict` set to `Off`, the type of `m` will be `Object`, regardless of whether `Option Infer` is set to `On` or `Off`. Local type inference does not apply.  
  
```  
Sub Main()  
    Static m = 10  
End Sub  
```  
  
 By default, this message is a warning. For information about how to hide warnings or how to treat warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42111  
  
### To address this warning  
  
-   Specify the data type for static local variables.  
  
     For example, if you want `m` in the previous example to be of type `Integer`, specify the type in the declaration.  
  
    ```  
    Sub Main()  
        Static m As Integer = 10  
    End Sub  
  
    ```  
  
## See Also  
 [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [NOTINBUILD How to: Lengthen a Variable's Lifetime](assetId:///04e7c56c-1db0-4fe5-a678-859a39ec654b)   
 [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md)   
 [Option Infer Statement](../vs140/Option-Infer-Statement.md)   
 [Static (Visual Basic)](../vs140/Static--Visual-Basic-.md)