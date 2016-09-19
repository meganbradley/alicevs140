---
title: "RoInitializeWrapper::RoInitializeWrapper Constructor"
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
ms.assetid: c6f7fb07-14af-4574-9135-cea164607f30
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RoInitializeWrapper::RoInitializeWrapper Constructor
Initializes a new instance of the RoInitializeWrapper class.  
  
## Syntax  
  
```cpp  
RoInitializeWrapper(   RO_INIT_TYPE flags)  
```  
  
#### Parameters  
 `flags`  
 One of the RO_INIT_TYPE enumerations, which specifies the support provided by the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Remarks  
 The RoInitializeWrapper class invokes Windows::Foundation::Initialize(*flags*).  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [RoInitialize Class](../vs140/HandleT-Class.md)