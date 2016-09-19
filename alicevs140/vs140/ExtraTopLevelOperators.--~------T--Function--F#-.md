---
title: "ExtraTopLevelOperators.( ~%% )&lt;&#39;T&gt; Function (F#)"
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
apiname: 
  - ExtraTopLevelOperators.( ~%% )<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f6d8d802-888a-4ed3-ad7e-8eace7be60ca
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExtraTopLevelOperators.( ~%% )&lt;&#39;T&gt; Function (F#)
Special prefix operator for splicing untyped expressions into quotation holes.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.ExtraTopLevelOperators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( ~%% ) : Expr -> 'T  
  
// Usage:  
%% expression  
```  
  
#### Parameters  
 `expression`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 An expression that is spliced into the quotation hole.  
  
## Return Value  
 The result of the expression.  
  
## Remarks  
 This function is named `SpliceUntypedExpression` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.ExtraTopLevelOperators Module (F#)](../Topic/Core.ExtraTopLevelOperators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)