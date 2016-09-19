---
title: "CStockPropImpl::get_BackColor"
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
ms.assetid: 72755bbf-a668-4fd9-89bb-3ea631862617
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_BackColor
Call this method to get the control's background color.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_BackColor(  
   OLE_COLOR * pclrBackColor  
);  
```  
  
#### Parameters  
 *pclrBackColor*  
 Variable that receives the control's background color.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_BackColor](../vs140/CStockPropImpl--put_BackColor.md)