---
title: "__RTDynamicCast"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - __RTDynamicCast
apilocation: 
  - msvcr90.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 56aa2d7a-aa47-46ef-830d-e37175611239
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __RTDynamicCast
Runtime implementation of the [dynamic_cast](../vs140/dynamic_cast-Operator.md) operator.  
  
## Syntax  
  
```cpp  
PVOID __RTDynamicCast (  
   PVOID inptr,   
   LONG VfDelta,  
   PVOID SrcType,  
   PVOID TargetType,   
   BOOL isReference  
   ) throw(...)  
```  
  
#### Parameters  
 `inptr`  
 Pointer to a polymorphic object.  
  
 `VfDelta`  
 Offset of virtual function pointer in object.  
  
 `SrcType`  
 Static type of object pointed to by the `inptr` parameter.  
  
 `TargetType`  
 Intended result of cast.  
  
 `isReference`  
 `true` if input is a reference; `false` if input is a pointer.  
  
## Return Value  
 Pointer to the appropriate sub-object, if successful; otherwise, NULL.  
  
## Exceptions  
 `bad_cast()` if the input to `dynamic_cast<>` is a reference and the cast fails.  
  
## Remarks  
 Converts `inptr` to an object of type `TargetType`. The type of `inptr` must be a pointer if `TargetType` is a pointer, or an l-value if `TargetType` is a reference. `TargetType` must be a pointer or a reference to a previously defined class type, or a pointer to void.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|__RTDynamicCast|rtti.h|