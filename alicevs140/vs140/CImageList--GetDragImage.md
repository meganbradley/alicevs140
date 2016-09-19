---
title: "CImageList::GetDragImage"
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
ms.assetid: 3fe7cea9-e3d0-4165-9c7d-a2762da2fda0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::GetDragImage
Gets the temporary image list that is used for dragging.  
  
## Syntax  
  
```  
  
      static CImageList* PASCAL GetDragImage(  
   LPPOINT lpPoint,  
   LPPOINT lpPointHotSpot   
);  
```  
  
#### Parameters  
 `lpPoint`  
 Address of a [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) structure that receives the current drag position.  
  
 *lpPointHotSpot*  
 Address of a **POINT** structure that receives the offset of the drag image relative to the drag position.  
  
## Return Value  
 If successful, a pointer to the temporary image list that is used for dragging; otherwise, **NULL**.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::SetDragCursorImage](../vs140/CImageList--SetDragCursorImage.md)