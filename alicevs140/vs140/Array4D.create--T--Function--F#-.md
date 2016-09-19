---
title: "Array4D.create&lt;&#39;T&gt; Function (F#)"
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
  - Array4D.create<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c146b4b0-2e63-4d00-8451-5d72833ccfdc
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array4D.create&lt;&#39;T&gt; Function (F#)
Creates an array whose elements are all initially the given value  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array4D  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array4D.create : int -> int -> int -> int -> 'T -> 'T [,,,]  
  
// Usage:  
Array4D.create length1 length2 length3 length4 initial  
```  
  
#### Parameters  
 `length1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the first dimension.  
  
 `length2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the second dimension.  
  
 `length3`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the third dimension.  
  
 `length4`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the fourth dimension.  
  
 `initial`  
 Type: `'T`  
  
 The initial value for each element of the array.  
  
## Return Value  
 The created array.  
  
## Remarks  
 This function is named `Create` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array4D Module (F#)](../vs140/Collections.Array4D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)