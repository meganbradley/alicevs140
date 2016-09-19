---
title: "CToolBarCtrl::SetImageList"
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
ms.assetid: ea89c227-951f-4fc4-95c7-c36d048b94a7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetImageList
Sets the image list that the toolbar will use to display buttons that are in their default state.  
  
## Syntax  
  
```  
  
      CImageList* SetImageList(  
   CImageList* pImageList   
);  
```  
  
#### Parameters  
 `pImageList`  
 A pointer to a `CImageList` object containing the images to be used by the toolbar control to display button images in their default state.  
  
## Return Value  
 A pointer to a [CImageList](../vs140/CImageList-Class.md) object that was previously used by the toolbar control to display button images in their default state.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_SETIMAGELIST](http://msdn.microsoft.com/library/windows/desktop/bb787433), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The MFC implementation of `SetImageList` uses a `CImageList` object containing the toolbar control's button images, rather than a handle to an image list.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetImageList](../vs140/CToolBarCtrl--GetImageList.md)   
 [CToolBarCtrl::SetDisabledImageList](../vs140/CToolBarCtrl--SetDisabledImageList.md)   
 [CToolBarCtrl::SetHotImageList](../vs140/CToolBarCtrl--SetHotImageList.md)