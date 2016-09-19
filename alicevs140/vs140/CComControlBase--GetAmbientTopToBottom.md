---
title: "CComControlBase::GetAmbientTopToBottom"
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
ms.assetid: 4050bbfa-8efd-4f67-b732-eeccfc319a9f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientTopToBottom
Retrieves **DISPID_AMBIENT_TOPTOBOTTOM**, the direction in which content is displayed by the container.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientTopToBottom(  
   BOOL& bTopToBottom   
);  
```  
  
#### Parameters  
 *bTopToBottom*  
 The property **DISPID_AMBIENT_TOPTOBOTTOM**. Set to **TRUE** if text is displayed top to bottom, **FALSE** if it is displayed bottom to top.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)