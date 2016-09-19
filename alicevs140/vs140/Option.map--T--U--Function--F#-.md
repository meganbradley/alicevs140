---
title: "Option.map&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Option.map<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 91a20385-7e73-40c2-9adc-635e86d6a622
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option.map&lt;&#39;T,&#39;U&gt; Function (F#)
Transforms an option value by using a specified mapping function.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.Option  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
map : ('T -> 'U) -> 'T option -> 'U option  
  
// Usage:  
map mapping option  
```  
  
#### Parameters  
 `mapping`  
 Type: `'T -> 'U`  
  
 A function to apply to the option value.  
  
 `option`  
 Type: `'T` [option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The input option.  
  
## Return Value  
 An option of the result of applying the mapping function, or `None` if the input is `None`.  
  
## Remarks  
 The expression `map f inp` evaluates to `match inp with None -> None | Some x -> Some (f x)`.  
  
 This function is named `Map` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable, Portable  
  
## See Also  
 [Core.Option Module (F#)](../vs140/Core.Option-Module--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)