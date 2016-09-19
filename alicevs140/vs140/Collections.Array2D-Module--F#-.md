---
title: "Collections.Array2D Module (F#)"
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
  - Collections.Array2D
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ae1a9746-7817-4430-bcdb-a79c2411bbd3
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.Array2D Module (F#)
Basic operations on 2-dimensional arrays.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Array2D  
```  
  
## Remarks  
 F# and CLI multi-dimensional arrays are typically zero-based. However, CLI multi-dimensional arrays used in conjunction with external libraries (for examples, libraries associated with Visual Basic) be non-zero based, using a potentially different base for each dimension. The operations in this module will accept such arrays, and the basing on an input array will be propagated to a matching output array on the [Array2D.map](../vs140/Array2D.map--T--U--Function--F#-.md) and [Array2D.mapi](../vs140/Array2D.mapi--T--U--Function--F#-.md) operations. Non-zero-based arrays can also be created using [Array2D.zeroCreateBased](../Topic/Array2D.zeroCreateBased%3C'T%3E%20Function%20\(F%23\).md), [Array2D.createBased](../Topic/Array2D.createBased%3C'T%3E%20Function%20\(F%23\).md) and [Array2D.initBased](../vs140/Array2D.initBased--T--Function--F#-.md).  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[base1](../vs140/Array2D.base1--T--Function--F#-.md)  `: 'T [,] -> int`|Fetches the base-index for the first dimension of the array.|  
|[base2](../vs140/Array2D.base2--T--Function--F#-.md)  `: 'T [,] -> int`|Fetches the base-index for the second dimension of the array.|  
|[blit](../vs140/Array2D.blit--T--Function--F#-.md)  `: 'T [,] -> int -> int -> 'T[,] -> int -> int -> int -> int -> unit`|Reads a range of elements from the first array and writes them into the second.|  
|[copy](../vs140/Array2D.copy--T--Function--F#-.md)  `: 'T [,] -> 'T [,]`|Creates a new array whose elements are the same as the input array.|  
|[create](../vs140/Array2D.create--T--Function--F#-.md)  `: int -> int -> 'T -> 'T [,]`|Creates an array whose elements are all initially the given value.|  
|[createBased](../Topic/Array2D.createBased%3C'T%3E%20Function%20\(F%23\).md)  `: int -> int -> int -> int -> 'T -> 'T [,]`|Creates a based array whose elements are all initially the given value.|  
|[get](../Topic/Array2D.get%3C'T%3E%20Function%20\(F%23\).md)  `: 'T [,] -> int -> int -> 'T`|Fetches an element from a 2D array. You can also use the syntax `array.[index1,index2]`.|  
|[init](../Topic/Array2D.init%3C'T%3E%20Function%20\(F%23\).md)  `: int -> int -> (int -> int -> 'T) -> 'T [,]`|Creates an array given the dimensions and a generator function to compute the elements.|  
|[initBased](../vs140/Array2D.initBased--T--Function--F#-.md)  `: int -> int -> int -> int -> (int -> int -> 'T) -> 'T [,]`|Creates a based array given the dimensions and a generator function to compute the elements.|  
|[iter](../vs140/Array2D.iter--T--Function--F#-.md)  `: ('T -> unit) -> 'T [,] -> unit`|Applies the given function to each element of the array.|  
|[iteri](../vs140/Array2D.iteri--T--Function--F#-.md) `: int -> int -> 'T -> unit`|Applies the given function to each element of the array. The integer indices passed to the function indicate the index of element.|  
|[length1](../vs140/Array2D.length1--T--Function--F#-.md)  `: 'T [,] -> int`|Returns the length of an array in the first dimension.|  
|[length2](../vs140/Array2D.length2--T--Function--F#-.md)  `: 'T [,] -> int`|Returns the length of an array in the second dimension.|  
|[map](../vs140/Array2D.map--T--U--Function--F#-.md)  `: ('T -> 'U) -> 'T [,] -> 'U [,]`|Creates a new array whose elements are the results of applying the given function to each of the elements of the array.|  
|[mapi](../vs140/Array2D.mapi--T--U--Function--F#-.md)  `: (int -> int -> 'T -> 'U) -> 'T [,] -> 'U [,]`|Creates a new array whose elements are the results of applying the given function to each of the elements of the array. The integer indices passed to the function indicate the element being transformed.|  
|[rebase](../vs140/Array2D.rebase--T--Function--F#-.md)  `: 'T [,] -> 'T [,]`|Creates a new array whose elements are the same as the input array but where a non-zero-based input array generates a corresponding zero-based output array.|  
|[set](../vs140/Array2D.set--T--Function--F#-.md)  `: 'T [,] -> int -> int -> 'T -> unit`|Sets the value of an element in an array. You can also use the syntax `array.[index1,index2] <- value`.|  
|[zeroCreate](../Topic/Array2D.zeroCreate%3C'T%3E%20Function%20\(F%23\).md)  `: int -> int -> 'T [,]`|Creates an array where the entries are initially [Unchecked.defaultof<'T>](../vs140/Unchecked.defaultof--T--Type-Function--F#-.md).|  
|[zeroCreateBased](../Topic/Array2D.zeroCreateBased%3C'T%3E%20Function%20\(F%23\).md)  `: int -> int -> int -> int -> 'T [,]`|Creates a based array where the entries are initially [Unchecked.defaultof<'T>](../vs140/Unchecked.defaultof--T--Type-Function--F#-.md).|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)