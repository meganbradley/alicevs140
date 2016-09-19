---
title: "CStockPropImpl::putref_Font"
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
ms.assetid: 3e3dcaeb-6529-47ef-a44d-89e3fc6717b3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::putref_Font
Call this method to set the control's font properties, with a reference count.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE putref_Font(  
   IFontDisp* pFont   
);  
```  
  
#### Parameters  
 `pFont`  
 A pointer to the control's font properties.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 The same as [CStockPropImpl::put_Font](../vs140/CStockPropImpl--put_Font.md), but with a reference count.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Font](../vs140/CStockPropImpl--put_Font.md)