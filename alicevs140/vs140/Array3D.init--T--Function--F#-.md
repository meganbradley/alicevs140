---
title: "Array3D.init&lt;&#39;T&gt; Function (F#)"
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
  - Array3D.init<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fcd89119-995c-4f28-9e79-7e8b14ca6f08
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array3D.init&lt;&#39;T&gt; Function (F#)
Creates an array given the dimensions and a generator function to compute the elements.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Array3D  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array3D.init : int -> int -> int -> (int -> int -> int -> 'T) -> 'T [,,]  
  
// Usage:  
Array3D.init length1 length2 length3 initializer  
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
  
 `initializer`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T`  
  
 The function to create an initial value at each index into the array.  
  
## Return Value  
 The created array.  
  
## Remarks  
 This function is named `Initialize` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array3D Module (F#)](../vs140/Collections.Array3D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)