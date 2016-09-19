---
title: "CStockPropImpl::put_ForeColor"
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
ms.assetid: 099aaeb0-40a3-4306-bb13-d2841e06251b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_ForeColor
Call this method to set the control's foreground color.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_ForeColor(  
   OLE_COLOR clrForeColor  
);  
```  
  
#### Parameters  
 *clrForeColor*  
 The new foreground color of the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_ForeColor](../vs140/CStockPropImpl--get_ForeColor.md)