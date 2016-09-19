---
title: "Patterns.PropertyGet Active Pattern (F#)"
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
  - Patterns.( |PropertyGet|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ee094de8-82ad-48fb-9576-f9ad7d43fd36
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.PropertyGet Active Pattern (F#)
Recognizes expressions that represent the reading of a static or instance property, or of a non-function value declared in a module.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |PropertyGet|_| ) : (input:Expr) -> (Expr option * PropertyInfo * Expr list) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Expr option * PropertyInfo * Expr list) option`. The option indicates whether the input results in a match. In a pattern matching expression, the input is decomposed, upon a successful match, into a tuple that has three elements. The first element is an optional expression that represents the instance. For a static property, this option is `None`. The second element is a <xref:System.Reflection.PropertyInfo?qualifyHint=False> object that represents the property. The third element is a list that contains the arguments of the `get` accessor, which is used for indexed properties.  
  
## Remarks  
 This function is named `PropertyGetPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)