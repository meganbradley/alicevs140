---
title: "Array.scan&lt;&#39;T,&#39;State&gt; Function (F#)"
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
  - Array.scan<'T,'State>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f6893608-9146-450d-9ebb-a0016803fbb0
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.scan&lt;&#39;T,&#39;State&gt; Function (F#)
Like [Array.fold](../vs140/Array.fold--T--State--Function--F#-.md), but returns the intermediate and final results.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.scan : ('State -> 'T -> 'State) -> 'State -> 'T [] -> 'State []  
  
// Usage:  
Array.scan folder state array  
```  
  
#### Parameters  
 `folder`  
 Type: `'State -> 'T -> 'State`  
  
 The function to update the state given the input elements.  
  
 `state`  
 Type: `'State`  
  
 The initial state.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The array of state values.  
  
## Remarks  
 This function is named `Scan` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Array.scan`.  
  
 [!CODE [FsArrays#35](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#35)]  
  
 **Output**  
  
 **Initial balance:**  
 **$   1122.73**  
**Transaction   Balance**  
**$   -100.00 $   1122.73**  
**$    450.34 $   1022.73**  
**$    -62.34 $   1473.07**  
**$   -127.00 $   1410.73**  
**$    -13.50 $   1283.73**  
**$    -12.92 $   1270.23**  
**Final balance:**  
 **$   1257.31**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)