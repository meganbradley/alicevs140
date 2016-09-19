---
title: "CComContainedObject::CComContainedObject"
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
ms.assetid: 5a007860-4b8f-49ea-8c77-dea5610b197a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComContainedObject::CComContainedObject
The constructor.  
  
## Syntax  
  
```  
  
      CComContainedObject(  
   void* pv   
);  
```  
  
#### Parameters  
 `pv`  
 [in] The owner object's **IUnknown**.  
  
## Remarks  
 Sets the `m_pOuterUnknown` member pointer (inherited through the `Base` class) to `pv`.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComContainedObject Class](../vs140/CComContainedObject-Class.md)   
 [CComObjectRootEx::m_pOuterUnknown](../vs140/CComObjectRootEx--m_pOuterUnknown.md)