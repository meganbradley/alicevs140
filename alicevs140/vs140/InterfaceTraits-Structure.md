---
title: "InterfaceTraits Structure"
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
ms.assetid: ede0c284-19a7-4892-9738-ff3da4923d0a
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InterfaceTraits Structure
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template<  
   typename I0  
>  
struct __declspec(novtable) InterfaceTraits;  
template<  
   typename CloakedType  
>  
struct __declspec(novtable) InterfaceTraits<CloakedIid<CloakedType>>;  
  
template<>  
struct __declspec(novtable) InterfaceTraits<Nil>;  
```  
  
#### Parameters  
 `I0`  
 The name of an interface.  
  
 `CloakedType`  
 For RuntimeClass, Implements and ChainInterfaces, an interface that won't be in the list of supported interface IDs.  
  
## Remarks  
 Implements common characteristics of an interface.  
  
 The second template is a specialization for cloaked interfaces. The third template is a specialization for Nil parameters.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`Base`|A synonym for the `I0` template parameter.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[InterfaceTraits::CanCastTo Method](../vs140/InterfaceTraits--CanCastTo-Method.md)|Indicates whether the specified pointer can be cast to a pointer to `Base`.|  
|[InterfaceTraits::CastToBase Method](../vs140/InterfaceTraits--CastToBase-Method.md)|Casts the specified pointer to a pointer to `Base`.|  
|[InterfaceTraits::CastToUnknown Method](../vs140/InterfaceTraits--CastToUnknown-Method.md)|Casts the specified pointer to a pointer to IUnknown.|  
|[InterfaceTraits::FillArrayWithIid Method](../vs140/InterfaceTraits--FillArrayWithIid-Method.md)|Assigns the interface ID of `Base` to the array element specified by the index argument.|  
|[InterfaceTraits::Verify Method](../vs140/InterfaceTraits--Verify-Method.md)|Verifies that Base is properly derived.|  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|[InterfaceTraits::IidCount Constant](../vs140/InterfaceTraits--IidCount-Constant.md)|Holds the number of interface IDs associated with the current InterfaceTraits object.|  
  
## Inheritance Hierarchy  
 `InterfaceTraits`  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)