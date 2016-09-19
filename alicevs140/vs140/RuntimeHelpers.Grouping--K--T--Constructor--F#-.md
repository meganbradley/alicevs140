---
title: "RuntimeHelpers.Grouping&lt;&#39;K,&#39;T&gt; Constructor (F#)"
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
ms.assetid: 6372a867-5fcd-41e1-9616-8d3d094d5103
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RuntimeHelpers.Grouping&lt;&#39;K,&#39;T&gt; Constructor (F#)
Constructs a new instance of a grouping for use in F# query expressions.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.RuntimeHelpers  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
new Grouping : 'K * seq<'T> -> Grouping<'K,'T>  
  
// Usage:  
new Grouping (key, values)  
```  
  
#### Parameters  
 `key`  
 Type: 'K  
  
 The grouping key.  
  
 `values`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)<'T>  
  
 The values to be grouped.  
  
## Return Value  
 A collection that represents the grouped values.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [RuntimeHelpers.Grouping<'K,'T> Class (F#)](../vs140/RuntimeHelpers.Grouping--K--T--Class--F#-.md)   
 [Microsoft.FSharp.Linq.RuntimeHelpers Namespace (F#)](../vs140/Microsoft.FSharp.Linq.RuntimeHelpers-Namespace--F#-.md)   
 [Query Expressions (F#)](../Topic/Query%20Expressions%20\(F%23\).md)