---
title: "Operators.lock&lt;&#39;Lock,&#39;T&gt; Function (F#)"
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
  - Operators.lock<'Lock,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: cf1fe60b-0fa1-485e-b81d-af4859c4558d
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.lock&lt;&#39;Lock,&#39;T&gt; Function (F#)
Execute the function as a mutual-exclusion region using the input value as a lock.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
lock : 'Lock -> (unit -> 'T) -> 'T (requires reference type)  
  
// Usage:  
lock lockObject action  
```  
  
#### Parameters  
 `lockObject`  
 Type: `'Lock`  
  
 The object to be locked.  
  
 `action`  
 Type: [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md) `-> 'T`  
  
 The action to perform during the lock.  
  
## Return Value  
 The resulting value.  
  
## Remarks  
 This function is named `Lock` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)