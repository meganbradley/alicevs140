---
title: "IOleObjectImpl::DoVerbPrimary"
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
ms.assetid: 9b5e4935-2d80-4cb4-9281-eb065cadd6a3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::DoVerbPrimary
Defines the action taken when the user double-clicks the control.  
  
## Syntax  
  
```  
  
      HRESULT DoVerbPrimary(  
   LPCRECT prcPosRect,  
   HWND hwndParent   
);  
```  
  
#### Parameters  
 `prcPosRec`  
 [in] Pointer to the rectangle the container wants the control to draw into.  
  
 *hwndParent*  
 [in] Handle of the window containing the control.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 By default, set to display the property pages. You can override this in your control class to invoke a different behavior on double-click; for example, play a video or go in-place active.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [CComControlBase::DoVerbProperties](../vs140/CComControlBase--DoVerbProperties.md)