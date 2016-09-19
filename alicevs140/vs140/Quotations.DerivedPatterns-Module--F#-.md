---
title: "Quotations.DerivedPatterns Module (F#)"
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
  - Quotations.DerivedPatterns
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d2434a6e-ae7b-4f3d-b567-c162938bc9cd
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Quotations.DerivedPatterns Module (F#)
Contains a set of derived F# active patterns to analyze F# expression objects  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module DerivedPatterns  
```  
  
## Remarks  
  
## Active Patterns  
  
|Active Pattern|Description|  
|--------------------|-----------------|  
|[AndAlso](../vs140/DerivedPatterns.AndAlso-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr) option`|Recognizes expressions of the form `a && b.`|  
|[Applications](../vs140/DerivedPatterns.Applications-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr list list) option`|Recognizes expressions that represent the application of a (possibly curried or tupled) first class function value.|  
|[Bool](../vs140/DerivedPatterns.Bool-Active-Pattern--F#-.md)  `: Expr -> bool option`|Recognizes constant Boolean expressions.|  
|[Byte](../vs140/DerivedPatterns.Byte-Active-Pattern--F#-.md)  `: Expr -> byte option`|Recognizes constant byte expressions.|  
|[Char](../vs140/DerivedPatterns.Char-Active-Pattern--F#-.md)  `: Expr -> char option`|Recognizes constant Unicode character expressions.|  
|[Double](../vs140/DerivedPatterns.Double-Active-Pattern--F#-.md)  `: Expr -> float option`|Recognizes constant 64-bit floating point number expressions.|  
|[Int16](../vs140/DerivedPatterns.Int16-Active-Pattern--F#-.md)  `: Expr -> int16 option`|Recognizes constant int16 expressions.|  
|[Int32](../vs140/DerivedPatterns.Int32-Active-Pattern--F#-.md)  `: Expr -> int32 option`|Recognizes constant int32 expressions.|  
|[Int64](../vs140/DerivedPatterns.Int64-Active-Pattern--F#-.md)  `: Expr -> int64 option`|Recognizes constant int64 expressions.|  
|[Lambdas](../vs140/DerivedPatterns.Lambdas-Active-Pattern--F#-.md)  `: Expr -> (Var list list * Expr) option`|Recognizes expressions that represent a (possibly curried or tupled) first class function value.|  
|[MethodWithReflectedDefinition](../vs140/DerivedPatterns.MethodWithReflectedDefinition-Active-Pattern--F#-.md)  `: MethodBase -> Expr option`|Recognizes methods that have an associated ReflectedDefinition.|  
|[OrElse](../vs140/DerivedPatterns.OrElse-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr) option`|Recognizes expressions of the form `a &#124;&#124; b.`|  
|[PropertyGetterWithReflectedDefinition](../Topic/DerivedPatterns.PropertyGetterWithReflectedDefinition%20Active%20Pattern%20\(F%23\).md)  `: PropertyInfo -> Expr option`|Recognizes property getters or values in modules that have an associated ReflectedDefinition.|  
|[PropertySetterWithReflectedDefinition](../Topic/DerivedPatterns.PropertySetterWithReflectedDefinition%20Active%20Pattern%20\(F%23\).md)  `: PropertyInfo -> Expr option`|Recognizes property setters that have an associated ReflectedDefinition.|  
|[SByte](../vs140/DerivedPatterns.SByte-Active-Pattern--F#-.md)  `: Expr -> sbyte option`|Recognizes constant signed byte expressions.|  
|[Single](../vs140/DerivedPatterns.Single-Active-Pattern--F#-.md)  `: Expr -> single option`|Recognizes constant 32-bit floating point number expressions.|  
|[SpecificCall](../vs140/DerivedPatterns.SpecificCall-Active-Pattern--F#-.md)  `: Expr -> Expr -> (Expr option * Type list * Expr list) option`|A parameterized active pattern to recognize calls to a specified function or method. The returned elements are the optional target object (present if the target is an instance method), the generic type instantiation (non-empty if the target is a generic instantiation), and the arguments to the function or method.|  
|[String](../vs140/DerivedPatterns.String-Active-Pattern--F#-.md)  `: Expr -> string option`|Recognizes constant string expressions.|  
|[UInt16](../vs140/DerivedPatterns.UInt16-Active-Pattern--F#-.md)  `: Expr -> uint16 option`|Recognizes constant unsigned int16 expressions.|  
|[UInt32](../vs140/DerivedPatterns.UInt32-Active-Pattern--F#-.md)  `: Expr -> uint32 option`|Recognizes constant unsigned int32 expressions.|  
|[UInt64](../vs140/DerivedPatterns.UInt64-Active-Pattern--F#-.md)  `: Expr -> uint64 option`|Recognizes constant unsigned int64 expressions.|  
|[Unit](../vs140/DerivedPatterns.Unit-Active-Pattern--F#-.md)  `: Expr -> unit option`|Recognizes `()` constant expressions.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)