---
title: "AddressOf Operator (Visual Basic)"
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
ms.assetid: 8105a59d-60d8-4ab5-b221-5899cdfacbf4
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AddressOf Operator (Visual Basic)
Creates a procedure delegate instance that references the specific procedure.  
  
## Syntax  
  
```  
  
AddressOf procedurename  
```  
  
## Parts  
 `procedurename`  
 Required. Specifies the procedure to be referenced by the newly created procedure delegate.  
  
## Remarks  
 The `AddressOf` operator creates a function delegate that points to the function specified by `procedurename`. When the specified procedure is an instance method then the function delegate refers to both the instance and the method. Then, when the function delegate is invoked the specified method of the specified instance is called.  
  
 The `AddressOf` operator can be used as the operand of a delegate constructor or it can be used in a context in which the type of the delegate can be determined by the compiler.  
  
## Example  
 This example uses the `AddressOf` operator to designate a delegate to handle the `Click` event of a button.  
  
 [!CODE [VbVbalrDelegates#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#8)]  
  
## Example  
 The following example uses the `AddressOf` operator to designate the startup function for a thread.  
  
 [!CODE [VbVbalrDelegates#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#9)]  
  
## See Also  
 [Declare Statement](../Topic/Declare%20Statement.md)   
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)   
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)   
 [Delegates (Visual Basic)](../Topic/Delegates%20\(Visual%20Basic\).md)