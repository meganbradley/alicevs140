---
title: "IOleObjectImpl::DoVerbShow"
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
ms.assetid: 218e3fda-5ce8-49aa-9dfd-71758789e4b5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::DoVerbShow
Tells the container to make the control visible.  
  
## Syntax  
  
```  
  
      HRESULT DoVerbShow(  
   LPCRECT prcPosRect,  
   HWND /* hwndParent */  
);  
```  
  
#### Parameters  
 `prcPosRec`  
 [in] Pointer to the rectangle the container wants the control to draw into.  
  
 *hwndParent*  
 [in] Handle of the window containing the control. Not used in the ATL implementation.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::DoVerbHide](../vs140/IOleObjectImpl--DoVerbHide.md)