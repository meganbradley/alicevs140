---
title: "Option.isSome&lt;&#39;T&gt; Function (F#)"
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
  - Option.isSome<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 41ad0857-5672-4326-84b5-c33dc43dcf79
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option.isSome&lt;&#39;T&gt; Function (F#)
Returns `true` if the option is not `None`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Option  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
isSome : 'T option -> bool  
  
// Usage:  
isSome option  
```  
  
#### Parameters  
 `option`  
 Type: `'T`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The input option.  
  
## Return Value  
 `true` if the option is not `None`.  
  
## Remarks  
 This function is named `IsSome` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Option Module (F#)](../vs140/Core.Option-Module--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)