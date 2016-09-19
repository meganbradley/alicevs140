---
title: "CStockPropImpl::put_FillStyle"
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
ms.assetid: 03078798-295b-4b75-8943-96e603a5843a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_FillStyle
Call this method to set the control's fill style, for example, solid, transparent, or cross-hatched.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_FillStyle(  
   LONG nFillStyle  
);  
```  
  
#### Parameters  
 *nFillStyle*  
 The new fill style for the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_FillStyle](../vs140/CStockPropImpl--get_FillStyle.md)