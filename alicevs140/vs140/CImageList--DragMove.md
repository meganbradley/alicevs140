---
title: "CImageList::DragMove"
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
ms.assetid: 2ac0ab9e-b2a8-4eb2-9028-a2b2ead18184
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::DragMove
Call this function to move the image that is being dragged during a drag-and-drop operation.  
  
## Syntax  
  
```  
  
      static BOOL PASCAL DragMove(  
   CPoint pt   
);  
```  
  
#### Parameters  
 `pt`  
 New drag position.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This function is typically called in response to a `WM_MOUSEMOVE` message. To begin a drag operation, use the `BeginDrag` member function.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#4)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md)   
 [CImageList::EndDrag](../vs140/CImageList--EndDrag.md)   
 [CImageList::Draw](../vs140/CImageList--Draw.md)