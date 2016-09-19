---
title: "Array4D.init&lt;&#39;T&gt; Function (F#)"
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
  - Array4D.init<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 41e8bf42-5a11-4884-8890-a1b194f5f80e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array4D.init&lt;&#39;T&gt; Function (F#)
Creates an array given the dimensions and a generator function to compute the elements.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array4D  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array4D.init : int -> int -> int -> int -> (int -> int -> int -> int -> 'T) -> 'T [,,,]  
  
// Usage:  
Array4D.init length1 length2 length3 length4 initializer  
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
  
 `initializer`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T`  
  
 The function to create an initial value at each index in the array.  
  
## Return Value  
 The created array.  
  
## Remarks  
 This function is named `Initialize` in the assembly. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array4D Module (F#)](../vs140/Collections.Array4D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)