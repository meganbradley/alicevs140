---
title: "RuntimeClass::AddRef Method"
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
ms.assetid: 9c705749-680b-4308-bbec-5b601e8e7dbd
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RuntimeClass::AddRef Method
Increments the reference count for the current RuntimeClass object.  
  
## Syntax  
  
```  
STDMETHOD_(  
   ULONG,  
   AddRef  
)();  
```  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that indicates the error.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [RuntimeClass Class](../vs140/RuntimeClass-Class.md)