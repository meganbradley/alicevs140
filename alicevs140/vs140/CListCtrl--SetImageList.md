---
title: "CListCtrl::SetImageList"
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
ms.assetid: 4734bcef-9850-40b5-9f05-4baebe9d0a26
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetImageList
Assigns an image list to a list view control.  
  
## Syntax  
  
```  
  
      CImageList* SetImageList(  
   CImageList* pImageList,  
   int nImageListType   
);  
```  
  
#### Parameters  
 `pImageList`  
 Pointer to the image list to assign.  
  
 `nImageListType`  
 Type of image list. It can be one of these values:  
  
-   `LVSIL_NORMAL` Image list with large icons.  
  
-   `LVSIL_SMALL` Image list with small icons.  
  
-   `LVSIL_STATE` Image list with state images.  
  
## Return Value  
 A pointer to the previous image list.  
  
## Example  
 See the example for [CListCtrl::GetImageList](../vs140/CListCtrl--GetImageList.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList Class](../vs140/CImageList-Class.md)   
 [CListCtrl::GetImageList](../vs140/CListCtrl--GetImageList.md)