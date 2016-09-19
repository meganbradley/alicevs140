---
title: "CStockPropImpl::put_Font"
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
ms.assetid: 709c3389-9c46-45fe-a133-db169dc47da9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_Font
Call this method to set the control's font properties.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_Font(  
   IFontDisp* pFont   
);  
```  
  
#### Parameters  
 `pFont`  
 A pointer to the control's font properties.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_Font](../vs140/CStockPropImpl--get_Font.md)   
 [CStockPropImpl::putref_Font](../vs140/CStockPropImpl--putref_Font.md)