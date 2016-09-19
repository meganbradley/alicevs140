---
title: "RemoveIUnknown Class"
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
ms.assetid: 998e711a-7d1a-44c6-a016-e6167aa40863
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RemoveIUnknown Class
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template <  
   typename T  
>  
struct RemoveIUnknown;  
  
template <  
   typename T  
>  
class RemoveIUnknown : public T;  
```  
  
#### Parameters  
 `T`  
 A class.  
  
## Remarks  
 Makes a type that is equivalent to an `IUnknown`-based type, but has  nonvirtual `QueryInterface`, `AddRef`, and `Release` member functions.  
  
 By default, COM methods provide virtual `QueryInterface`, `AddRef`, and Release methods. However, `ComPtr` doesn't require the overhead of virtual methods. `RemoveIUnknown` eliminates that overhead by providing private, nonvirtual `QueryInterface`, `AddRef`, and `Release` methods.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`ReturnType`|A synonym for a type that is equivalent to template parameter `T` but has nonvirtual IUnknown members.|  
  
## Inheritance Hierarchy  
 `T`  
  
 `RemoveIUnknown`  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)