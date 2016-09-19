---
title: "Option.exists&lt;&#39;T&gt; Function (F#)"
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
  - Option.exists<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a606d2d4-fddc-4eab-ab37-c6138fb7ad99
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option.exists&lt;&#39;T&gt; Function (F#)
Evaluates the equivalent of [List.exists](../vs140/List.exists--T--Function--F#-.md) for an option.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Option  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
exists : ('T -> bool) -> 'T option -> bool  
  
// Usage:  
exists predicate option  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 A function that evaluates to a Boolean when given a value from the option type.  
  
 `option`  
 Type: `'T`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The input option.  
  
## Return Value  
 Returns `false` if the option is `None`, otherwise it returns the result of applying the predicate to the option value.  
  
## Remarks  
 The expression `exists p inp` evaluates to `match inp with None -> false | Some x -> p x`.  
  
 This function is named `Exists` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Option.exists`.  
  
 [!CODE [FsOptions#3](../CodeSnippet/VS_Snippets_Fsharp/fsoptions#3)]  
  
 **Output**  
  
 **truefalsefalse**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Option Module (F#)](../vs140/Core.Option-Module--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)