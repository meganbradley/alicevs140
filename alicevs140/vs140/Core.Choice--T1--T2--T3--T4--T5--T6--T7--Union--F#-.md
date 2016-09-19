---
title: "Core.Choice&lt;&#39;T1,&#39;T2,&#39;T3,&#39;T4,&#39;T5,&#39;T6,&#39;T7&gt; Union (F#)"
ms.custom: na
ms.date: 09/18/2016
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
  - Core.Choice<'T1,'T2,'T3,'T4,'T5,'T6,'T7> Union (F#)
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e1aae03b-685c-479f-900c-c4cc6659f286
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.Choice&lt;&#39;T1,&#39;T2,&#39;T3,&#39;T4,&#39;T5,&#39;T6,&#39;T7&gt; Union (F#)
Helper types for active patterns with seven choices.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<StructuralEquality>]  
[<StructuralComparison>]  
type Choice<'T1,'T2,'T3,'T4,'T5,'T6,'T7> =  
| Choice1Of7 of 'T1  
| Choice2Of7 of 'T2  
| Choice3Of7 of 'T3  
| Choice4Of7 of 'T4  
| Choice5Of7 of 'T5  
| Choice6Of7 of 'T6  
| Choice7Of7 of 'T7  
 with  
  interface IStructuralEquatable  
  interface IComparable  
  interface IComparable  
  interface IStructuralComparable  
 end  
```  
  
## Remarks  
  
## Union Cases  
  
|Case|Description|  
|----------|-----------------|  
|Choice1Of7 of 'T1|The first choice.|  
|Choice2Of7 of 'T2|The second choice.|  
|Choice3Of7 of 'T3|The third choice.|  
|Choice4Of7 of 'T4|The fourth choice.|  
|Choice5Of7 of 'T5|The fifth choice.|  
|Choice6Of7 of 'T6|The sixth choice.|  
|Choice7Of7 of 'T7|The seventh choice.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)