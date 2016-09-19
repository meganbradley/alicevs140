---
title: "FuncConvert.ToFSharpFunc&lt;&#39;T,&#39;U&gt; Method (F#)"
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
ms.assetid: 1352ba11-7edc-4038-8173-de73133ad490
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FuncConvert.ToFSharpFunc&lt;&#39;T,&#39;U&gt; Method (F#)
Convert the given <xref:System.Converter`2?qualifyHint=False> delegate object to an F# function value.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member ToFSharpFunc : Converter<'T,'U> -> 'T -> 'U  
  
// Usage:  
FuncConvert.ToFSharpFunc (converter)  
```  
  
#### Parameters  
 `converter`  
 Type: <xref:System.Converter`2?qualifyHint=False>`<'T,'U>`  
  
 The input Converter.  
  
## Return Value  
 The F# function.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.FuncConvert Class (F#)](../Topic/Core.FuncConvert%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)