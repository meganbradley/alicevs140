---
title: "CComControlBase::GetAmbientLocaleID"
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
ms.assetid: 7dc7afb7-dcce-4e37-8edd-e3b80b3fce23
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientLocaleID
Retrieves **DISPID_AMBIENT_LOCALEID**, the identifier of the language used by the container.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientLocaleID(  
   LCID& lcid   
);  
```  
  
#### Parameters  
 `lcid`  
 The property **DISPID_AMBIENT_LOCALEID**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 The control can use this identifier to adapt its user interface to different languages.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)