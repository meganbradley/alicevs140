---
title: "CView::IsSelected"
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
ms.assetid: 9763d7ee-b3b2-4b64-8c9d-8e8d191ad1a4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::IsSelected
Called by the framework to check whether the specified document item is selected.  
  
## Syntax  
  
```  
  
      virtual BOOL IsSelected(  
   const CObject* pDocItem   
) const;  
```  
  
#### Parameters  
 `pDocItem`  
 Points to the document item being tested.  
  
## Return Value  
 Nonzero if the specified document item is selected; otherwise 0.  
  
## Remarks  
 The default implementation of this function returns **FALSE**. Override this function if you are implementing selection using [CDocItem](../vs140/CDocItem-Class.md) objects. You must override this function if your view contains OLE items.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocItem Class](../vs140/CDocItem-Class.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)