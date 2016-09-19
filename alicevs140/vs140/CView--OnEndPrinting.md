---
title: "CView::OnEndPrinting"
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
ms.assetid: fbf67c96-e296-45e2-8e5f-42ce905b502f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnEndPrinting
Called by the framework after a document has been printed or previewed.  
  
## Syntax  
  
```  
  
      virtual void OnEndPrinting(  
   CDC* pDC,  
   CPrintInfo* pInfo   
);  
```  
  
#### Parameters  
 `pDC`  
 Points to the printer device context.  
  
 `pInfo`  
 Points to a [CPrintInfo](../vs140/CPrintInfo-Structure.md) structure that describes the current print job.  
  
## Remarks  
 The default implementation of this function does nothing. Override this function to free any GDI resources you allocated in the [OnBeginPrinting](../vs140/CView--OnBeginPrinting.md) member function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnBeginPrinting](../vs140/CView--OnBeginPrinting.md)