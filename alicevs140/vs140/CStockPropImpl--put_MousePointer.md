---
title: "CStockPropImpl::put_MousePointer"
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
ms.assetid: 6cf4db3a-469d-464f-b6a4-022fce57de6f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_MousePointer
Call this method to set the type of mouse pointer displayed when the mouse is over the control, for example, arrow, cross, or hourglass.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_MousePointer(  
   LONG nMousePointer  
);  
```  
  
#### Parameters  
 *nMousePointer*  
 The type of mouse pointer.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_MousePointer](../vs140/CStockPropImpl--get_MousePointer.md)