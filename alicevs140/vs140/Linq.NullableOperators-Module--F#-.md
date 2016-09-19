---
title: "Linq.NullableOperators Module (F#)"
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
ms.assetid: 2c3633c5-3f31-4d62-a9f8-272ad6b19007
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linq.NullableOperators Module (F#)
Operators for working with nullable values.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AutoOpen>]  
module NullableOperators  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[( %? )](../Topic/NullableOperators.\(%20%25?%20\)%3C%5ET1,%5ET2,%5ET3%3E%20Function%20\(F%23\).md)|The modulus operator where a nullable value appears on the right.|  
|[( *? )](../vs140/NullableOperators.-------^T1-^T2-^T3--Function--F#-.md)|The multiplication operator where a nullable value appears on the right.|  
|[( +? )](../vs140/NullableOperators.-------^T1-^T2-^T3--Function--F#-.md)|The addition operator where a nullable value appears on the right.|  
|[( -? )](../Topic/NullableOperators.\(%20-?%20\)%3C%5ET1,%5ET2,%5ET3%3E%20Function%20\(F%23\)1.md)|The subtraction operator where a nullable value appears on the right.|  
|[( /? )](../vs140/NullableOperators.-------^T1-^T2-^T3--Function--F#-2.md)|The division operator where a nullable value appears on the right.|  
|[( <=? )](../Topic/NullableOperators.\(%20%3C=?%20\)%3C'T%3E%20Function%20\(F%23\).md)|The `<=` operator where a nullable value appears on the right.|  
|[( <>? )](../vs140/NullableOperators.---------T--Function--F#-.md)|The `<>` operator where a nullable value appears on the right.|  
|[( <? )](../vs140/NullableOperators.--------T--Function--F#-.md)|The `<` operator where a nullable value appears on the right.|  
|[( =? )](../vs140/NullableOperators.--=-----T--Function--F#-.md)|The `=` operator where a nullable value appears on the right.|  
|[( >=? )](../Topic/NullableOperators.\(%20%3E=?%20\)%3C'T%3E%20Function%20\(F%23\).md)|The `>=` operator where a nullable value appears on the right.|  
|[( >? )](../vs140/NullableOperators.--------T--Function--F#-.md)|The '>' operator where a nullable value appears on the right.|  
|[( ?% )](../vs140/NullableOperators.------^T1-^T2-^T3--Function--F#-.md)|The modulus operator where a nullable value appears on the left.|  
|[( ?%? )](../Topic/NullableOperators.\(%20?%25%20?\)%3C%5ET1,%5ET2,%5ET3%3E%20Function%20\(F%23\).md)|The modulus operator where a nullable value appears on both left and right sides.|  
|[( ?* )](../vs140/NullableOperators.-------^T1-^T2-^T3--Function--F#-.md)|The multiplication operator where a nullable value appears on the left.|  
|[( ?*? )](../Topic/NullableOperators.\(%20?*?%20\)%3C%5ET1,%5ET2,%5ET3%3E%20Function%20\(F%23\).md)|The multiplication operator where a nullable value appears on both left and right sides.|  
|[( ?+ )](../Topic/NullableOperators.\(%20?+%20\)%3C%5ET1,%5ET2,%5ET3%3E%20Function%20\(F%23\).md)|The addition operator where a nullable value appears on the left.|  
|[( ?+? )](../vs140/NullableOperators.--------^T1-^T2-^T3--Function--F#-.md)|The addition operator where a nullable value appears on both left and right sides.|  
|[( ?- )](../vs140/NullableOperators.-------^T1-^T2-^T3--Function--F#-1.md)|The subtraction operator where a nullable value appears on the left.|  
|[( ?-? )](../Topic/NullableOperators.\(%20?-?%20\)%3C%5ET1,%5ET2,%5ET3%3E%20Function%20\(F%23\)1.md)|The subtraction operator where a nullable value appears on both left and right sides .|  
|[( ?/ )](../Topic/NullableOperators.\(%20?-%20\)%3C%5ET1,%5ET2,%5ET3%3E%20Function%20\(F%23\)2.md)|The division operator where a nullable value appears on the left.|  
|[( ?/? )](../vs140/NullableOperators.--------^T1-^T2-^T3--Function--F#-2.md)|The division operator where a nullable value appears on both left and right sides.|  
|[( ?< )](../vs140/NullableOperators.--------T--Function--F#-.md)|The `<` operator where a nullable value appears on the left.|  
|[( ?<= )](../vs140/NullableOperators.----=----T--Function--F#-.md)|The `<=` operator where a nullable value appears on the left.|  
|[( ?<=? )](../vs140/NullableOperators.----=-----T--Function--F#-.md)|The `<=` operator where a nullable value appears on both left and right sides.|  
|[( ?<> )](../vs140/NullableOperators.---------T--Function--F#-.md)|The `<>` operator where a nullable value appears on the left.|  
|[( ?<>? )](../vs140/NullableOperators.----------T--Function--F#-.md)|The `<>` operator where a nullable value appears on both left and right sides.|  
|[( ?<? )](../vs140/NullableOperators.---------T--Function--F#-.md)|The `<` operator where a nullable value appears on both left and right sides.|  
|[( ?= )](../vs140/NullableOperators.---=----T--Function--F#-.md)|The `=` operator where a nullable value appears on the left.|  
|[( ?=? )](../vs140/NullableOperators.---=-----T--Function--F#-.md)|The `=` operator where a nullable value appears on both left and right sides.|  
|[( ?> )](../vs140/NullableOperators.--------T--Function--F#-.md)|The `>` operator where a nullable value appears on the left.|  
|[( ?>= )](../vs140/NullableOperators.----=----T--Function--F#-.md)|The `>=` operator where a nullable value appears on the left.|  
|[( ?>=? )](../vs140/NullableOperators.----=-----T--Function--F#-.md)|The `>=` operator where a nullable value appears on both left and right sides.|  
|[( ?>? )](../vs140/NullableOperators.---------T--Function--F#-.md)|The `>` operator where a nullable value appears on both left and right sides.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)