---
title: "Array.init&lt;&#39;T&gt; Function (F#)"
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
  - Array.init<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ee898089-63b0-40aa-910c-5ae7e32f6665
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.init&lt;&#39;T&gt; Function (F#)
Creates an array given the dimension and a generator function to compute the elements.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Array  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.init : int -> (int -> 'T) -> 'T []  
  
// Usage:  
Array.init count initializer  
```  
  
#### Parameters  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of elements to initialize.  
  
 `initializer`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T`  
  
 The function to generate the initial values for each index.  
  
## Return Value  
 The created array.  
  
## Remarks  
 This function is named `Initialize` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code demonstrates the use of `Array.init`.  
  
 [!CODE [FsArrays#101](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#101)]  
  
 **Array of squares: [&#124;0; 1; 4; 9; 16; 25; 36; 49; 64; 81&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)