---
title: "ComPtrRef::ReleaseAndGetAddressOf Method"
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
ms.assetid: 004aac42-e135-41ce-8d1d-4c5969d55004
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtrRef::ReleaseAndGetAddressOf Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
InterfaceType** ReleaseAndGetAddressOf();  
```  
  
## Return Value  
 Pointer to the interface that was represented by the deleted ComPtrRef object.  
  
## Remarks  
 Deletes the current ComPtrRef object and returns a pointer-to-a-pointer to the interface that was represented by the ComPtrRef object.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [ComPtrRef Class](../vs140/ComPtrRef-Class.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)