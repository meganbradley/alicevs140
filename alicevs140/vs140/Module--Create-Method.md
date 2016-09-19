---
title: "Module::Create Method"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: bfa97fd7-5226-4604-92a5-3b9697053e64
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module::Create Method
Creates an instance of a module.  
  
## Syntax  
  
```  
WRL_NOTHROW static Module& Create();  
template<  
   typename T  
>  
WRL_NOTHROW static Module& Create(  
   T callback  
);  
template<  
   typename T  
>  
WRL_NOTHROW static Module& Create(  
   _In_ T* object,  
   _In_ void (T::* method)()  
);  
```  
  
#### Parameters  
 `T`  
 Module type.  
  
 `callback`  
 Called when the last instance object of the module is released.  
  
 `object`  
 The `object` and `method` parameters are used in combination. Points to the last instance object when the last instance object in the module is released.  
  
 `method`  
 The `object` and `method` parameters are used in combination. Points to the method of the last instance object when the last instance object in the module is released.  
  
## Return Value  
 Reference to the module.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Module Class](../vs140/Module-Class.md)