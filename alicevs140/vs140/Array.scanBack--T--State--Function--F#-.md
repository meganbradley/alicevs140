---
title: "Array.scanBack&lt;&#39;T,&#39;State&gt; Function (F#)"
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
  - Array.scanBack<'T,'State>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7610f406-7a5c-41db-a0ca-8e2a2a4826ad
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.scanBack&lt;&#39;T,&#39;State&gt; Function (F#)
Like [Array.foldBack](../vs140/Array.foldBack--T--State--Function--F#-.md), but returns both the intermediate and final results.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.scanBack : ('T -> 'State -> 'State) -> 'T [] -> 'State -> 'State []  
  
// Usage:  
Array.scanBack folder array state  
```  
  
#### Parameters  
 `folder`  
 Type: `'T -> 'State -> 'State`  
  
 The function to update the state given the input elements.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
 `state`  
 Type: `'State`  
  
 The initial state.  
  
## Return Value  
 The array of state values.  
  
## Remarks  
 This function is named `ScanBack` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code contrasts the behavior of [Array.scan](../vs140/Array.scan--T--State--Function--F#-.md) and `Array.scanBack`.  
  
 [!CODE [FsArrays#36](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#36)]  
  
 **Output**  
  
  **10         10**  
 **11          5**  
 **13          7**  
 **8          8**  
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
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)