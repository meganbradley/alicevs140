---
title: "ComPtr::ComPtr Constructor"
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
ms.assetid: eaf70907-beac-458f-a503-2e5e27b0c196
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr::ComPtr Constructor
Intializes a new instance of the ComPtr class. Overloads provide default, copy, move, and conversion constructors.  
  
## Syntax  
  
```  
WRL_NOTHROW ComPtr();  
WRL_NOTHROW ComPtr(  
   decltype(__nullptr)  
);  
template<  
   class U  
>  
WRL_NOTHROW ComPtr(  
   _In_opt_ U *other  
);  
WRL_NOTHROW ComPtr(  
   const ComPtr& other  
);  
template<  
   class U  
>  
WRL_NOTHROW ComPtr(  
   const ComPtr<U> &other,  
   typename ENABLE_IF<__is_convertible_to(U*,  
   T*),  
   void *>;  
WRL_NOTHROW ComPtr(  
   _Inout_ ComPtr &&other  
);  
template<  
   class U  
>  
WRL_NOTHROW ComPtr(  
   _Inout_ ComPtr<U>&& other,  
   typename ENABLE_IF<__is_convertible_to(U*,  
   T*),  
   void *>;  
```  
  
#### Parameters  
 `U`  
 The type of the `other` parameter.  
  
 `other`  
 An object of type `U`.  
  
## Return Value  
  
## Remarks  
 The first constructor is the default constructor, which implictly creates an empty object. The second constructor specifies [__nullptr](../vs140/nullptr---C---Component-Extensions-.md), which explicitly creates an empty object.  
  
 The third constructor creates an object from the object specified by a pointer.  
  
 The fourth and fifth constructors are copy constructors. The fifth constructor copies an object if it is convertible to the current type.  
  
 The sixth and seventh constructors are move constructors. The seventh constructor moves an object if it is convertible to the current type.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ComPtr Class](../vs140/ComPtr-Class.md)