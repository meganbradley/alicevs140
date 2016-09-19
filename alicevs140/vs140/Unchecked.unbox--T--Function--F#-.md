---
title: "Unchecked.unbox&lt;&#39;T&gt; Function (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c24a9f99-8562-4dba-8c93-d831ecf94795
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Unchecked.unbox&lt;&#39;T&gt; Function (F#)
Unboxes a strongly typed value. This is the inverse of `box`; therefore, `unbox<t>(box<t> a)` equals `a`.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.Operators.Unchecked  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
unbox : obj -> 'T  
  
// Usage:  
unbox   
```  
  
#### Parameters  
 `value`  
 Type: [obj](../Topic/Core.obj%20Type%20Abbreviation%20\(F%23\).md)  
  
 The value to unbox.  
  
## Return Value  
 The unboxed result.  
  
## Remarks  
 This function is named `Unbox` in the .NET assembly. If accessing the member from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Operators.Unchecked Module (F#)](../vs140/Operators.Unchecked-Module--F#-.md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Operators.box<'T> Function (F#)](../vs140/Operators.box--T--Function--F#-.md)