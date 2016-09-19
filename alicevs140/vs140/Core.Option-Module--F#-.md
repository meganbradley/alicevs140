---
title: "Core.Option Module (F#)"
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
  - Core.Option
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e615e4d3-bbbb-49ba-addc-6061ea2e2f4c
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.Option Module (F#)
Basic operations on options.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Option  
```  
  
## Remarks  
 For an overview of options in F#, see [Options (F#)](../Topic/Options%20\(F%23\).md).  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[bind](../vs140/Option.bind--T--U--Function--F#-.md)  `: ('T -> 'U option) -> 'T option -> 'U option`|Invokes a function on an optional value that itself yields an option.|  
|[count](../vs140/Option.count--T--Function--F#-.md)  `: 'T option -> int`|Evaluates the equivalent of [Set.count](../vs140/Set.count--T--Function--F#-.md) for an option.|  
|[exists](../vs140/Option.exists--T--Function--F#-.md)  `: ('T -> bool) -> 'T option -> bool`|Evaluates the equivalent of [List.exists](../vs140/List.exists--T--Function--F#-.md) for an option.|  
|[fold](../vs140/Option.fold--T--State--Function--F#-.md)  `: ('State -> 'T -> 'State) -> 'State -> 'T option -> 'State`|Evaluates the equivalent of [List.fold](../vs140/List.fold--T--State--Function--F#-.md) for an option.|  
|[foldBack](../vs140/Option.foldBack--T--State--Function--F#-.md)  `: ('T -> 'State -> 'State) -> 'T option -> 'State -> 'State`|Performs the equivalent of the [List.foldBack](../vs140/List.foldBack--T--State--Function--F#-.md) operation on an option.|  
|[forall](../vs140/Option.forall--T--Function--F#-.md)  `: ('T -> bool) -> 'T option -> bool`|Evaluates the equivalent of [List.forall](../vs140/List.forall--T--Function--F#-.md) for an option type.|  
|[get](../vs140/Option.get--T--Function--F#-.md)  `: 'T option -> 'T`|Gets the value associated with the option.|  
|[isNone](../vs140/Option.isNone--T--Function--F#-.md)  `: 'T option -> bool`|Returns `true` if the option is `None`.|  
|[isSome](../vs140/Option.isSome--T--Function--F#-.md)  `: 'T option -> bool`|Returns `true` if the option is not `None`.|  
|[iter](../vs140/Option.iter--T--Function--F#-.md)  `: ('T -> unit) -> 'T option -> unit`|Executes a function for an option value.|  
|[map](../vs140/Option.map--T--U--Function--F#-.md)  `: ('T -> 'U) -> 'T option -> 'U option`|Transforms an option value by using a specified mapping function.|  
|[toArray](../vs140/Option.toArray--T--Function--F#-.md)  `: 'T option -> 'T []`|Convert the option to an array of length 0 or 1.|  
|[toList](../vs140/Option.toList--T--Function--F#-.md)  `: 'T option -> 'T list`|Convert the option to a list of length 0 or 1.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)