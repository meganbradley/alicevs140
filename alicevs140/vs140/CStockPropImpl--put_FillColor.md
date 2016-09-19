---
title: "CStockPropImpl::put_FillColor"
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
ms.assetid: bd5f48da-b207-481d-8a56-ef621d19f834
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_FillColor
Call this method to set the control's fill color.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_FillColor(   
   OLE_COLOR clrFillColor  
);  
```  
  
#### Parameters  
 *clrFillColor*  
 The new fill color for the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_FillColor](../vs140/CStockPropImpl--get_FillColor.md)