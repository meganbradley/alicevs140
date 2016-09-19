---
title: "Collections.Array4D Module (F#)"
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
  - Collections.Array4D
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 9fdbd023-7c17-4a68-a405-8a1b826ac032
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.Array4D Module (F#)
Basic operations on rank 4 arrays.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Array4D  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[create](../vs140/Array4D.create--T--Function--F#-.md)  `: int -> int -> int -> int -> 'T -> 'T [,,,]`|Creates an array whose elements are all initially the given value|  
|[get](../vs140/Array4D.get--T--Function--F#-.md)  `: 'T [,,,] -> int -> int -> int -> int -> 'T`|Fetches an element from a 4D array.|  
|[init](../vs140/Array4D.init--T--Function--F#-.md)  `: int -> int -> int -> int -> (int -> int -> int -> int -> 'T) -> 'T [,,,]`|Creates an array given the dimensions and a generator function to compute the elements.|  
|[length1](../vs140/Array4D.length1--T--Function--F#-.md)  `: 'T [,,,] -> int`|Returns the length of an array in the first dimension|  
|[length2](../vs140/Array4D.length2--T--Function--F#-.md)  `: 'T [,,,] -> int`|Returns the length of an array in the second dimension.|  
|[length3](../vs140/Array4D.length3--T--Function--F#-.md)  `: 'T [,,,] -> int`|Returns the length of an array in the third dimension.|  
|[length4](../vs140/Array4D.length4--T--Function--F#-.md)  `: 'T [,,,] -> int`|Returns the length of an array in the fourth dimension.|  
|[set](../vs140/Array4D.set--T--Function--F#-.md)  `: 'T [,,,] -> int -> int -> int -> int -> 'T -> unit`|Sets the value of an element in an array.|  
|[zeroCreate](../vs140/Array4D.zeroCreate--T--Function--F#-.md)  `: int -> int -> int -> int -> 'T [,,,]`|Creates an array where the entries are initially the default value.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)