---
title: "LanguagePrimitives.IntrinsicFunctions Module (F#)"
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
  - LanguagePrimitives.IntrinsicFunctions
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1700df47-c8f8-4231-bc57-d7f18dcb14ac
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.IntrinsicFunctions Module (F#)
The F# compiler emits calls to some of the functions in this module as part of the compiled form of some language constructs  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module IntrinsicFunctions  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[CheckThis](../vs140/IntrinsicFunctions.CheckThis--T--Function--F#-.md)|A compiler intrinsic for checking initialization soundness of recursive bindings|  
|[CreateInstance](../vs140/IntrinsicFunctions.CreateInstance--T--Function--F#-.md)|This function implements calls to default constructors acccessed by 'new' constraints.|  
|[Dispose](../vs140/IntrinsicFunctions.Dispose--T--Function--F#-.md)|A compiler intrinsic for the efficient compilation of sequence expressions|  
|[FailInit](../vs140/IntrinsicFunctions.FailInit-Function--F#-.md)|A compiler intrinsic for checking initialization soundness of recursive bindings|  
|[FailStaticInit](../vs140/IntrinsicFunctions.FailStaticInit-Function--F#-.md)|A compiler intrinsic for checking initialization soundness of recursive static bindings|  
|[GetArray](../vs140/IntrinsicFunctions.GetArray--T--Function--F#-.md)|The standard overloaded associative (indexed) lookup operator|  
|[GetArray2D](../vs140/IntrinsicFunctions.GetArray2D--T--Function--F#-.md)|The standard overloaded associative (2-indexed) lookup operator|  
|[GetArray3D](../vs140/IntrinsicFunctions.GetArray3D--T--Function--F#-.md)|The standard overloaded associative (3-indexed) lookup operator|  
|[GetArray4D](../vs140/IntrinsicFunctions.GetArray4D--T--Function--F#-.md)|The standard overloaded associative (4-indexed) lookup operator|  
|[GetString](../vs140/IntrinsicFunctions.GetString-Function--F#-.md)|Primitive used by pattern match compilation|  
|[MakeDecimal](../vs140/IntrinsicFunctions.MakeDecimal-Function--F#-.md)|This function implements parsing of decimal constants|  
|[SetArray](../vs140/IntrinsicFunctions.SetArray--T--Function--F#-.md)|The standard overloaded associative (indexed) mutation operator|  
|[SetArray2D](../vs140/IntrinsicFunctions.SetArray2D--T--Function--F#-.md)|The standard overloaded associative (2-indexed) mutation operator|  
|[SetArray3D](../vs140/IntrinsicFunctions.SetArray3D--T--Function--F#-.md)|The standard overloaded associative (3-indexed) mutation operator|  
|[SetArray4D](../vs140/IntrinsicFunctions.SetArray4D--T--Function--F#-.md)|The standard overloaded associative (4-indexed) mutation operator|  
|[TypeTestFast](../vs140/IntrinsicFunctions.TypeTestFast--T--Function--F#-.md)|A compiler intrinsic that implements the ':?' operator|  
|[TypeTestGeneric](../vs140/IntrinsicFunctions.TypeTestGeneric--T--Function--F#-.md)|A compiler intrinsic that implements the ':?' operator|  
|[UnboxFast](../vs140/IntrinsicFunctions.UnboxFast--T--Function--F#-.md)|A compiler intrinsic that implements the ':?>' operator|  
|[UnboxGeneric](../vs140/IntrinsicFunctions.UnboxGeneric--T--Function--F#-.md)|A compiler intrinsic that implements the ':?>' operator|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core.LanguagePrimitives Namespace (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)