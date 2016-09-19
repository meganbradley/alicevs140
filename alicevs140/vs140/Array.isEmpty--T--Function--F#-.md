---
title: "Array.isEmpty&lt;&#39;T&gt; Function (F#)"
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
  - Array.isEmpty<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c2bd48e9-8aba-4bea-ad84-17352886d3a8
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.isEmpty&lt;&#39;T&gt; Function (F#)
Tests whether an array is empty.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.isEmpty : 'T [] -> bool  
  
// Usage:  
Array.isEmpty array  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 `true` if the array is empty. Otherwise, returns `false`.  
  
## Remarks  
 This function is named `IsEmpty` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Array.isEmpty`.  
  
 [!CODE [FsArrays#48](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#48)]  
  
 **Output**  
  
 **This array contains the following elements:**  
**"test1" "test2"**   
**There are no elements in this array.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)