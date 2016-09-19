---
title: "CImageList::SetDragCursorImage"
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
ms.assetid: 1fd55298-950d-4505-917a-006e5b067ec4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::SetDragCursorImage
Creates a new drag image by combining the given image (typically a mouse cursor image) with the current drag image.  
  
## Syntax  
  
```  
  
      BOOL SetDragCursorImage(  
   int nDrag,  
   CPoint ptHotSpot   
);  
```  
  
#### Parameters  
 *nDrag*  
 Index of the new image to be combined with the drag image.  
  
 `ptHotSpot`  
 Position of the hot spot within the new image.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Because the dragging functions use the new image during a drag operation, you should use the Windows [ShowCursor](http://msdn.microsoft.com/library/windows/desktop/ms648396) function to hide the actual mouse cursor after calling `CImageList::SetDragCursorImage`. Otherwise, the system may appear to have two mouse cursors for the duration of the drag operation.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md)   
 [CImageList::EndDrag](../vs140/CImageList--EndDrag.md)   
 [CImageList::GetDragImage](../vs140/CImageList--GetDragImage.md)