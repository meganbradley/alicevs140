---
title: "List.find&lt;&#39;T&gt; Function (F#)"
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
  - List.find<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 0594593e-9c75-44c1-8f5a-a37b2e561c06
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.find&lt;&#39;T&gt; Function (F#)
Returns the first element for which the given function returns `true`. Raises <xref:System.Collections.Generic.KeyNotFoundException?qualifyHint=False> if no such element exists.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.find : ('T -> bool) -> 'T list -> 'T  
  
// Usage:  
List.find predicate list  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.Collections.Generic.KeyNotFoundException?qualifyHint=False>|Thrown if the predicate evaluates to false for all the elements of the list.|  
  
## Return Value  
 The first element that satisfies the predicate.  
  
## Remarks  
 This function is named `Find` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.find`.  
  
 [!CODE [FsLists#8](../CodeSnippet/VS_Snippets_Fsharp/fslists#8)]  
  
 **Output**  
  
 **5**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)