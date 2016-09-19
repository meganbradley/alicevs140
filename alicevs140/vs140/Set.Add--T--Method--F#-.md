---
title: "Set.Add&lt;&#39;T&gt; Method (F#)"
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
  - Set.Add<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 81a5d225-7c60-4243-9b4e-7162cb0e001b
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.Add&lt;&#39;T&gt; Method (F#)
A useful shortcut for [Set.add](../vs140/Set.add--T--Function--F#-.md). Note this operation produces a new set and does not mutate the original set. The new set will share many storage nodes with the original. See the [Set module](../vs140/Collections.Set-Module--F#-.md) for further operations on sets.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Add : 'T -> Set<'T> (requires comparison)  
  
// Usage:  
set.Add (value)  
```  
  
#### Parameters  
 `value`  
 Type: `'T`  
  
 The value to add to the set.  
  
## Return Value  
 The result set.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set<'T> Class (F#)](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)