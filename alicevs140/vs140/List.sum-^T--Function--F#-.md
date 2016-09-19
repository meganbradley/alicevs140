---
title: "List.sum&lt;^T&gt; Function (F#)"
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
  - List.sum<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 54d47fe3-5ecf-4883-beb5-e915342a17f9
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.sum&lt;^T&gt; Function (F#)
Returns the sum of the elements in the list.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.sum : ^T list -> ^T (requires ^T with static member (+) and ^T with static member Zero)  
  
// Usage:  
List.sum list  
```  
  
#### Parameters  
 `list`  
 Type: `^T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The resulting sum.  
  
## Remarks  
 This function is named `Sum` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.sum`, [List.sumBy](../vs140/List.sumBy--T-^U--Function--F#-.md), and [List.average](../Topic/List.average%3C%5ET%3E%20Function%20\(F%23\).md).  
  
 [!CODE [FsLists#11](../CodeSnippet/VS_Snippets_Fsharp/fslists#11)]  
  
 **Output**  
  
 **1.000000**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)