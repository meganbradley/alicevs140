---
title: "List.ofArray&lt;&#39;T&gt; Function (F#)"
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
  - List.of_array<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f4bddc26-8c8f-4307-a6d7-a49dceb97032
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.ofArray&lt;&#39;T&gt; Function (F#)
Creates a list from the given array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.ofArray : 'T [] -> 'T list  
  
// Usage:  
List.ofArray array  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The list of elements from the array.  
  
## Remarks  
 This function is named `OfArray` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.ofArray`.  
  
 [!CODE [FsLists#59](../CodeSnippet/VS_Snippets_Fsharp/fslists#59)]  
  
 **F# Interactive Output**  
  
 **val list1 : int list = [1; 2; 3; 4; 5; 6; 7; 8; 9; 10]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)