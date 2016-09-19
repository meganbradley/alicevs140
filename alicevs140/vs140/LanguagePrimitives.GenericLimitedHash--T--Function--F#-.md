---
title: "LanguagePrimitives.GenericLimitedHash&lt;&#39;T&gt; Function (F#)"
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
  - LanguagePrimitives.GenericLimitedHash<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1ada2a57-433f-4fa7-b8ce-1aa010d626c7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.GenericLimitedHash&lt;&#39;T&gt; Function (F#)
Hash a value according to its structure. Use the given limit to restrict the hash when hashing F# records, lists and union types.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
GenericLimitedHash : int -> 'T -> int  
  
// Usage:  
GenericLimitedHash limit obj  
```  
  
#### Parameters  
 `limit`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The limit on the number of nodes.  
  
 `obj`  
 Type: `'T`  
  
 The input object.  
  
## Return Value  
 The hashed value.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.LanguagePrimitives Module (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)