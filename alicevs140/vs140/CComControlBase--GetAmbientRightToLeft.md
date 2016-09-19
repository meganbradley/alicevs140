---
title: "CComControlBase::GetAmbientRightToLeft"
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
ms.assetid: 836130d9-9573-47a6-8317-9417c059caa9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientRightToLeft
Retrieves **DISPID_AMBIENT_RIGHTTOLEFT**, the direction in which content is displayed by the container.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientRightToLeft(  
   BOOL& bRightToLeft   
);  
```  
  
#### Parameters  
 *bRightToLeft*  
 The property **DISPID_AMBIENT_RIGHTTOLEFT**. Set to **TRUE** if content is displayed right to left, **FALSE** if it is displayed left to right.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)