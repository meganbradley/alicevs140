---
title: "WeakReference::WeakReference Constructor"
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
ms.assetid: 4959a9d7-78ea-423d-a46b-50d010d29fff
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WeakReference::WeakReference Constructor
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
WeakReference();  
```  
  
## Remarks  
 Initializes a new instance of the WeakReference class.  
  
 The strong reference pointer for the WeakReference object is initialized to `nullptr`, and the strong reference count is initialized to 1.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [WeakReference Class](../vs140/WeakReference-Class.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)