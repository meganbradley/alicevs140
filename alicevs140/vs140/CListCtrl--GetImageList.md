---
title: "CListCtrl::GetImageList"
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
ms.assetid: 727575c9-ab06-407b-b1ec-8bdae89f7f08
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetImageList
Retrieves the handle of an image list used for drawing list view items.  
  
## Syntax  
  
```  
  
      CImageList* GetImageList(  
   int nImageList   
) const;  
```  
  
#### Parameters  
 `nImageList`  
 Value specifying which image list to retrieve. It can be one of these values:  
  
-   `LVSIL_NORMAL` Image list with large icons.  
  
-   `LVSIL_SMALL` Image list with small icons.  
  
-   `LVSIL_STATE` Image list with state images.  
  
## Return Value  
 A pointer to the image list used for drawing list view items.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#20)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList Class](../vs140/CImageList-Class.md)   
 [CListCtrl::SetImageList](../vs140/CListCtrl--SetImageList.md)