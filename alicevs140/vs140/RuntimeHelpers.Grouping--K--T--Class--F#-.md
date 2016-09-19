---
title: "RuntimeHelpers.Grouping&lt;&#39;K,&#39;T&gt; Class (F#)"
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
ms.assetid: 4a6ac4d6-5b30-44bb-b34d-c6773f86dedf
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RuntimeHelpers.Grouping&lt;&#39;K,&#39;T&gt; Class (F#)
Reconstructs a grouping after applying a mutable to immutable mapping transformation on a result of a query. This type is used to implement `groupBy` and `groupValBy` for F# query expressions.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.RuntimeHelpers  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type Grouping<'K,'T> =  
 class  
  inherit IEnumerable<'T>  
  inherit IEnumerable  
  inherit IGrouping<'K,'T>  
  new Grouping : 'K * seq<'T> -> Grouping<'K,'T>  
 end  
```  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/RuntimeHelpers.Grouping--K--T--Constructor--F#-.md)|Constructs a new instance of `Grouping`.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Linq.RuntimeHelpers Namespace (F#)](../vs140/Microsoft.FSharp.Linq.RuntimeHelpers-Namespace--F#-.md)   
 [Query Expressions (F#)](../Topic/Query%20Expressions%20\(F%23\).md)