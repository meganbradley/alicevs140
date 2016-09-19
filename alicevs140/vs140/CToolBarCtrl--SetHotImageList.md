---
title: "CToolBarCtrl::SetHotImageList"
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
ms.assetid: fab24c55-da98-4618-93c8-837835cb55c2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetHotImageList
Sets the image list that the toolbar control will use to display "hot" buttons.  
  
## Syntax  
  
```  
  
      CImageList* SetHotImageList(  
   CImageList* pImageList   
);  
```  
  
#### Parameters  
 `pImageList`  
 A pointer to a `CImageList` object containing the images to be used by the toolbar control to display hot button images.  
  
## Return Value  
 A pointer to a [CImageList](../vs140/CImageList-Class.md) object that was previously used by the toolbar control to display hot button images.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_SETHOTIMAGELIST](http://msdn.microsoft.com/library/windows/desktop/bb787429), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The MFC implementation of `SetHotImageList` uses a `CImageList` object containing the toolbar control's hot button images, rather than a handle to an image list. A hot button appears highlighted when the pointer is above it.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetHotImageList](../vs140/CToolBarCtrl--GetHotImageList.md)   
 [CToolBarCtrl::SetDisabledImageList](../vs140/CToolBarCtrl--SetDisabledImageList.md)   
 [CToolBarCtrl::SetImageList](../vs140/CToolBarCtrl--SetImageList.md)