---
title: "accelerator::get_device_path Method"
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
ms.assetid: 92a9351b-818d-418e-8c82-01834ce0e49a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator::get_device_path Method
Returns the path of the accelerator. The path is unique on the system.  
  
## Syntax  
  
```  
std::wstring get_device_path() const;  
```  
  
## Return Value  
 The system-wide unique device instance path.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator Class](../vs140/accelerator-Class.md)