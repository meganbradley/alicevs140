---
title: "Collections.Set Module (F#)"
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
  - Collections.Set
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 61efa732-d55d-4c32-993f-628e2f98e6a0
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.Set Module (F#)
Functional programming operators related to the [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md) type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Set  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[add](../vs140/Set.add--T--Function--F#-.md)  `: 'T -> Set<'T> -> Set<'T>`|Returns a new set with an element added to the set. No exception is raised if the set already contains the given element.|  
|[contains](../vs140/Set.contains--T--Function--F#-.md)  `: 'T -> Set<'T> -> bool`|Evaluates to `true` if the given element is in the given set.|  
|[count](../vs140/Set.count--T--Function--F#-.md)  `: Set<'T> -> int`|Returns the number of elements in the set.|  
|[difference](../vs140/Set.difference--T--Function--F#-.md)  `: Set<'T> -> Set<'T> -> Set<'T>`|Returns a new set with the elements of the second set removed from the first.|  
|[empty](../vs140/Set.empty--T--Type-Function--F#-.md)  `: Set<'T>`|The empty set for the specified type.|  
|[exists](../vs140/Set.exists--T--Function--F#-.md)  `: ('T -> bool) -> Set<'T> -> bool`|Tests if any element of the collection satisfies the given predicate. If the input function is `predicate` and the elements are `i0...iN`, then this function computes `predicate i0 or ... or predicate iN`.|  
|[filter](../vs140/Set.filter--T--Function--F#-.md)  `: ('T -> bool) -> Set<'T> -> Set<'T>`|Returns a new collection containing only the elements of the collection for which the given predicate returns `true`.|  
|[fold](../vs140/Set.fold--T--State--Function--F#-.md)  `: ('State -> 'T -> 'State) -> 'State -> Set<'T> -> 'State`|Applies the given accumulating function to all the elements of the set|  
|[foldBack](../vs140/Set.foldBack--T--State--Function--F#-.md)  `: ('T -> 'State -> 'State) -> Set<'T> -> 'State -> 'State`|Applies the given accumulating function to all the elements of the set.|  
|[forall](../vs140/Set.forall--T--Function--F#-.md)  `: ('T -> bool) -> Set<'T> -> bool`|Tests if all elements of the collection satisfy the given predicate. If the input function is `p` and the elements are `i0...iN,` then this function computes `p i0 && ... && p iN`.|  
|[intersect](../vs140/Set.intersect--T--Function--F#-.md)  `: Set<'T> -> Set<'T> -> Set<'T>`|Computes the intersection of the two sets.|  
|[intersectMany](../vs140/Set.intersectMany--T--Function--F#-.md)  `: seq<Set<'T>> -> Set<'T>`|Computes the intersection of a sequence of sets. The sequence must be non-empty.|  
|[isEmpty](../vs140/Set.isEmpty--T--Function--F#-.md)  `: Set<'T> -> bool`|Returns `true` if the set is empty.|  
|[isProperSubset](../vs140/Set.isProperSubset--T--Function--F#-.md)  `: Set<'T> -> Set<'T> -> bool`|Evaluates to `true` if all elements of the first set are in the second, and at least one element of the second is not in the first.|  
|[isProperSuperset](../vs140/Set.isProperSuperset--T--Function--F#-.md)  `: Set<'T> -> Set<'T> -> bool`|Evaluates to `true` if all elements of the second set are in the first, and at least one element of the first is not in the second.|  
|[isSubset](../vs140/Set.isSubset--T--Function--F#-.md)  `: Set<'T> -> Set<'T> -> bool`|Evaluates to `true` if all elements of the first set are in the second|  
|[isSuperset](../vs140/Set.isSuperset--T--Function--F#-.md)  `: Set<'T> -> Set<'T> -> bool`|Evaluates to `true` if all elements of the second set are in the first.|  
|[iter](../vs140/Set.iter--T--Function--F#-.md)  `: ('T -> unit) -> Set<'T> -> unit`|Applies the given function to each element of the set, in order according to the comparison function.|  
|[map](../vs140/Set.map--T--U--Function--F#-.md)  `: ('T -> 'U) -> Set<'T> -> Set<'U>`|Returns a new collection containing the results of applying the given function to each element of the input set.|  
|[maxElement](../vs140/Set.maxElement--T--Function--F#-.md)  `: Set<'T> -> 'T`|Returns the highest element in the set according to the ordering being used for the set.|  
|[minElement](../vs140/Set.minElement--T--Function--F#-.md)  `: Set<'T> -> 'T`|Returns the lowest element in the set according to the ordering being used for the set.|  
|[ofArray](../vs140/Set.ofArray--T--Function--F#-.md)  `: 'T array -> Set<'T>`|Creates a set that contains the same elements as the given array.|  
|[ofList](../vs140/Set.ofList--T--Function--F#-.md)  `: 'T list -> Set<'T>`|Creates a set that contains the same elements as the given list.|  
|[ofSeq](../vs140/Set.ofSeq--T--Function--F#-.md)  `: seq<'T> -> Set<'T>`|Creates a new collection from the given enumerable object.|  
|[partition](../vs140/Set.partition--T--Function--F#-.md)  `: ('T -> bool) -> Set<'T> -> Set<'T> * Set<'T>`|Splits the set into two sets containing the elements for which the given predicate returns true and false respectively.|  
|[remove](../vs140/Set.remove--T--Function--F#-.md)  `: 'T -> Set<'T> -> Set<'T>`|Returns a new set with the given element removed. No exception is raised if the set doesn't contain the given element.|  
|[singleton](../vs140/Set.singleton--T--Function--F#-.md)  `: 'T -> Set<'T>`|The set containing the given element.|  
|[toArray](../vs140/Set.toArray--T--Function--F#-.md)  `: Set<'T> -> 'T array`|Creates an array that contains the elements of the set in order.|  
|[toList](../vs140/Set.toList--T--Function--F#-.md) `: Set<'T> -> 'T list`|Creates a list that contains the elements of the set in order.|  
|[toSeq](../vs140/Set.toSeq--T--Function--F#-.md)  `: Set<'T> -> seq<'T>`|Returns an ordered view of the collection as an enumerable object.|  
|[union](../vs140/Set.union--T--Function--F#-.md)  `: Set<'T> -> Set<'T> -> Set<'T>`|Computes the union of the two sets.|  
|[unionMany](../vs140/Set.unionMany--T--Function--F#-.md)  `: seq<Set<'T>> -> Set<'T>`|Computes the union of a sequence of sets.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)