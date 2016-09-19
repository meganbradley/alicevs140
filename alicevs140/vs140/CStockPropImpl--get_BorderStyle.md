---
title: "CStockPropImpl::get_BorderStyle"
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
ms.assetid: ac7ffb5d-5309-4b57-9813-0d94daff3fca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_BorderStyle
Call this method to get the control's border style.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_BorderStyle(  
   LONG * pnBorderStyle  
);  
```  
  
#### Parameters  
 *pnBorderStyle*  
 Variable that receives the control's border style.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_BorderStyle](../vs140/CStockPropImpl--put_BorderStyle.md)