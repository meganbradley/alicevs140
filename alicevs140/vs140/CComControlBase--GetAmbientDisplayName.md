---
title: "CComControlBase::GetAmbientDisplayName"
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
ms.assetid: dd17e53a-95db-4972-b890-00db6781d1ff
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientDisplayName
Retrieves **DISPID_AMBIENT_DISPLAYNAME**, the name the container has supplied to the control.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientDisplayName(  
   BSTR& bstrDisplayName   
);   
```  
  
#### Parameters  
 *bstrDisplayName*  
 The property **DISPID_AMBIENT_DISPLAYNAME**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)