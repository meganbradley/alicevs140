---
title: "CStockPropImpl::get_Appearance"
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
ms.assetid: 3df25cca-169d-439c-b902-3ac294a431d2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_Appearance
Call this method to get the paint style used by the control, for example, flat or 3D.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Appearance(  
   SHORT pnAppearance  
);  
```  
  
#### Parameters  
 *pnAppearance*  
 Variable that receives the control's paint style.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Appearance](../vs140/CStockPropImpl--put_Appearance.md)