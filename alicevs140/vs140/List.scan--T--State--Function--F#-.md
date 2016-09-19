---
title: "List.scan&lt;&#39;T,&#39;State&gt; Function (F#)"
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
  - List.scan<'T,'State>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 21f636db-885c-4a72-970e-e3841f33a1b8
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.scan&lt;&#39;T,&#39;State&gt; Function (F#)
Applies a function to each element of the collection, threading an accumulator argument through the computation. This function takes the second argument, and applies the function to it and the first element of the list. Then, it passes this result into the function along with the second element, and so on. Finally, it returns the list of intermediate results and the final result.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.scan : ('State -> 'T -> 'State) -> 'State -> 'T list -> 'State list  
  
// Usage:  
List.scan folder state list  
```  
  
#### Parameters  
 `folder`  
 Type: `'State -> 'T -> 'State`  
  
 The function to update the state given the input elements.  
  
 `state`  
 Type: `'State`  
  
 The initial state.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The list of states.  
  
## Remarks  
 This function is named `Scan` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.scan`.  
  
 [!CODE [FsLists#54](../CodeSnippet/VS_Snippets_Fsharp/fslists#54)]  
  
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
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)