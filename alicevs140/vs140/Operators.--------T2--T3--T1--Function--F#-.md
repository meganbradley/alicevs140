---
title: "Operators.( &lt;&lt; )&lt;&#39;T2,&#39;T3,&#39;T1&gt; Function (F#)"
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
  - Operators.( << )<'T2,'T3,'T1>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c0293938-8230-46c3-a775-0d539854171f
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.( &lt;&lt; )&lt;&#39;T2,&#39;T3,&#39;T1&gt; Function (F#)
Composes two functions, the function on the right being applied first.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( << ) : ('T2 -> 'T3) -> ('T1 -> 'T2) -> 'T1 -> 'T3  
  
// Usage:  
func2 << func1  
```  
  
#### Parameters  
 `func2`  
 Type: `'T2 -> 'T3`  
  
 The second function to apply.  
  
 `func1`  
 Type: `'T1 -> 'T2`  
  
 The first function to apply.  
  
## Return Value  
 The composition of the input functions.  
  
## Remarks  
 This operator is referred to as the *backward* or *reverse composition operator*.  
  
## Example  
 The following example demonstrates the use of the reverse composition operator (`<<`).  
  
 [!CODE [FsOperators#8](../CodeSnippet/VS_Snippets_Fsharp/fsoperators#8)]  
  
 **abc.append2.append1**  
**abc.append3.append2.append1**  
**myfile.txt**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)