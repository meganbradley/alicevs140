---
title: "FSharpFunc.Invoke&lt;&#39;T1,&#39;T2,&#39;T3,&#39;U&gt; Method (F#)"
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
  - FSharpFunc.Invoke<'T1,'T2,'T3,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 212501c1-8378-461b-b5ad-54f8b3d41f56
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpFunc.Invoke&lt;&#39;T1,&#39;T2,&#39;T3,&#39;U&gt; Method (F#)
Invoke an F# first class function value that accepts three curried arguments without intervening execution.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.OptimizedClosures  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.Invoke : FSharpFunc<'T1,'T2,'T3,'U> -> 'T1 * 'T2 * 'T3 -> 'U  
  
// Usage:  
fSharpFunc.Invoke (arg1, arg2, arg3)  
```  
  
#### Parameters  
 `arg1`  
 Type: `'T1`  
  
 The first argument.  
  
 `arg2`  
 Type: `'T2`  
  
 The second argument.  
  
 `arg3`  
 Type: `'T3`  
  
 The third argument.  
  
## Return Value  
 The function result.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [OptimizedClosures.FSharpFunc<'T1,'T2,'T3,'U> Class (F#)](../vs140/OptimizedClosures.FSharpFunc--T1--T2--T3--U--Class--F#-.md)   
 [Microsoft.FSharp.Core.OptimizedClosures Namespace (F#)](../vs140/Core.OptimizedClosures-Module--F#-.md)