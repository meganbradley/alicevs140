---
title: "Core.FSharpInterfaceDataVersionAttribute Class (F#)"
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
  - Core.FSharpInterfaceDataVersionAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 900505db-8d27-432e-a216-07ec17dc179d
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.FSharpInterfaceDataVersionAttribute Class (F#)
This attribute is added to generated assemblies to indicate the version of the data schema used to encode additional F# specific information in the resource attached to compiled F# libraries.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Assembly, AllowMultiple = false)>]  
[<Sealed>]  
type FSharpInterfaceDataVersionAttribute =  
 class  
  new FSharpInterfaceDataVersionAttribute : int * int * int -> FSharpInterfaceDataVersionAttribute  
  member this.Major :  int  
  member this.Minor :  int  
  member this.Release :  int  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `FSharpInterfaceDataVersion`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.FSharpInterfaceDataVersionAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Major](../vs140/FSharpInterfaceDataVersionAttribute.Major-Property--F#-.md)|The major version number of the F# version associated with the attribute|  
|[Minor](../vs140/FSharpInterfaceDataVersionAttribute.Minor-Property--F#-.md)|The minor version number of the F# version associated with the attribute|  
|[Release](../vs140/FSharpInterfaceDataVersionAttribute.Release-Property--F#-.md)|The release number of the F# version associated with the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)