---
title: "CStockPropImpl::put_BackColor"
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
ms.assetid: 55e24bee-6e29-453a-a3d6-3b1193298b4e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_BackColor
Call this method to set the control's background color.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_BackColor(  
   OLE_COLOR clrBackColor  
);  
```  
  
#### Parameters  
 *clrBackColor*  
 The new control background color.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_BackColor](../vs140/CStockPropImpl--get_BackColor.md)