---
title: "CTabCtrl::RemoveImage"
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
ms.assetid: ff4f199b-2213-4bf8-ad98-b703d9f5284f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::RemoveImage
Removes the specified image from a tab control's image list.  
  
## Syntax  
  
```  
  
      void RemoveImage(  
  int nImage   
);  
```  
  
#### Parameters  
 `nImage`  
 Zero-based index of the image to remove.  
  
## Remarks  
 The tab control updates each tab's image index so that each tab remains associated with the same image.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::GetImageList](../vs140/CTabCtrl--GetImageList.md)   
 [CTabCtrl::SetImageList](../vs140/CTabCtrl--SetImageList.md)