---
title: "List.scanBack&lt;&#39;T,&#39;State&gt; Function (F#)"
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
  - List.scanBack<'T,'State>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 6c131a36-d152-46d4-80c6-d3ee3ac80925
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.scanBack&lt;&#39;T,&#39;State&gt; Function (F#)
Like [List.foldBack](../vs140/List.foldBack--T--State--Function--F#-.md), but returns both the intermediate and final results.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.scanBack : ('T -> 'State -> 'State) -> 'T list -> 'State -> 'State list  
  
// Usage:  
List.scanBack folder list state  
```  
  
#### Parameters  
 `folder`  
 Type: `'T -> 'State -> 'State`  
  
 The function to update the state given the input elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
 `state`  
 Type: `'State`  
  
 The initial state.  
  
## Return Value  
 The list of states.  
  
## Remarks  
 This function is named `ScanBack` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows how to use `List.scanBack`, and also contrasts its behavior with [List.scan](../vs140/List.scan--T--State--Function--F#-.md).  
  
 [!CODE [FsLists#61](../CodeSnippet/VS_Snippets_Fsharp/fslists#61)]  
  
 Output  
  
 **Operations:**  
**add 1  add 2  subtract 5**   
**List.scan List.scanBack**  
 **10         10**  
 **11          5**  
 **13          7**  
 **8          8**  
**Operations:**  
**add 1  multiply by 5  square**   
**List.scan List.scanBack**  
 **10         10**  
 **11        100**  
 **55        500**  
 **3025        501**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)