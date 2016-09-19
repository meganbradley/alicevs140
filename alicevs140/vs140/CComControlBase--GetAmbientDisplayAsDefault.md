---
title: "CComControlBase::GetAmbientDisplayAsDefault"
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
ms.assetid: 0712f936-3f15-47d7-9eb1-ee553ab90f54
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientDisplayAsDefault
Retrieves **DISPID_AMBIENT_DISPLAYASDEFAULT**, a flag that is **TRUE** if the container has marked the control in this site to be a default button, and therefore a button control should draw itself with a thicker frame.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientDisplayAsDefault(  
   BOOL& bDisplayAsDefault   
);  
```  
  
#### Parameters  
 `bDisplayAsDefault`  
 The property **DISPID_AMBIENT_DISPLAYASDEFAULT**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)