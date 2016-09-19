---
title: "CBindStatusCallback::OnLowResource"
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
ms.assetid: e709a86d-74f5-4ca1-b83b-60d3780dbb17
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::OnLowResource
Called when resources are low.  
  
## Syntax  
  
```  
  
      STDMETHOD(OnLowResource)(  
   DWORD /* dwReserved */  
);  
```  
  
#### Parameters  
 `dwReserved`  
 Reserved.  
  
## Return Value  
 Returns `S_OK`.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)