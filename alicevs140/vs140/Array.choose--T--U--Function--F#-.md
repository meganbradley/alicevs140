---
title: "Array.choose&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Array.choose<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f5c8a5e2-637f-44d4-b35c-be96a6618b09
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.choose&lt;&#39;T,&#39;U&gt; Function (F#)
Applies the given function to each element of the array. Returns the array comprised of the results `x` for each element where the function returns `Some(x)`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.choose : ('T -> 'U option) -> 'T [] -> 'U []  
  
// Usage:  
Array.choose chooser array  
```  
  
#### Parameters  
 `chooser`  
 Type: `'T -> 'U`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The function to generate options from the elements.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The array of results.  
  
## Remarks  
 This function is named `Choose` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code demonstrates the use of `Array.choose` to perform an operation only on the even numbers in an array.  
  
 [!CODE [FsArrays#14](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#14)]  
  
 **[&#124;3.0; 15.0; 35.0; 63.0; 99.0&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)