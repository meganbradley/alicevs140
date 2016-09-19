---
title: "Collections.List&lt;&#39;T&gt; Union (F#)"
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
  - Collections.List<'T> Union (F#)
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c627b668-477b-4409-91ed-06d7f1b3e4a7
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.List&lt;&#39;T&gt; Union (F#)
The type of immutable singly-linked lists.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<DefaultAugmentation(false)>]  
[<StructuralEquality>]  
[<StructuralComparison>]  
type List<'T> =  
| ( [] )  
| ( :: ) of 'T * 'T list  
 with  
  interface IStructuralEquatable  
  interface IComparable  
  interface IComparable  
  interface IStructuralComparable  
  interface IEnumerable  
  interface IEnumerable  
  static member List.Cons : 'T * 'T list -> 'T list  
  static member List.Empty :  'T list  
  member this.Head :  'T  
  member this.IsEmpty :  bool  
  member this.Item (int) :  'T  
  member this.Length :  int  
  member this.Tail :  'T list  
 end  
```  
  
## Remarks  
 Use the constructors `[]` and `::` (infix) to create values of this type, or the notation `[1;2;3]`. Use the values in the `List` module to manipulate values of this type, or pattern match against the values directly.  
  
 This type is named `FSharpList` in the .NET assembly. If accessing the type from a .NET language other than F#, or through reflection, use this name.  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Head](../vs140/List.Head--T--Property--F#-.md)|Gets the first element of the list.|  
|[IsEmpty](../vs140/List.IsEmpty--T--Property--F#-.md)|Gets a value indicating if the list contains no entries.|  
|[Item](../vs140/List.Item--T--Property--F#-.md)|Gets the element of the list at the given position.|  
|[Length](../vs140/List.Length--T--Property--F#-.md)|Gets the number of items contained in the list.|  
|[Tail](../vs140/List.Tail--T--Property--F#-.md)|Gets the tail of the list, which is a list containing all the elements of the list, excluding the first element.|  
  
## Static Members  
  
|Member|Description|  
|------------|-----------------|  
|[Cons](../vs140/List.Cons--T--Method--F#-.md)|Returns a list with the first argument as its first element and the second argument as its subsequent elements.|  
|[Empty](../vs140/Empty--T--Property--F#-.md)|Returns an empty list of a particular type.|  
  
## Union Cases  
  
|Case|Description|  
|----------|-----------------|  
|( :: ) of 'T * 'T list|The cons operator.|  
|( [] )|The empty list.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)   
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)