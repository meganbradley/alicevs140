---
title: "List.head&lt;&#39;T&gt; Function (F#)"
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
  - List.hd<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 22514cc5-0511-498b-a2cc-837b688a6da2
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.head&lt;&#39;T&gt; Function (F#)
Returns the first element of the list.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.head : 'T list -> 'T  
  
// Usage:  
List.head list  
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
 The first element of the list.  
  
## Remarks  
 Raises <xref:System.ArgumentException?qualifyHint=False> if `list` is empty  
  
 This function is named `Head` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)