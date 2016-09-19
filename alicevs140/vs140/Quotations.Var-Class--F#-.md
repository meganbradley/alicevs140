---
title: "Quotations.Var Class (F#)"
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
  - Quotations.FSharpVar
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2b1237f9-d897-4bcf-872a-4a297db3f7b5
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Quotations.Var Class (F#)
Represents information at the binding site of a variable.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<Sealed>]  
type Var =  
 class  
  interface IComparable  
  new Var : string * Type * bool option -> Var  
  static member Global : string * Type -> Var  
  member this.IsMutable :  bool  
  member this.Name :  string  
  member this.Type :  Type  
 end  
```  
  
## Remarks  
 This type is named `FSharpVar` in compiled assemblies. If you are accessing the type from a language other than F#, or through reflection, use this name.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../Topic/Quotations.Var%20Constructor%20\(F%23\).md)|Creates a new variable with the given name, type and mutability|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[IsMutable](../vs140/Var.IsMutable-Property--F#-.md)|Indicates if the variable represents a mutable storage location|  
|[Name](../vs140/Var.Name-Property--F#-.md)|The declared name of the variable|  
|[Type](../Topic/Var.Type%20Property%20\(F%23\).md)|The type associated with the variable|  
  
## Static Members  
  
|Member|Description|  
|------------|-----------------|  
|[Global](../vs140/Var.Global-Method--F#-.md)|Fetches or creates a new variable with the given name and type from a global pool of shared variables indexed by name and type.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)