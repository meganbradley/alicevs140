---
title: "LeafExpressionConverter.QuotationToExpression Function (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 6a71ff35-492b-4047-b31e-fb2e3fc0e7ae
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LeafExpressionConverter.QuotationToExpression Function (F#)
Converts a subset of F# quotations to a LINQ expression, for the subset of LINQ expressions represented by the expression syntax in the C# language.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.RuntimeHelpers.LeafExpressionConverter  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
QuotationToExpression : Expr -> Expression  
  
// Usage:  
QuotationToExpression   
```  
  
#### Parameters  
 `quotation`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 A quotation to convert to a LINQ expression.  
  
## Return Value  
 The converted expression.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [RuntimeHelpers.LeafExpressionConverter Module (F#)](../Topic/RuntimeHelpers.LeafExpressionConverter%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Linq.RuntimeHelpers Namespace (F#)](../vs140/Microsoft.FSharp.Linq.RuntimeHelpers-Namespace--F#-.md)