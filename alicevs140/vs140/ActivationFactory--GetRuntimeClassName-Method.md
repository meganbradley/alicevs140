---
title: "ActivationFactory::GetRuntimeClassName Method"
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
ms.assetid: 74e34f0a-9c51-4b40-89f5-45c6c5886ece
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ActivationFactory::GetRuntimeClassName Method
Gets the runtime class name of the object that the current ActivationFactory instantiates.  
  
## Syntax  
  
```  
STDMETHOD(  
   GetRuntimeClassName  
)(_Out_ HSTRING* runtimeName);  
```  
  
#### Parameters  
 `runtimeName`  
 When this operation completes, a handle to a string that contains the runtime class name of the object that the current ActivationFactory instantiates.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that describes the failure.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ActivationFactory Class](../vs140/ActivationFactory-Class.md)