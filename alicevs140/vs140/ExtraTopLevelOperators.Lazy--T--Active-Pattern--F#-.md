---
title: "ExtraTopLevelOperators.Lazy&lt;&#39;T&gt; Active Pattern (F#)"
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
  - ExtraTopLevelOperators.( |Lazy| )<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 5dc8b945-3004-42a4-b2a1-b19bb21836e1
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExtraTopLevelOperators.Lazy&lt;&#39;T&gt; Active Pattern (F#)
An active pattern to force the execution of values of type [Lazy](../vs140/Control.Lazy--T--Type-Abbreviation--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.ExtraTopLevelOperators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |Lazy| ) : Lazy<'T> -> 'T  
```  
  
#### Parameters  
 `input`  
 Type: [Lazy](../vs140/Control.Lazy--T--Type-Abbreviation--F#-.md)`<'T>`  
  
## Return Value  
  
## Remarks  
 This function is named `LazyPattern` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of the `Lazy` active pattern.  
  
 [!CODE [FsCoreLib2#8](../CodeSnippet/VS_Snippets_Fsharp/fscorelib2#8)]  
  
 **Output**  
  
 **10 factorial is 3628800**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.ExtraTopLevelOperators Module (F#)](../Topic/Core.ExtraTopLevelOperators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)