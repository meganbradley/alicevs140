---
title: "CStockPropImpl::get_ForeColor"
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
ms.assetid: 92f9b8e9-4fc3-410f-81ba-70473a616055
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_ForeColor
Call this method to get the control's foreground color.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_ForeColor(  
   OLE_COLOR * pclrForeColor  
);  
```  
  
#### Parameters  
 *pclrForeColor*  
 Variable that receives the controls foreground color.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_ForeColor](../vs140/CStockPropImpl--put_ForeColor.md)