---
title: "CImageList::BeginDrag"
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
ms.assetid: f76526b7-7aea-499e-a87b-d18775cbb322
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::BeginDrag
Call this function to begin dragging an image.  
  
## Syntax  
  
```  
  
      BOOL BeginDrag(  
   int nImage,  
   CPoint ptHotSpot   
);  
```  
  
#### Parameters  
 `nImage`  
 Zero-based index of the image to drag.  
  
 `ptHotSpot`  
 Coordinates of the starting drag position (typically, the cursor position). The coordinates are relative to the upper left corner of the image.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This function creates a temporary image list that is used for dragging. The image combines the specified image and its mask with the current cursor. In response to subsequent `WM_MOUSEMOVE` messages, you can move the drag image by using the `DragMove` member function. To end the drag operation, you can use the `EndDrag` member function.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#3)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::Draw](../vs140/CImageList--Draw.md)   
 [CImageList::EndDrag](../vs140/CImageList--EndDrag.md)   
 [CImageList::DragMove](../vs140/CImageList--DragMove.md)