---
title: "CToolBarCtrl::GetDropTarget"
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
ms.assetid: 1d9d89f2-e717-4509-8e04-fdc2d513afbd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetDropTarget
Retrieves the [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) interface for a toolbar control.  
  
## Syntax  
  
```  
  
      HRESULT GetDropTarget(  
   IDropTarget** ppDropTarget   
) const;  
```  
  
#### Parameters  
 `ppDropTarget`  
 A pointer to an [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) interface pointer. If an error occurs, a **NULL** pointer is placed in this address.  
  
## Return Value  
 Returns an `HRESULT` value indicating success or failure of the operation.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETOBJECT](http://msdn.microsoft.com/library/windows/desktop/bb787343), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)