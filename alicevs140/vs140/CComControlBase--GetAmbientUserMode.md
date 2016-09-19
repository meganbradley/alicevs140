---
title: "CComControlBase::GetAmbientUserMode"
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
ms.assetid: 8cc820e3-5b78-4a25-a345-39350e99ea68
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientUserMode
Retrieves **DISPID_AMBIENT_USERMODE**, a flag indicating whether the container is in run-mode (**TRUE**) or design-mode (**FALSE**).  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientUserMode(  
   BOOL& bUserMode  
);  
```  
  
#### Parameters  
 `bUserMode`  
 The property **DISPID_AMBIENT_USERMODE**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)