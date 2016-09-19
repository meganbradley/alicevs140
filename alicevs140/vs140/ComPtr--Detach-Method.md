---
title: "ComPtr::Detach Method"
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
ms.assetid: b9016775-1ade-4581-be1f-0d6f9c2ca658
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr::Detach Method
Disassociates this `ComPtr` object from the interface that it represents.  
  
## Syntax  
  
```  
T* Detach();  
```  
  
## Return Value  
 A pointer to the interface that was represented by this `ComPtr` object.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ComPtr Class](../vs140/ComPtr-Class.md)