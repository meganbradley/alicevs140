---
title: "Collections.Array3D Module (F#)"
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
  - Collections.Array3D
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c8355e2d-add8-48a4-8aa6-1c57ae74c560
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.Array3D Module (F#)
Basic operations on rank 3 arrays.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Array3D  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[create](../vs140/Array3D.create--T--Function--F#-.md)  `: int -> int -> int -> int -> 'T -> 'T [,,]`|Creates an array whose elements are all initially the given value.|  
|[get](../vs140/Array3D.get--T--Function--F#-.md)  `: 'T [,,] -> int -> int -> int -> 'T`|Fetches an element from a 3D array. You can also use the syntax `array.[index1,index2,index3]`.|  
|[init](../vs140/Array3D.init--T--Function--F#-.md)  `: int -> int -> int -> (int -> int -> int -> 'T) -> 'T [,,]`|Creates an array given the dimensions and a generator function to compute the elements.|  
|[iter](../vs140/Array3D.iter--T--Function--F#-.md)  `: ('T -> unit) -> 'T [,,] -> unit`|Applies the given function to each element of the array.|  
|[iteri](../vs140/Array3D.iteri--T--Function--F#-.md)  `: (int -> int -> int -> 'T -> unit) -> 'T [,,] -> unit`|Applies the given function to each element of the array. The integer indices passed to the function indicate the index of element.|  
|[length1](../vs140/Array3D.length1--T--Function--F#-.md)  `: 'T [,,] -> int`|Returns the length of an array in the first dimension|  
|[length2](../vs140/Array3D.length2--T--Function--F#-.md)  `: 'T [,,] -> int`|Returns the length of an array in the second dimension.|  
|[length3](../vs140/Array3D.length3--T--Function--F#-.md)  `: 'T [,,] -> int`|Returns the length of an array in the third dimension.|  
|[map](../vs140/Array3D.map--T--U--Function--F#-.md)  `: ('T -> 'U) -> 'T [,,] -> 'U [,,]`|Builds a new array whose elements are the results of applying the given function to each of the elements of the array.|  
|[mapi](../vs140/Array3D.mapi--T--U--Function--F#-.md)  `: (int -> int -> int -> 'T -> 'U) -> 'T [,,] -> 'U [,,]`|Builds a new array whose elements are the results of applying the given function to each of the elements of the array. The integer indices passed to the function indicate the element being transformed.|  
|[set](../vs140/Array3D.set--T--Function--F#-.md)  `: 'T [,,] -> int -> int -> int -> 'T -> unit`|Sets the value of an element in an array. You can also use the syntax `array.[index1,index2,index3] <- value`.|  
|[zeroCreate](../vs140/Array3D.zeroCreate--T--Function--F#-.md)  `: int -> int -> int -> 'T [,,]`|Creates an array where the entries are initially the default value.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)