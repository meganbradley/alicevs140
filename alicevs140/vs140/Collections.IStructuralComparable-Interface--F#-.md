---
title: "Collections.IStructuralComparable Interface (F#)"
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
  - Collections.IStructuralComparable
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c963a83d-f9ba-41ec-b61a-4c35c529ccdd
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.IStructuralComparable Interface (F#)
Supports the structural comparison of collection objects.  
  
 **Namespace/Module Path**: System.Collections  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type IStructuralComparable =  
 interface  
  abstract this.CompareTo : obj * IComparer -> int  
 end  
```  
  
## Remarks  
 This type is provided for use only with the F# Core Library Versions that targets .NET Framework 2.0. If you are using .NET Framework 4, use the .NET Framework 4 type with the same name, <xref:System.Collections.IStructuralComparable?qualifyHint=False>.  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[CompareTo](../Topic/IStructuralComparable.CompareTo%20Method%20\(F%23\).md)|Determines whether the current object precedes, occurs in the same position as, or follows another object in the sort order.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0  
  
## See Also  
 [System.Collections Namespace (F#)](../Topic/System.Collections%20Namespace%20\(F%23\).md)