---
title: "RoInitializeWrapper::~RoInitializeWrapper Destructor"
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
ms.assetid: afef4c1f-ffde-4cd2-8654-8de4182eb5f4
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RoInitializeWrapper::~RoInitializeWrapper Destructor
Uninitializes the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```cpp  
~RoInitializeWrapper()  
```  
  
## Remarks  
 The RoInitializeWrapper class invokes Windows::Foundation::Uninitialize().  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [RoInitialize Class](../vs140/HandleT-Class.md)