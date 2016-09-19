---
title: "CBindStatusCallback::GetPriority"
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
ms.assetid: 676f30c2-1114-4abb-b8e1-959ef5a71ec1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::GetPriority
Called by the asynchronous moniker to get the priority of the bind operation.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetPriority)(  
   LONG* pnPriority   
);  
```  
  
#### Parameters  
 *pnPriority*  
 [out] Address of the **LONG** variable that, on success, receives the priority.  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)