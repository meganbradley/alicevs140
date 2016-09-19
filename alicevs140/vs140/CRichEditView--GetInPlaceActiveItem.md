---
title: "CRichEditView::GetInPlaceActiveItem"
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
ms.assetid: 00bb819a-0dd3-40c5-9803-fbb078e9bb0f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetInPlaceActiveItem
Call this function to get the OLE item that is currently activated in place in this `CRichEditView` object.  
  
## Syntax  
  
```  
  
CRichEditCntrItem* GetInPlaceActiveItem( ) const;  
  
```  
  
## Return Value  
 A pointer to the single, in-place active [CRichEditCntrItem](../vs140/CRichEditCntrItem-Class.md) object in this rich edit view; **NULL** if there is no OLE item currently in the in-place active state.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::GetInPlaceActiveItem](../vs140/COleDocument--GetInPlaceActiveItem.md)   
 [CRichEditCntrItem Class](../vs140/CRichEditCntrItem-Class.md)   
 [CRichEditView::GetSelectedItem](../vs140/CRichEditView--GetSelectedItem.md)