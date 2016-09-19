---
title: "CStockPropImpl::put_MouseIcon"
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
ms.assetid: d31243ca-ad22-4421-a598-3eb1f92f4457
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_MouseIcon
Call this method to set the picture properties of the graphic (icon, bitmap, or metafile) to be displayed when the mouse is over the control.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_MouseIcon(  
   IPictureDisp* pPicture   
);  
```  
  
#### Parameters  
 `pPicture`  
 A pointer to the picture properties of the graphic.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_MouseIcon](../vs140/CStockPropImpl--get_MouseIcon.md)   
 [CStockPropImpl::putref_MouseIcon](../vs140/CStockPropImpl--putref_MouseIcon.md)