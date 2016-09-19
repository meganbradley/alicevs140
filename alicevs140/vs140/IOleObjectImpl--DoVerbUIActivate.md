---
title: "IOleObjectImpl::DoVerbUIActivate"
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
ms.assetid: bc05755f-8934-49b7-a862-77a3a0eadef9
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::DoVerbUIActivate
Activates the control's user interface and notifies the container that its menus are being replaced by composite menus.  
  
## Syntax  
  
```  
  
      HRESULT DoVerbUIActivate(  
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
 [CComControlBase::InPlaceActivate](../vs140/CComControlBase--InPlaceActivate.md)   
 [IOleObjectImpl::DoVerbInPlaceActivate](../vs140/IOleObjectImpl--DoVerbInPlaceActivate.md)