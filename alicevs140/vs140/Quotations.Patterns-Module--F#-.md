---
title: "Quotations.Patterns Module (F#)"
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
  - Quotations.Patterns
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 093944a9-c752-403a-8983-5fcd5dbf92a4
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Quotations.Patterns Module (F#)
Contains a set of primitive F# active patterns to analyze F# expression objects.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Patterns  
```  
  
## Remarks  
  
## Active Patterns  
  
|Active Pattern|Description|  
|--------------------|-----------------|  
|[AddressOf](../vs140/Patterns.AddressOf-Active-Pattern--F#-.md)  `: Expr -> Expr option`|Recognizes expressions that represent getting the address of a value.|  
|[AddressSet](../vs140/Patterns.AddressSet-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr) option`|Recognizes expressions that represent setting the value held at an address .|  
|[Application](../vs140/Patterns.Application-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr) option`|Recognizes expressions that represent applications of first class function values.|  
|[Call](../vs140/Patterns.Call-Active-Pattern--F#-.md)  `: Expr -> (Expr option * MethodInfo * Expr list) option`|Recognizes expressions that represent calls to static and instance methods, and functions defined in modules.|  
|[Coerce](../Topic/Patterns.Coerce%20Active%20Pattern%20\(F%23\).md)  `: Expr -> (Expr * Type) option`|Recognizes expressions that represent coercions from one type to another.|  
|[DefaultValue](../vs140/Patterns.DefaultValue-Active-Pattern--F#-.md)  `: Expr -> Type option`|Recognizes expressions that represent invocations of a default constructor of a structure.|  
|[FieldGet](../vs140/Patterns.FieldGet-Active-Pattern--F#-.md)  `: Expr -> (Expr option * FieldInfo)`|Recognizes expressions that represent getting a static or instance field.|  
|[FieldSet](../Topic/Patterns.FieldSet%20Active%20Pattern%20\(F%23\).md)  `: Expr -> (Expr option * FieldInfo * Expr) option`|Recognizes expressions that represent setting a static or instance field.|  
|[ForIntegerRangeLoop](../vs140/Patterns.ForIntegerRangeLoop-Active-Pattern--F#-.md)  `: Expr -> (Var * Expr * Expr * Expr) option`|Recognizes expressions that represent loops over integer ranges.|  
|[IfThenElse](../vs140/Patterns.IfThenElse-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr * Expr) option`|Recognizes expressions that represent conditionals.|  
|[Lambda](../vs140/Patterns.Lambda-Active-Pattern--F#-.md)  `: Expr -> (Var * Expr) option`|Recognizes expressions that represent first class function values.|  
|[LetRecursive](../vs140/Patterns.LetRecursive-Active-Pattern--F#-.md)  `: Expr -> ((Var * Expr) list * Expr) option`|Recognizes expressions that represent recursive let bindings of one or more variables.|  
|[Let](../vs140/Patterns.Let-Active-Pattern--F#-.md)  `: Expr -> (Var * Expr * Expr) option`|Recognizes expressions that represent let bindings.|  
|[NewArray](../vs140/Patterns.NewArray-Active-Pattern--F#-.md)  `: Expr -> (Type * Expr list) option`|Recognizes expressions that represent the construction of arrays.|  
|[NewDelegate](../Topic/Patterns.NewDelegate%20Active%20Pattern%20\(F%23\).md)  `: Expr -> (Type * Var list * Expr) option`|Recognizes expressions that represent construction of delegate values.|  
|[NewObject](../Topic/Patterns.NewObject%20Active%20Pattern%20\(F%23\).md)  `: Expr -> (ConstructorInfo * Expr list) option`|Recognizes expressions that represent invocation of object constructors.|  
|[NewRecord](../vs140/Patterns.NewRecord-Active-Pattern--F#-.md)  `: Expr -> (Type * Expr list) option`|Recognizes expressions that represent construction of record values.|  
|[NewTuple](../vs140/Patterns.NewTuple-Active-Pattern--F#-.md)  `: Expr -> (Expr list) option`|Recognizes expressions that represent construction of tuple values.|  
|[NewUnionCase](../vs140/Patterns.NewUnionCase-Active-Pattern--F#-.md)  `: Expr -> (UnionCaseInfo * Expr list) option`|Recognizes expressions that represent construction of particular union case values.|  
|[PropertyGet](../vs140/Patterns.PropertyGet-Active-Pattern--F#-.md)  `: Expr -> (Expr option * PropertyInfo * Expr list) option`|Recognizes expressions that represent the read of a static or instance property, or a non-function value declared in a module.|  
|[PropertySet](../vs140/Patterns.PropertySet-Active-Pattern--F#-.md)  `: Expr -> (Expr option * PropertyInfo * Expr list * Expr) option`|Recognizes expressions that represent setting a static or instance property, or a non-function value declared in a module.|  
|[Quote](../vs140/Patterns.Quote-Active-Pattern--F#-.md)  `: Expr -> Expr option`|Recognizes expressions that represent a nested quotation literal.|  
|[Sequential](../vs140/Patterns.Sequential-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr) option`|Recognizes expressions that represent sequential execution of one expression followed by another.|  
|[TryFinally](../vs140/Patterns.TryFinally-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr) option`|Recognizes expressions that represent a `try...finally` construct.|  
|[TryWith](../vs140/Patterns.TryWith-Active-Pattern--F#-.md)  `: Expr -> (Expr * Var * Expr * Var * Expr) option`|Recognizes expressions that represent a `try...with` construct for exception filtering and catching.|  
|[TupleGet](../vs140/Patterns.TupleGet-Active-Pattern--F#-.md)  `: Expr -> (Expr * int) option`|Recognizes expressions that represent getting a tuple field.|  
|[TypeTest](../Topic/Patterns.TypeTest%20Active%20Pattern%20\(F%23\).md)  `: Expr -> (Expr * Type) option`|Recognizes expressions that represent a dynamic type test.|  
|[UnionCaseTest](../vs140/Patterns.UnionCaseTest-Active-Pattern--F#-.md)  `: Expr -> (Expr * UnionCaseInfo) option`|Recognizes expressions that represent a test if a value is of a particular union case.|  
|[Value](../Topic/Patterns.Value%20Active%20Pattern%20\(F%23\).md)  `: Expr -> (obj * Type) option`|Recognizes expressions that represent a constant value.|  
|[VarSet](../vs140/Patterns.VarSet-Active-Pattern--F#-.md)  `: Expr -> (Var * Expr) option`|Recognizes expressions that represent setting a mutable variable.|  
|[Var](../vs140/Patterns.Var-Active-Pattern--F#-.md)  `: Expr -> Var option`|Recognizes expressions that represent a variable.|  
|[WhileLoop](../vs140/Patterns.WhileLoop-Active-Pattern--F#-.md)  `: Expr -> (Expr * Expr) option`|Recognizes expressions that represent while loops.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)