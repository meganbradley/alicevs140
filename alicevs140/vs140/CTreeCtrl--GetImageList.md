---
title: "CTreeCtrl::GetImageList"
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
ms.assetid: d4a08f4f-78cb-401f-b06c-aa9d0816be12
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetImageList
Call this function to retrieve the handle of the normal or state image list associated with the tree view control.  
  
## Syntax  
  
```  
  
      CImageList* GetImageList(  
   UINT nImageList   
) const;  
```  
  
#### Parameters  
 `nImageList`  
 Type of image list to retrieve. The image list can be one of the following values:  
  
-   `TVSIL_NORMAL` Retrieves the normal image list, which contains the selected and nonselected images for the tree view item.  
  
-   `TVSIL_STATE` Retrieves the state image list, which contains the images for tree view items that are in a user-defined state.  
  
## Return Value  
 Pointer to the control's image list if successful; otherwise **NULL**.  
  
## Remarks  
 Each item in a tree view control can have a pair of bitmapped images associated with it. One image is displayed when the item is selected, and the other is displayed when the item is not selected. For example, an item might display an open folder when it is selected and a closed folder when it is not selected.  
  
 For more information on image lists, see the [CImageList](../vs140/CImageList-Class.md) class.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#11)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList Class](../vs140/CImageList-Class.md)   
 [CTreeCtrl::SetImageList](../vs140/CTreeCtrl--SetImageList.md)