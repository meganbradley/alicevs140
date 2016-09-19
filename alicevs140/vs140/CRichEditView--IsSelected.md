---
title: "CRichEditView::IsSelected"
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
ms.assetid: ca0a29f7-8de2-4e49-b59e-5fbb6cf614f9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::IsSelected
Call this function to determine if the specified OLE item is currently selected in this view.  
  
## Syntax  
  
```  
  
      virtual BOOL IsSelected(  
   const CObject* pDocItem   
) const;  
```  
  
#### Parameters  
 `pDocItem`  
 Pointer to an object in the view.  
  
## Return Value  
 Nonzero if the object is selected; otherwise 0.  
  
## Remarks  
 Override this function if your derived view class has a different method for handling selection of OLE items.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::GetSelectedItem](../vs140/CRichEditView--GetSelectedItem.md)   
 [CRichEditView::GetInPlaceActiveItem](../vs140/CRichEditView--GetInPlaceActiveItem.md)