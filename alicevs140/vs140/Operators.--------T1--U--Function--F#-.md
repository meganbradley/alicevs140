---
title: "Operators.( |&gt; )&lt;&#39;T1,&#39;U&gt; Function (F#)"
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
  - Operators.( |> )<'T1,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 698b9e4a-a6d7-4ab1-8809-b2fdba783070
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.( |&gt; )&lt;&#39;T1,&#39;U&gt; Function (F#)
Apply a function to a value, the value being on the left, the function on the right.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |> ) : 'T1 -> ('T1 -> 'U) -> 'U  
  
// Usage:  
arg |> func  
```  
  
#### Parameters  
 `arg`  
 Type: `'T1`  
  
 The argument.  
  
 `func`  
 Type: `'T1 -> 'U`  
  
 The function.  
  
## Return Value  
 The function result.  
  
## Remarks  
  
## Example  
 The following example demonstrates the use of the forward pipe operator.  
  
 [!CODE [FsOperators#1](../CodeSnippet/VS_Snippets_Fsharp/fsoperators#1)]  
  
 **"abc" &#124;> append1 gives "abc.append1"**  
**result2: "abc.append1.append2"**  
**300 200 100**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)