---
title: "ClassFactory Class"
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
ms.assetid: f13e6bce-722b-4f18-b7cf-3ffa6345c1db
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ClassFactory Class
Implements the basic functionality of the IClassFactory interface.  
  
## Syntax  
  
```  
template <  
   typename I0 = Details::Nil,  
   typename I1 = Details::Nil,  
   typename I2 = Details::Nil  
>  
class ClassFactory : public Details::RuntimeClass<  
   typename Details::InterfaceListHelper<IClassFactory,   
   I0,   
   I1,   
   I2,   
   Details::Nil>::TypeT,   
   RuntimeClassFlags<ClassicCom | InhibitWeakReference>,   
      false>;  
```  
  
#### Parameters  
 `I0`  
 The zeroth interface.  
  
 `I1`  
 The first interface.  
  
 `I2`  
 The second interface.  
  
## Remarks  
 Utilize `ClassFactory` to provide a user-defined factory implementation.  
  
 The following programming pattern demonstrates how to use the [Implements](../vs140/Implements-Structure.md) structure to specify more than three interfaces on a class factory.  
  
 `struct MyFactory : ClassFactory<Implements<I1, I2, I3>, I4, I5>`  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[ClassFactory::ClassFactory Constructor](../vs140/ClassFactory--ClassFactory-Constructor.md)||  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ClassFactory::AddRef Method](../vs140/ClassFactory--AddRef-Method.md)|Increments the reference count for the current ClassFactory object.|  
|[ClassFactory::LockServer Method](../vs140/ClassFactory--LockServer-Method.md)|Increments or decrements the number of underlying objects that are tracked by the current ClassFactory object.|  
|[ClassFactory::QueryInterface Method](../vs140/ClassFactory--QueryInterface-Method.md)|Retrieves a pointer to the interface specified by parameter.|  
|[ClassFactory::Release Method](../vs140/ClassFactory--Release-Method.md)|Decrements the reference count for the current ClassFactory object.|  
  
## Inheritance Hierarchy  
 `I0`  
  
 `ChainInterfaces`  
  
 `I0`  
  
 `RuntimeClassBase`  
  
 `ImplementsHelper`  
  
 `DontUseNewUseMake`  
  
 `RuntimeClassFlags`  
  
 `RuntimeClassBaseT`  
  
 `RuntimeClass`  
  
 `ClassFactory`  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)   
 [RuntimeClassType Enumeration](../vs140/RuntimeClassType-Enumeration.md)