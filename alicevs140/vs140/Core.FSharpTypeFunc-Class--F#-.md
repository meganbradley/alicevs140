---
title: "Core.FSharpTypeFunc Class (F#)"
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
  - Core.FSharpTypeFunc
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 695a5ba3-d499-464a-9ccd-85bb3e5573dc
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.FSharpTypeFunc Class (F#)
The .NET Framework type used to represent F# first-class type function values. This type is for use by compiled F# code.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AbstractClass>]  
type FSharpTypeFunc =  
 class  
  new FSharpTypeFunc : unit -> FSharpTypeFunc  
  abstract this.Specialize : unit -> obj  
 end  
```  
  
## Remarks  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.FSharpTypeFunc-Constructor--F#-.md)|Construct an instance of an F# first class type function value|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Specialize](../vs140/FSharpTypeFunc.Specialize--T--Method--F#-.md)|Specialize the type function at a given type|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)