---
title: "CDragListBox::CancelDrag"
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
ms.assetid: ec2bf084-4dd3-450e-98bf-d17110a19cc0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDragListBox::CancelDrag
Called by the framework when a drag operation has been canceled.  
  
## Syntax  
  
```  
  
      virtual void CancelDrag(  
   CPoint pt   
);  
```  
  
#### Parameters  
 `pt`  
 A [CPoint](../vs140/CPoint-Class.md) object that contains the coordinates of the item being dragged.  
  
## Remarks  
 Override this function to handle any special processing for your list box control.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CDragListBox Class](../vs140/CDragListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDragListBox::BeginDrag](../vs140/CDragListBox--BeginDrag.md)   
 [CDragListBox::Dragging](../vs140/CDragListBox--Dragging.md)