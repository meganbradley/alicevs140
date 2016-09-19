---
title: "Operators.Unchecked Module (F#)"
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
  - Operators.Unchecked
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 4489ee14-8fae-42af-96b2-51b6c94b5c47
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.Unchecked Module (F#)
This module contains basic operations which do not apply runtime and/or static checks.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Unchecked  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[compare](../vs140/Unchecked.compare--T--Function--F#-.md)  `: 'T -> 'T -> int`|Perform generic comparison on two values where the type of the values is not statically required to have the comparison constraint.|  
|[defaultof](../vs140/Unchecked.defaultof--T--Type-Function--F#-.md)  `: 'T`|Generate a default value for any type. This is null for reference types, For structures, this is structure value where all fields have the default value. This function is unsafe in the sense that some F# values do not have proper `null` values.|  
|[equals](../vs140/Unchecked.equals--T--Function--F#-.md)  `: 'T -> 'T -> bool`|Perform generic equality on two values where the type of the values is not statically required to satisfy the equality constraint.|  
|[hash](../vs140/Unchecked.hash--T--Function--F#-.md)  `: 'T -> int`|Perform generic hashing on a value where the type of the value is not statically required to satisfy the equality constraint.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)