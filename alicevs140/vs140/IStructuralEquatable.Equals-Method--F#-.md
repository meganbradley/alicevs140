---
title: "IStructuralEquatable.Equals Method (F#)"
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
  - IStructuralEquatable.Equals
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d8d24d5c-1a02-49e7-ad4d-4c38b92aa670
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IStructuralEquatable.Equals Method (F#)
Equality comparison against a target object with a given comparer.  
  
 **Namespace/Module Path**: System.Collections  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
abstract this.Equals : obj * IEqualityComparer -> bool  
  
// Usage:  
iStructuralEquatable.Equals (obj, comparer)  
```  
  
#### Parameters  
 `obj`  
 Type: [obj](../Topic/Core.obj%20Type%20Abbreviation%20\(F%23\).md)  
  
 The target for comparison.  
  
 `comparer`  
 Type: <xref:System.Collections.IEqualityComparer?qualifyHint=False>  
  
 Compares the two objects.  
  
## Return Value  
 The result of the comparer.  
  
## Remarks  
 This API is provided for use only with the F# Core Library Versions that targets .NET Framework 2.0. If you are using .NET Framework 4, use the .NET Framework 4 API with the same name, <xref:System.Collections.IStructuralEquatable.Equals?qualifyHint=False>.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0  
  
## See Also  
 [Collections.IStructuralEquatable Interface (F#)](../vs140/Collections.IStructuralEquatable-Interface--F#-.md)   
 [System.Collections Namespace (F#)](../Topic/System.Collections%20Namespace%20\(F%23\).md)