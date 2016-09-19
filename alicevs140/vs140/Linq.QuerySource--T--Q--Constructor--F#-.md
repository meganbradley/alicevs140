---
title: "Linq.QuerySource&lt;&#39;T,&#39;Q&gt; Constructor (F#)"
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
ms.assetid: 9ca12119-7ff2-4e0a-b1cc-ac32dfcbb2f6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linq.QuerySource&lt;&#39;T,&#39;Q&gt; Constructor (F#)
Constructs an instance of `QuerySource`.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
new QuerySource : seq<'T> -> QuerySource<'T,'Q>  
  
// Usage:  
new QuerySource (source)  
```  
  
#### Parameters  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)<'T>  
  
 An enumerable sequence of data to query against, such as a database table or collection.  
  
## Return Value  
 A new instance of `QuerySource`.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Linq.QuerySource<'T,'Q> Class (F#)](../vs140/Linq.QuerySource--T--Q--Class--F#-.md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)