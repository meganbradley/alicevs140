---
title: "CTreeCtrl::SetItemImage"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: a79bec3e-f7f6-4a53-8856-b46205e8c42b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetItemImage
Associates images with an item.  
  
## Syntax  
  
```  
  
      BOOL SetItemImage(  
   HTREEITEM hItem,  
   int nImage,  
   int nSelectedImage   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of the item whose image is to be set.  
  
 `nImage`  
 Index of the item's image in the tree view control's image list.  
  
 `nSelectedImage`  
 Index of the item's selected image in the tree view control's image list.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Each item in a tree view control can have a pair of bitmapped images associated with it. The images appear on the left side of an item's label. One image is displayed when the item is selected, and the other is displayed when the item is not selected. For example, an item might display an open folder when it is selected and a closed folder when it is not selected.  
  
 Call this function to set the index of the item's image and its selected image within the tree view control's image list.  
  
 For more information on images, see [CImageList](../vs140/CImageList-Class.md).  
  
## Example  
 See the example for [CTreeCtrl::GetItemImage](../vs140/CTreeCtrl--GetItemImage.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetItemImage](../vs140/CTreeCtrl--GetItemImage.md)   
 [CImageList Class](../vs140/CImageList-Class.md)