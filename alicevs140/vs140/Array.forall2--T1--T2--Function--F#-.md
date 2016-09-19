---
title: "Array.forall2&lt;&#39;T1,&#39;T2&gt; Function (F#)"
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
  - Array.forall2<'T1,'T2>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c68f61a1-030c-4024-b705-c4768b6c96b9
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.forall2&lt;&#39;T1,&#39;T2&gt; Function (F#)
Tests if all corresponding elements of the array satisfy the given predicate pairwise.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.forall2 : ('T1 -> 'T2 -> bool) -> 'T1 [] -> 'T2 [] -> bool  
  
// Usage:  
Array.forall2 predicate array1 array2  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T1 -> 'T2 ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `array1`  
 Type: `'T1`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The first input array.  
  
 `array2`  
 Type: `'T2`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The second input array.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input arrays differ in length.|  
  
## Return Value  
 `true` if all of the array elements satisfy the predicate. Otherwise, returns `false`.  
  
## Remarks  
 The predicate is applied to matching elements in the two collections up to the lesser of the two lengths of the collections. If any application returns `false` then the overall result is `false` and no further elements are tested. Otherwise, if one collection is longer than the other, then the <xref:System.ArgumentException?qualifyHint=False> exception is raised.  
  
 This function is named `ForAll2` in compiled assemblies. If accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example shows the use of `Array.forall2` to test the equality of all the elements in two arrays.  
  
 [!CODE [FsArrays#242](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#242)]  
  
 **true**  
**false**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)