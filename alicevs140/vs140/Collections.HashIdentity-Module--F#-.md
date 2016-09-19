---
title: "Collections.HashIdentity Module (F#)"
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
  - Collections.HashIdentity
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8e676091-4b8d-44d6-83cc-5caeb3f78cf4
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.HashIdentity Module (F#)
Common notions of value identity used with hash tables.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module HashIdentity  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[FromFunctions](../Topic/HashIdentity.FromFunctions%3C'T%3E%20Function%20\(F%23\).md)  `: ('T -> int) -> ('T -> 'T -> bool) -> IEqualityComparer<'T>`|Hash using the given hashing and equality functions.|  
|[LimitedStructural](../Topic/HashIdentity.LimitedStructural%3C'T%3E%20Function%20\(F%23\).md)  `: int -> IEqualityComparer<'T>`|Provides structural hashing up to a specified number of elements.|  
|[Reference](../Topic/HashIdentity.Reference%3C'T%3E%20Type%20Function%20\(F%23\).md)  `: IEqualityComparer<'T>`|Implements physical hashing, which means that it hashes on reference identity of objects, and the contents of value types..|  
|[Structural](../Topic/HashIdentity.Structural%3C'T%3E%20Type%20Function%20\(F%23\).md)  `: IEqualityComparer<'T>`|Implements structural hashing. Hashes using [Operators.(=)](../vs140/Operators.--=----T--Function--F#-.md) and [Operators.hash](../Topic/Operators.hash%3C'T%3E%20Function%20\(F%23\).md).|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)