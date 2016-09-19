---
title: "Option.foldBack&lt;&#39;T,&#39;State&gt; Function (F#)"
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
  - Option.foldBack<'T,'State>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a882fbaf-c019-46f0-b4f5-b8c2b8b90ffb
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option.foldBack&lt;&#39;T,&#39;State&gt; Function (F#)
Performs the equivalent of the [List.foldBack](../vs140/List.foldBack--T--State--Function--F#-.md) operation on an option.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Option  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
foldBack : ('T -> 'State -> 'State) -> 'T option -> 'State -> 'State  
  
// Usage:  
foldBack folder option state  
```  
  
#### Parameters  
 `folder`  
 Type: `'T -> 'State -> 'State`  
  
 A function to update the state data when given a value from an option.  
  
 `option`  
 Type: `'T`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The input option.  
  
 `state`  
 Type: `'State`  
  
 The initial state.  
  
## Return Value  
 If the option is `None`, it returns the initial value of `state`. Otherwise, it returns the updated state, the result of applying the `folder` function with the option value and the initial state.  
  
## Remarks  
 The expression `fold f inp s` evaluates to `match inp with None -> s | Some x -> f x s`.  
  
 This function is named `FoldBack` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Option.foldBack`.  
  
 [!CODE [FsOptions#5](../CodeSnippet/VS_Snippets_Fsharp/fsoptions#5)]  
  
 **Output**  
  
 **[1; 2; 3; 4; 5; 6; 7; 8; 9; 10][0; 1; 2; 3; 4; 5; 6; 7; 8; 9; 10]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Option Module (F#)](../vs140/Core.Option-Module--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)