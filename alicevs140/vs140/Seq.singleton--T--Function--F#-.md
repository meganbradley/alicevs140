---
title: "Seq.singleton&lt;&#39;T&gt; Function (F#)"
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
  - Seq.singleton<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 9b8cc460-a282-4ec5-b29a-630ab17e9de7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.singleton&lt;&#39;T&gt; Function (F#)
Returns a sequence that yields one item only.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Seq  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.singleton : 'T -> seq<'T>  
  
// Usage:  
Seq.singleton value  
```  
  
#### Parameters  
 `value`  
 Type: `'T`  
  
 The input item.  
  
## Return Value  
 The result sequence.  
  
## Remarks  
 This function is named `Singleton` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)