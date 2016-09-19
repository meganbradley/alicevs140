---
title: "CImageList::DragShowNolock"
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
ms.assetid: fb8a3055-4f91-476b-8c84-f391c030d443
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::DragShowNolock
Shows or hides the drag image during a drag operation, without locking the window.  
  
## Syntax  
  
```  
  
      static BOOL PASCAL DragShowNolock(  
   BOOL bShow   
);  
```  
  
#### Parameters  
 `bShow`  
 Specifies whether the drag image is to be shown.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The [CImageList::DragEnter](../vs140/CImageList--DragEnter.md) function locks all updates to the window during a drag operation. This function, however, does not lock the window.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md)   
 [CImageList::EndDrag](../vs140/CImageList--EndDrag.md)   
 [CImageList::DragEnter](../vs140/CImageList--DragEnter.md)   
 [CImageList::DragLeave](../vs140/CImageList--DragLeave.md)   
 [CImageList::Draw](../vs140/CImageList--Draw.md)