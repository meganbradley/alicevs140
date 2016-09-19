---
title: "CToolBarCtrl::GetImageList"
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
ms.assetid: ddeab856-cf3d-428e-8c6f-185a4e749dc6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetImageList
Retrieves the image list that a toolbar control uses to display buttons in their default state.  
  
## Syntax  
  
```  
  
CImageList* GetImageList( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CImageList](../vs140/CImageList-Class.md) object, or **NULL** if no image list is set.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETIMAGELIST](http://msdn.microsoft.com/library/windows/desktop/bb787337), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetDisabledImageList](../vs140/CToolBarCtrl--GetDisabledImageList.md)   
 [CToolBarCtrl::GetHotImageList](../vs140/CToolBarCtrl--GetHotImageList.md)