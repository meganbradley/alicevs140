---
title: "Printf.StringFormat&lt;&#39;T,&#39;Result&gt; Type Abbreviation (F#)"
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
  - Printf.StringFormat<'T,'Result>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d69a911f-3a25-42fa-bd51-a9c9c1102fa8
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Printf.StringFormat&lt;&#39;T,&#39;Result&gt; Type Abbreviation (F#)
Represents a statically-analyzed format when formatting builds a string. The first type parameter indicates the arguments of the format operation and the last the overall return type. This type is a type abbreviation for [Format<'Printer,unit,string,'Result>](../vs140/Core.Format--Printer--State--Residue--Result--Type-Abbreviation--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Printf  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type StringFormat<'T,'Result> = Format<'Printer,unit,string,'Result>  
```  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core.PrintfModule Namespace (F#)](../Topic/Core.Printf%20Module%20\(F%23\).md)   
 [Format<'Printer,'State,'Residue,'Result>](../vs140/Core.Format--Printer--State--Residue--Result--Type-Abbreviation--F#-.md)