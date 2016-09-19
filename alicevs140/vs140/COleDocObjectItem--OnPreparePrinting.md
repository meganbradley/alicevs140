---
title: "COleDocObjectItem::OnPreparePrinting"
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
ms.assetid: d783fd82-1d3e-42ef-bf83-45424049762e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocObjectItem::OnPreparePrinting
This member function is called by the framework to prepare a document for printing.  
  
## Syntax  
  
```  
  
      static BOOL OnPreparePrinting(  
   CView* pCaller,  
   CPrintInfo* pInfo,  
   BOOL bPrintAll = TRUE   
);  
```  
  
#### Parameters  
 `pCaller`  
 A pointer to a [CView](../vs140/CView-Class.md) object that is sending the print command.  
  
 `pInfo`  
 A pointer to a [CPrintInfo](../vs140/CPrintInfo-Structure.md) object that describes the job to be printed.  
  
 `bPrintAll`  
 Specifies whether the entire document is to be printed.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocObjectItem Class](../vs140/COleDocObjectItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocObjectItem::OnPrint](../vs140/COleDocObjectItem--OnPrint.md)