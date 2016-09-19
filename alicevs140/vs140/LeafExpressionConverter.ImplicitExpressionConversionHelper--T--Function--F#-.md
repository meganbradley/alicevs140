---
title: "LeafExpressionConverter.ImplicitExpressionConversionHelper&lt;&#39;T&gt; Function (F#)"
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
ms.assetid: 5f36b846-ac35-45a4-b845-5a058af226eb
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LeafExpressionConverter.ImplicitExpressionConversionHelper&lt;&#39;T&gt; Function (F#)
When used in a quotation, this function indicates that a specific conversion should be performed when converting the quotation to a LINQ expression. This function should not be called directly.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.RuntimeHelpers.LeafExpressionConverter  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
ImplicitExpressionConversionHelper : 'T -> Expression<'T>  
  
// Usage:  
ImplicitExpressionConversionHelper   
```  
  
#### Parameters  
 `input`  
 Type: 'T  
  
 The input value.  
  
## Return Value  
 The resulting LINQ expression.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [RuntimeHelpers.LeafExpressionConverter Module (F#)](../Topic/RuntimeHelpers.LeafExpressionConverter%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Linq.RuntimeHelpers Namespace (F#)](../vs140/Microsoft.FSharp.Linq.RuntimeHelpers-Namespace--F#-.md)