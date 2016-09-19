---
title: "CImageList::DragLeave"
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
ms.assetid: c11a88a7-7f49-4d41-aec5-17151f3dca1b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::DragLeave
Unlocks the window specified by `pWndLock` and hides the drag image, allowing the window to be updated.  
  
## Syntax  
  
```  
  
      static BOOL PASCAL DragLeave(  
   CWnd* pWndLock   
);  
```  
  
#### Parameters  
 `pWndLock`  
 Pointer to the window that owns the drag image.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 See the example for [CImageList::EndDrag](../vs140/CImageList--EndDrag.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md)   
 [CImageList::EndDrag](../vs140/CImageList--EndDrag.md)   
 [CImageList::DragMove](../vs140/CImageList--DragMove.md)   
 [CImageList::DragEnter](../vs140/CImageList--DragEnter.md)