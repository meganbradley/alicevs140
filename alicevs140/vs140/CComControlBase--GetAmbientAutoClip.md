---
title: "CComControlBase::GetAmbientAutoClip"
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
ms.assetid: 28d5d789-68f2-40c2-8726-ca81be844c47
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientAutoClip
Retrieves **DISPID_AMBIENT_AUTOCLIP**, a flag indicating whether the container supports automatic clipping of the control display area.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientAutoClip(  
   BOOL& bAutoClip   
);   
```  
  
#### Parameters  
 *bAutoClip*  
 The property **DISPID_AMBIENT_AUTOCLIP**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)