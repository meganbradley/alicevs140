---
title: "CComControlBase::GetAmbientUIDead"
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
ms.assetid: c9e6d8e6-ef7b-4a40-b16f-bb6ad11e9129
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientUIDead
Retrieves **DISPID_AMBIENT_UIDEAD**, a flag indicating whether the container wants the control to respond to user-interface actions.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientUIDead(  
   BOOL& bUIDead  
);  
```  
  
#### Parameters  
 *bUIDead*  
 The property **DISPID_AMBIENT_UIDEAD**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 If **TRUE**, the control should not respond. This flag applies regardless of the **DISPID_AMBIENT_USERMODE** flag. See [CComControlBase::GetAmbientUserMode](../vs140/CComControlBase--GetAmbientUserMode.md).  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)