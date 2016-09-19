---
title: "Array4D.get&lt;&#39;T&gt; Function (F#)"
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
  - Array4D.get<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d268205c-d77b-4816-8360-57be8e770005
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array4D.get&lt;&#39;T&gt; Function (F#)
Fetches an element from a 4D array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array4D  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array4D.get : 'T [,,,] -> int -> int -> int -> int -> 'T  
  
// Usage:  
Array4D.get array index1 index2 index3 index4  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;,,,&#93;](../vs140/Core.--T--Type--F#-1.md)  
  
 The input array.  
  
 `index1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the first dimension.  
  
 `index2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the second dimension.  
  
 `index3`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the third dimension.  
  
 `index4`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the fourth dimension.  
  
## Return Value  
 The value at the given index.  
  
## Remarks  
 You can also use the syntax `array.[index1,index2,index3,index4]`.  
  
 This function is named `Get` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array4D Module (F#)](../vs140/Collections.Array4D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)