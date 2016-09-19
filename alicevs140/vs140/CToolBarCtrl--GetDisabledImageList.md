---
title: "CToolBarCtrl::GetDisabledImageList"
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
ms.assetid: bab771ec-ff12-4158-b2a8-d2109d5a8869
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetDisabledImageList
Retrieves the image list that a toolbar control uses to display disabled buttons.  
  
## Syntax  
  
```  
  
CImageList* GetDisabledImageList( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CImageList](../vs140/CImageList-Class.md) object, or **NULL** if no disabled image list is set.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETDISABLEDIMAGELIST](http://msdn.microsoft.com/library/windows/desktop/bb787329), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The MFC implementation of `GetDisabledImageList` uses a `CImageList` object containing the toolbar control's button images, rather than a handle to an image list.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetDisabledImageList](../vs140/CToolBarCtrl--SetDisabledImageList.md)   
 [CToolBarCtrl::GetHotImageList](../vs140/CToolBarCtrl--GetHotImageList.md)   
 [CToolBarCtrl::GetImageList](../vs140/CToolBarCtrl--GetImageList.md)