---
title: "Option.get&lt;&#39;T&gt; Function (F#)"
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
  - Option.get<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 803e9fcb-6edd-4910-808c-25f08cbc55ea
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option.get&lt;&#39;T&gt; Function (F#)
Gets the value associated with the option.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Option  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
get : 'T option -> 'T  
  
// Usage:  
get option  
```  
  
#### Parameters  
 `option`  
 Type: `'T`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The input option.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the option is None.|  
  
## Return Value  
 The value within the option.  
  
## Remarks  
 This function is named `GetValue` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Option.get`.  
  
 [!CODE [FsOptions#7](../CodeSnippet/VS_Snippets_Fsharp/fsoptions#7)]  
  
 **Output**  
  
 **1"xyz"1.0**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Option Module (F#)](../vs140/Core.Option-Module--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)