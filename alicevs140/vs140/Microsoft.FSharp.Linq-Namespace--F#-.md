---
title: "Microsoft.FSharp.Linq Namespace (F#)"
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
ms.assetid: 4765b4e8-4006-4d8c-a405-39c218b3c82d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Microsoft.FSharp.Linq Namespace (F#)
This namespace includes types that support F# query expressions. This includes functions and operators for working with nullable values frequently encountered when working with databases, and the types that are used to implement the query expressions language feature. For more information, see [Query Expressions (F#)](../Topic/Query%20Expressions%20\(F%23\).md).  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
namespace Microsoft.FSharp.Linq  
```  
  
## Namespaces  
  
|Namespace|Description|  
|---------------|-----------------|  
|namespace Microsoft.FSharp.Linq.QueryRunExtensions|Contains modules and functions that support the F# query syntax.|  
  
## Modules  
  
|Module|Description|  
|------------|-----------------|  
|module [Nullable](../Topic/Linq.Nullable%20Module%20\(F%23\).md)|Functions for converting nullable values.|  
|module [NullableOperators](../vs140/Linq.NullableOperators-Module--F#-.md)|Operators for working with nullable values.|  
  
## Type Definitions  
  
|Type|Description|  
|----------|-----------------|  
|type [QueryBuilder](../Topic/Linq.QueryBuilder%20Class%20\(F%23\).md)|The type used to support the F# query syntax.|  
|type [QuerySource<'T,'Q>](../vs140/Linq.QuerySource--T--Q--Class--F#-.md)|A partial input or result in an F# query.|  
  
## See Also  
 [F# Library Reference](../Topic/F%23%20Core%20Library%20Reference.md)   
 [Nullable Operators (F#)](../Topic/Nullable%20Operators%20\(F%23\).md)