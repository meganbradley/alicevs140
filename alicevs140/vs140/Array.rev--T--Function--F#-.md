---
title: "Array.rev&lt;&#39;T&gt; Function (F#)"
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
  - Array.rev<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1bbf822c-763b-4794-af21-97d2e48ef709
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.rev&lt;&#39;T&gt; Function (F#)
Returns a new array with the elements in reverse order.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.rev : 'T [] -> 'T []  
  
// Usage:  
Array.rev array  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The reversed array.  
  
## Remarks  
 This function is named `Reverse` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example shows how to reverse the elements in an array by using `Array.rev`.  
  
 [!CODE [FsArrays#18](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#18)]  
  
 **"Hello world!"**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)