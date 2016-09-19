---
title: "Operators.( &gt;&gt; )&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)"
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
  - Operators.( >> )<'T1,'T2,'T3>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b604e1f2-7d61-4ff0-aa0d-0b691b17bd0b
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.( &gt;&gt; )&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)
Composes two functions, the function on the left being applied first  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( >> ) : ('T1 -> 'T2) -> ('T2 -> 'T3) -> 'T1 -> 'T3  
  
// Usage:  
func1 >> func2  
```  
  
#### Parameters  
 `func1`  
 Type: `'T1 -> 'T2`  
  
 The first function to apply.  
  
 `func2`  
 Type: `'T2 -> 'T3`  
  
 The second function to apply.  
  
## Return Value  
 The composition of the input functions.  
  
## Remarks  
  
## Example  
 The following example demonstrates the use of the composition operator (`>>`).  
  
 [!CODE [FsOperators#7](../CodeSnippet/VS_Snippets_Fsharp/fsoperators#7)]  
  
 **abc.append1.append2**  
**abc.append1.append2.append3**  
**myfile.txt**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)