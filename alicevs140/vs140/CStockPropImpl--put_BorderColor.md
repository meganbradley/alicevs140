---
title: "CStockPropImpl::put_BorderColor"
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
ms.assetid: 68d8c09c-61b7-462a-964d-4857fefcfad2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_BorderColor
Call this method to set the control's border color.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_BorderColor(  
   OLE_COLOR clrBorderColor  
);  
```  
  
#### Parameters  
 *clrBorderColor*  
 The new border color. The OLE_COLOR data type is internally represented as a 32-bit long integer.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_BorderColor](../vs140/CStockPropImpl--get_BorderColor.md)