---
title: "IntrinsicFunctions.SetArray&lt;&#39;T&gt; Function (F#)"
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
  - IntrinsicFunctions.SetArray<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f7904de2-c969-4314-a5ad-a2e3fed17a4a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IntrinsicFunctions.SetArray&lt;&#39;T&gt; Function (F#)
The standard overloaded associative (indexed) mutation operator.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives.IntrinsicFunctions  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
SetArray : 'T [] -> int -> 'T -> unit  
  
// Usage:  
SetArray target index value  
```  
  
#### Parameters  
 `target`  
 Type: `'T` [&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 An array.  
  
 `index`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 An index into the array.  
  
 `value`  
 Type: `'T`  
  
 The new value to set at the specified array index.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [LanguagePrimitives.IntrinsicFunctions Module (F#)](../vs140/LanguagePrimitives.IntrinsicFunctions-Module--F#-.md)   
 [Microsoft.FSharp.Core.LanguagePrimitives Namespace (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)