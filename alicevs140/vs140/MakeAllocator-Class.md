---
title: "MakeAllocator Class"
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
ms.topic: reference
ms.assetid: a1114615-abd7-4a56-9bc3-750c118f0fa1
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MakeAllocator Class
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
  
template<  
   typename T,  
   bool hasWeakReferenceSupport =   
         !__is_base_of(RuntimeClassFlags<InhibitWeakReference>,   
   T)> , T)> class MakeAllocator;  
  
template<  
   typename T  
>  
class MakeAllocator<T, false>;  
  
template<  
   typename T  
>  
class MakeAllocator<T, true>;  
```  
  
#### Parameters  
 `T`  
 A type name.  
  
 `hasWeakReferenceSupport`  
 `true` to allocate memory for an object that supports weak references; `false` to allocate memory for an object that doesn't support weak references.  
  
## Remarks  
 Allocates memory for an activatable class, with or without weak reference support.  
  
 Override the MakeAllocator class to implement a user-defined memory allocation model.  
  
 MakeAllocator is typically used to prevent memory leaks if an object throws during construction.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[MakeAllocator::MakeAllocator Constructor](../vs140/MakeAllocator--MakeAllocator-Constructor.md)|Initializes a new instance of the MakeAllocator class.|  
|[MakeAllocator::~MakeAllocator Destructor](../vs140/MakeAllocator--~MakeAllocator-Destructor.md)|Deinitializes the current instance of the MakeAllocator class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[MakeAllocator::Allocate Method](../vs140/MakeAllocator--Allocate-Method.md)|Allocates memory and associates it with the current MakeAllocator object.|  
|[MakeAllocator::Detach Method](../vs140/MakeAllocator--Detach-Method.md)|Disassociates memory allocated by the [Allocate](../vs140/MakeAllocator--Allocate-Method.md) method from the current MakeAllocator object.|  
  
## Inheritance Hierarchy  
 `MakeAllocator`  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)