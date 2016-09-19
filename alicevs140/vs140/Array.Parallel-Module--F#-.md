---
title: "Array.Parallel Module (F#)"
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
ms.assetid: 60f30b77-5af4-4050-9a5c-bcdb3f5cbb09
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.Parallel Module (F#)
Provides parallel operations on arrays  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Array  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Parallel  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[choose](../vs140/Parallel.choose--T--U--Function--F#-.md)  `: ('T -> 'U option) -> 'T [] -> 'U []`|Apply the given function to each element of the array. Return the array comprised of the results "x" for each element where the function returns Some(x).|  
|[collect](../vs140/Parallel.collect--T--U--Function--F#-.md)  `: ('T -> 'U []) -> 'T [] -> 'U []`|For each element of the array, apply the given function. Concatenate all the results and return the combined array.|  
|[init](../vs140/Parallel.init--T--Function--F#-.md)  `: int -> (int -> 'T) -> 'T []`|Create an array given the dimension and a generator function to compute the elements.|  
|[iter](../vs140/Parallel.iter--T--Function--F#-.md)  `: ('T -> unit) -> 'T [] -> unit`|Apply the given function to each element of the array.|  
|[iteri](../vs140/Parallel.iteri--T--Function--F#-.md)  `: (int -> 'T -> unit) -> 'T [] -> unit`|Apply the given function to each element of the array. The integer passed to the function indicates the index of element.|  
|[map](../vs140/Parallel.map--T--U--Function--F#-.md)  `: ('T -> 'U) -> 'T [] -> 'U []`|Build a new array whose elements are the results of applying the given function to each of the elements of the array.|  
|[mapi](../vs140/Parallel.mapi--T--U--Function--F#-.md)  `: (int -> 'T -> 'U) -> 'T [] -> 'U []`|Build a new array whose elements are the results of applying the given function to each of the elements of the array. The integer index passed to the function indicates the index of element being transformed.|  
|[partition](../vs140/Parallel.partition--T--Function--F#-.md)  `: ('T -> bool) -> 'T [] -> 'T [] * 'T []`|Split the collection into two collections, containing the elements for which the given predicate returns "true" and "false" respectively|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)