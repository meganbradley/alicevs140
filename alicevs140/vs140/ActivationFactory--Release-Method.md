---
title: "ActivationFactory::Release Method"
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
ms.assetid: 5bc25ff0-ee3c-4a2d-a9b6-2d8f158033ad
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ActivationFactory::Release Method
Decrements the reference count of the current ActivationFactory object.  
  
## Syntax  
  
```  
STDMETHOD_(  
   ULONG,  
   Release  
)();  
```  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that describes the failure.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ActivationFactory Class](../vs140/ActivationFactory-Class.md)