---
title: "Lazy.Create&lt;&#39;T&gt; Extension Method (F#)"
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
  - Lazy.Create<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b3ac5a61-f87d-4332-b45c-f56712693b77
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Lazy.Create&lt;&#39;T&gt; Extension Method (F#)
Creates a lazy computation that evaluates to the result of the given function when forced.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.LazyExtensions  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
type System.Lazy with  
  member static Create : Lazy<'T>  
  
// Usage:  
lazy.Create (creator)  
```  
  
#### Parameters  
 `creator`  
 Type: [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md) `-> 'T`  
  
 The function to provide the value when needed.  
  
## Return Value  
 The created [Lazy](../vs140/Control.Lazy--T--Type-Abbreviation--F#-.md) object.  
  
## Remarks  
  
## Example  
 The following code illustrates the use of `Create`.  
  
 [!CODE [FsCoreLib2#11](../CodeSnippet/VS_Snippets_Fsharp/fscorelib2#11)]  
  
 The output is the factorial of 10.  
  
 **3628800**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0  
  
## See Also  
 <xref:System.Lazy`1?qualifyHint=False>   
 [Control.LazyExtensions Module (F#)](../vs140/Control.LazyExtensions-Module--F#-.md)   
 [Lazy Computations (F#)](../vs140/Lazy-Computations--F#-.md)