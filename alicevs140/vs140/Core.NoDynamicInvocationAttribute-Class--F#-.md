---
title: "Core.NoDynamicInvocationAttribute Class (F#)"
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
  - Core.NoDynamicInvocationAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fceab6c1-2592-43a4-88b4-c294b2082e16
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.NoDynamicInvocationAttribute Class (F#)
This attribute is used to tag values that may not be dynamically invoked at runtime. This is typically added to inline functions whose implementations include unverifiable code. It causes the method body emitted for the inline function to raise an exception if dynamically invoked, rather than including the unverifiable code in the generated assembly.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Method ||| AttributeTargets.Property, AllowMultiple = false)>]  
[<Sealed>]  
type NoDynamicInvocationAttribute =  
 class  
  new NoDynamicInvocationAttribute : unit -> NoDynamicInvocationAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `NoDynamicInvocation`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.NoDynamicInvocationAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)