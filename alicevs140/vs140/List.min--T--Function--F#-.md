---
title: "List.min&lt;&#39;T&gt; Function (F#)"
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
  - List.min<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 24ec1666-00b9-49f0-9f03-4b157b8c331e
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.min&lt;&#39;T&gt; Function (F#)
Returns the lowest of all elements of the list, compared by using [Operators.min](../vs140/Operators.min--T--Function--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.min : 'T list -> 'T (requires comparison)  
  
// Usage:  
List.min list  
```  
  
#### Parameters  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the list is empty.|  
  
## Return Value  
 The minimum value.  
  
## Remarks  
 This function is named `Min` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.min`.  
  
 [!CODE [FsLists#57](../CodeSnippet/VS_Snippets_Fsharp/fslists#57)]  
  
 **Output**  
  
 **-4**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)