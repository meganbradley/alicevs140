---
title: "List.length&lt;&#39;T&gt; Function (F#)"
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
  - List.length<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7a1f5f43-d7fd-42cc-95bf-9ac906d46ca9
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.length&lt;&#39;T&gt; Function (F#)
Returns the length of the list.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.length : 'T list -> int  
  
// Usage:  
List.length list  
```  
  
#### Parameters  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The length of the list.  
  
## Remarks  
 This function is named `Length` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.length`.  
  
 [!CODE [FsLists#48](../CodeSnippet/VS_Snippets_Fsharp/fslists#48)]  
  
 **Output**  
  
 **Length: 100**  
**Length: 0**  
**Length: 50**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)