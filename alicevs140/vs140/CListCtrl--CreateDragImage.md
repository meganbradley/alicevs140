---
title: "CListCtrl::CreateDragImage"
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
ms.assetid: 9d57d7f3-15aa-4c78-8a7b-9f8a74c12c42
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::CreateDragImage
Creates a drag image list for the item specified by `nItem`.  
  
## Syntax  
  
```  
  
      CImageList* CreateDragImage(  
   int nItem,  
   LPPOINT lpPoint   
);  
```  
  
#### Parameters  
 `nItem`  
 Index of the item whose drag image list is to be created.  
  
 `lpPoint`  
 Address of a [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) structure that receives the initial location of the upper-left corner of the image, in view coordinates.  
  
## Return Value  
 A pointer to the drag image list if successful; otherwise **NULL**.  
  
## Remarks  
 The `CImageList` object is permanent, and you must delete it when finished. For example:  
  
 [!CODE [NVC_MFC_CListCtrl#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#3)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList Class](../vs140/CImageList-Class.md)   
 [CListCtrl::GetImageList](../vs140/CListCtrl--GetImageList.md)