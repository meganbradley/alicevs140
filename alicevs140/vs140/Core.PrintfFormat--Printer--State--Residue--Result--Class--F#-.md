---
title: "Core.PrintfFormat&lt;&#39;Printer,&#39;State,&#39;Residue,&#39;Result&gt; Class (F#)"
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
  - Core.PrintfFormat<'Printer,'State,'Residue,'Result>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 60c973f2-afb2-44ca-8331-3758a5f96467
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.PrintfFormat&lt;&#39;Printer,&#39;State,&#39;Residue,&#39;Result&gt; Class (F#)
Type of a formatting expression.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type PrintfFormat<'Printer,'State,'Residue,'Result> =  
 class  
  new PrintfFormat : string -> PrintfFormat<'Printer,'State,'Residue,'Result>  
  member this.Value :  string  
 end  
```  
  
## Remarks  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.PrintfFormat--Printer--State--Residue--Result--Constructor--F#-.md)|Construct a format string|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Value](../vs140/PrintfFormat.Value--Printer--State--Residue--Result--Property--F#-.md)|The raw text of the format string.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)