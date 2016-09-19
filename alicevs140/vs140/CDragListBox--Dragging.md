---
title: "CDragListBox::Dragging"
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
ms.assetid: 2e4fad60-4016-41fc-afd7-187e718a467d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDragListBox::Dragging
Called by the framework when a list box item is being dragged within the `CDragListBox` object.  
  
## Syntax  
  
```  
  
      virtual UINT Dragging(  
   CPoint pt   
);  
```  
  
#### Parameters  
 `pt`  
 A [CPoint](../vs140/CPoint-Class.md) object that contains the x and y screen coordinates of the cursor.  
  
## Return Value  
 The resource ID of the cursor to be displayed. The following values are possible:  
  
-   `DL_COPYCURSOR` Indicates that the item will be copied.  
  
-   `DL_MOVECURSOR` Indicates that the item will be moved.  
  
-   `DL_STOPCURSOR` Indicates that the current drop target is not acceptable.  
  
## Remarks  
 The default behavior returns `DL_MOVECURSOR`. Override this function if you want to provide additional functionality.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CDragListBox Class](../vs140/CDragListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDragListBox::BeginDrag](../vs140/CDragListBox--BeginDrag.md)   
 [CDragListBox::CancelDrag](../vs140/CDragListBox--CancelDrag.md)