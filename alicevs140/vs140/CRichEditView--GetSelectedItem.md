---
title: "CRichEditView::GetSelectedItem"
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
ms.assetid: aa2f3e58-cbae-486a-ad35-ed9c47f6727f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetSelectedItem
Call this function to retrieve the OLE item (a `CRichEditCntrItem` object) currently selected in this `CRichEditView` object.  
  
## Syntax  
  
```  
  
CRichEditCntrItem* GetSelectedItem( ) const;  
  
```  
  
## Return Value  
 Pointer to a [CRichEditCntrItem](../vs140/CRichEditCntrItem-Class.md) object selected in the `CRichEditView` object; **NULL** if no item is selected in this view.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCntrItem Class](../vs140/CRichEditCntrItem-Class.md)   
 [CRichEditView::GetInPlaceActiveItem](../vs140/CRichEditView--GetInPlaceActiveItem.md)