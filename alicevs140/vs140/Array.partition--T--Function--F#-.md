---
title: "Array.partition&lt;&#39;T&gt; Function (F#)"
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
  - Array.partition<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1ecc2a7d-ad05-40c0-a8a8-08cc698f7566
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.partition&lt;&#39;T&gt; Function (F#)
Splits the collection into two collections, containing the elements for which the given predicate returns `true` and `false` respectively.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.partition : ('T -> bool) -> 'T [] -> 'T [] * 'T []  
  
// Usage:  
Array.partition predicate array  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->` [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `array`  
 Type: `'T` [&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 A pair of arrays. The first containing the elements the predicate for which the predicate evaluated to `true`, and the second containing those for which the predicate evaluated to `false`.  
  
## Remarks  
 This function is named `Partition` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Array.partition`.  
  
 [!CODE [FsArrays#33](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#33)]  
  
 **Output**  
  
 **[&#124;51; 52; 53; 54; 55; 56; 57; 58; 59&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)