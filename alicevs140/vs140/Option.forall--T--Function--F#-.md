---
title: "Option.forall&lt;&#39;T&gt; Function (F#)"
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
  - Option.forall<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ba884586-5eae-49c5-9e36-05481c1c3428
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option.forall&lt;&#39;T&gt; Function (F#)
Evaluates the equivalent of [List.forall](../vs140/List.forall--T--Function--F#-.md) for an option type.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.Option  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
forall : ('T -> bool) -> 'T option -> bool  
  
// Usage:  
forall predicate option  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 A function that evaluates to a Boolean when given a value from the option type.  
  
 `option`  
 Type: `'T`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The input option.  
  
## Return Value  
 `true` if the option is `None`, otherwise it returns the result of applying the predicate to the option value.  
  
## Remarks  
 The expression `forall p inp` evaluates to `match inp with None -> true | Some x -> p x`.  
  
 This function is named `ForAll` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Option.forall`.  
  
 [!CODE [FsOptions#6](../CodeSnippet/VS_Snippets_Fsharp/fsoptions#6)]  
  
 **Output**  
  
 **truetruefalsefalsetruefalse**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Option Module (F#)](../vs140/Core.Option-Module--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)