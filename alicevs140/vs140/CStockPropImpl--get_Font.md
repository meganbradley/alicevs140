---
title: "CStockPropImpl::get_Font"
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
ms.assetid: f0a8cca1-b3d6-4b5e-b461-2ae2572dc579
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_Font
Call this method to get a pointer to the control's font properties.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Font(  
   IFontDisp** ppFont  
);  
```  
  
#### Parameters  
 `ppFont`  
 Variable that receives a pointer to the control's font properties.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Font](../vs140/CStockPropImpl--put_Font.md)