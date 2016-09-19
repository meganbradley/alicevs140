---
title: "CComAggObject::CComAggObject"
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
ms.assetid: 01c3288f-62ba-428b-9666-39c9c6c60fc1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAggObject::CComAggObject
The constructor.  
  
## Syntax  
  
```  
  
      CComAggObject(  
   void* pv   
);  
```  
  
#### Parameters  
 `pv`  
 [in] The outer unknown.  
  
## Remarks  
 Initializes the `CComContainedObject` member, [m_contained](../vs140/CComAggObject--m_contained.md), and increments the module lock count.  
  
 The destructor decrements the module lock count.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComAggObject Class](../vs140/CComAggObject-Class.md)   
 [CComAggObject::FinalConstruct](../vs140/CComAggObject--FinalConstruct.md)   
 [CComAggObject::FinalRelease](../vs140/CComAggObject--FinalRelease.md)