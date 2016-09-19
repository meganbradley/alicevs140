---
title: "List.unzip3&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)"
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
  - List.unzip3<'T1,'T2,'T3>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 43078c77-32ec-4342-85b3-c31ccf984db4
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.unzip3&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)
Splits a list of triples into three lists.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.unzip3 : ('T1 * 'T2 * 'T3) list -> 'T1 list * 'T2 list * 'T3 list  
  
// Usage:  
List.unzip3 list  
```  
  
#### Parameters  
 `list`  
 Type: `('T1 * 'T2 * 'T3)`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 Three lists of split elements.  
  
## Remarks  
 This function is named `Unzip3` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.forall2`.  
  
 [!CODE [FsLists#39](../CodeSnippet/VS_Snippets_Fsharp/fslists#39)]  
  
 **Output**  
  
 **[1; 4] [2; 5] [3; 6]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)