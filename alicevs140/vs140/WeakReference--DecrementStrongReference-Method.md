---
title: "WeakReference::DecrementStrongReference Method"
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
ms.assetid: 97d70d9f-41b8-4f8d-a6fa-4137cc4f9029
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WeakReference::DecrementStrongReference Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
ULONG DecrementStrongReference();  
```  
  
## Remarks  
 Decrements the strong reference count of the current WeakReference object.  
  
 When the strong reference count becomes zero, the strong reference is set to `nullptr`.  
  
## Return Value  
 The decremented strong reference count.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [WeakReference Class](../vs140/WeakReference-Class.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)