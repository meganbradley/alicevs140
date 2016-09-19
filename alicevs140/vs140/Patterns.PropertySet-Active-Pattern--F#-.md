---
title: "Patterns.PropertySet Active Pattern (F#)"
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
  - Patterns.( |PropertySet|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 9a674e05-e14f-42dd-a645-91f5221fd872
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.PropertySet Active Pattern (F#)
Recognizes expressions that represent setting a static or instance property, or setting a non-function value declared in a module.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |PropertySet|_| ) : (input:Expr) -> (Expr option * PropertyInfo * Expr list * Expr) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return value is `(Expr option * PropertyInfo * Expr list * Expr) option`. The option type indicates whether the input results in a match. In a pattern matching expression, the input is decomposed, upon a successful match, into a tuple of four elements. The first element is an option whose value is an expression that represents the instance, or `None` if the property is static. The second element is a <xref:System.Reflection.PropertyInfo?qualifyHint=False> object that represents the property (or the module value). The third element is an expression list that represents the arguments to the `set` accessor, which is used for indexed properties. The fourth element is an expression that represents the value to set, which is also the right side of the assignment.  
  
## Remarks  
 This function is named `PropertySetPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)