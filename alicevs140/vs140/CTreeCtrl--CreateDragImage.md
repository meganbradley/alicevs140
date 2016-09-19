---
title: "CTreeCtrl::CreateDragImage"
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
ms.assetid: b3748a06-598f-48d8-bcb5-643544e7ae08
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::CreateDragImage
Call this function to create a dragging bitmap for the given item in a tree view control, create an image list for the bitmap, and add the bitmap to the image list.  
  
## Syntax  
  
```  
  
      CImageList* CreateDragImage(  
   HTREEITEM hItem   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of the tree item to be dragged.  
  
## Return Value  
 Pointer to the image list to which the dragging bitmap was added, if successful; otherwise **NULL**.  
  
## Remarks  
 An application uses the image-list functions to display the image when the item is being dragged.  
  
 The `CImageList` object is permanent, and you must delete it when finished. For example:  
  
 [!CODE [NVC_MFC_CTreeCtrl#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#2)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SelectDropTarget](../vs140/CTreeCtrl--SelectDropTarget.md)   
 [CTreeCtrl::GetDropHilightItem](../vs140/CTreeCtrl--GetDropHilightItem.md)   
 [CTreeCtrl::SetImageList](../vs140/CTreeCtrl--SetImageList.md)