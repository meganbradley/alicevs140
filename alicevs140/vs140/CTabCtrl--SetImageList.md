---
title: "CTabCtrl::SetImageList"
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
ms.assetid: f5c25c02-7cea-485d-ada3-e1d83280d5bf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::SetImageList
Assigns an image list to a tab control.  
  
## Syntax  
  
```  
  
      CImageList * SetImageList(  
  CImageList * pImageList   
);  
```  
  
#### Parameters  
 `pImageList`  
 Pointer to the image list to be assigned to the tab control.  
  
## Return Value  
 Returns a pointer to the previous image list or **NULL** if there is no previous image list.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::GetImageList](../vs140/CTabCtrl--GetImageList.md)   
 [CImageList Class](../vs140/CImageList-Class.md)