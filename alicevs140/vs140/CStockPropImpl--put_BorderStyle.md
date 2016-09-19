---
title: "CStockPropImpl::put_BorderStyle"
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
ms.assetid: 44090edc-049c-48af-a2cf-7914e8bb7573
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_BorderStyle
Call this method to set the control's border style.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_BorderStyle(  
   LONG nBorderStyle  
);  
```  
  
#### Parameters  
 *nBorderStyle*  
 The new border style.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_BorderStyle](../vs140/CStockPropImpl--get_BorderStyle.md)