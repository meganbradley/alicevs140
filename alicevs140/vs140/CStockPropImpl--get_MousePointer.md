---
title: "CStockPropImpl::get_MousePointer"
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
ms.assetid: 74349bf9-48b9-4141-b139-a3588205eab0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_MousePointer
Call this method to get the type of mouse pointer displayed when the mouse is over the control, for example, arrow, cross, or hourglass.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_MousePointer(  
   LONG * pnMousePointer  
);  
```  
  
#### Parameters  
 *pnMousePointer*  
 Variable that receives the type of mouse pointer.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_MousePointer](../vs140/CStockPropImpl--put_MousePointer.md)