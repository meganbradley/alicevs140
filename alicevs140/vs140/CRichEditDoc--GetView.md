---
title: "CRichEditDoc::GetView"
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
ms.assetid: ed84e2e4-9e8b-420a-9881-c32294156ce4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditDoc::GetView
Call this function to access the [CRichEditView](../vs140/CRichEditView-Class.md) object associated with this `CRichEditDoc` object.  
  
## Syntax  
  
```  
  
virtual CRichEditView* GetView( ) const;  
  
```  
  
## Return Value  
 Pointer to the `CRichEditView` object associated with the document.  
  
## Remarks  
 The text and formatting information are contained within the `CRichEditView` object. The `CRichEditDoc` object maintains the OLE items for serialization. There should be only one `CRichEditView` for each `CRichEditDoc`.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditDoc Class](../vs140/CRichEditDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [CDocument::GetNextView](../vs140/CDocument--GetNextView.md)