---
title: "CDragListBox::Dropped"
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
ms.assetid: abbbd0a7-d5c2-46ba-96a7-b95c3e84e088
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDragListBox::Dropped
Called by the framework when an item is dropped within a `CDragListBox` object.  
  
## Syntax  
  
```  
  
      virtual void Dropped(  
   int nSrcIndex,  
   CPoint pt   
);  
```  
  
#### Parameters  
 *nSrcIndex*  
 Specifies the zero-based index of the dropped string.  
  
 `pt`  
 A [CPoint](../vs140/CPoint-Class.md) object that contains the coordinates of the drop site.  
  
## Remarks  
 The default behavior copies the list box item and its data to the new location and then deletes the original item. Override this function to customize the default behavior, such as enabling copies of list box items to be dragged to other locations within the list.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CDragListBox Class](../vs140/CDragListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDragListBox::BeginDrag](../vs140/CDragListBox--BeginDrag.md)