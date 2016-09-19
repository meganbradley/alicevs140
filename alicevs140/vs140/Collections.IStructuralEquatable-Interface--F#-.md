---
title: "Collections.IStructuralEquatable Interface (F#)"
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
  - Collections.IStructuralEquatable
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b8684c3a-2f1e-47b5-ae74-0e4ad75b4ab3
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.IStructuralEquatable Interface (F#)
Defines methods to support the comparison of objects for structural equality.  
  
 **Namespace/Module Path**: System.Collections  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type IStructuralEquatable =  
 interface  
  abstract this.Equals : obj * IEqualityComparer -> bool  
  abstract this.GetHashCode : IEqualityComparer -> int  
 end  
```  
  
## Remarks  
 This type is provided for use only with the F# Core Library Versions that targets .NET Framework 2.0. If you are using .NET Framework 4, use the .NET Framework 4 type with the same name, <xref:System.Collections.IStructuralEquatable?qualifyHint=False>.  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Equals](../vs140/IStructuralEquatable.Equals-Method--F#-.md)|Equality comparison against a target object with a given comparer.|  
|[GetHashCode](../Topic/IStructuralEquatable.GetHashCode%20Method%20\(F%23\).md)|Returns a hash code for the current instance.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0  
  
## See Also  
 [System.Collections Namespace (F#)](../Topic/System.Collections%20Namespace%20\(F%23\).md)