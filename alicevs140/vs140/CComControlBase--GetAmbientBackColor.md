---
title: "CComControlBase::GetAmbientBackColor"
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
ms.assetid: b197d89e-06be-4bde-b742-514ec030b648
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientBackColor
Retrieves **DISPID_AMBIENT_BACKCOLOR**, the ambient background color for all controls, defined by the container.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientBackColor(  
   OLE_COLOR& BackColor   
);  
```  
  
#### Parameters  
 *BackColor*  
 The property **DISPID_AMBIENT_BACKCOLOR**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)