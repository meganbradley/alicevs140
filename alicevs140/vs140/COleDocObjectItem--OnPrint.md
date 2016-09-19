---
title: "COleDocObjectItem::OnPrint"
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
ms.assetid: dc391b39-98e4-46f9-a4c8-97f873298b4d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocObjectItem::OnPrint
This member function is called by the framework to print a document.  
  
## Syntax  
  
```  
  
      static void OnPrint(  
   CView* pCaller,  
   CPrintInfo* pInfo,  
   BOOL bPrintAll = TRUE   
);  
```  
  
#### Parameters  
 `pCaller`  
 A pointer to a CView object that is sending the print command.  
  
 `pInfo`  
 A pointer to a [CPrintInfo](../vs140/CPrintInfo-Structure.md) object that describes the job to be printed.  
  
 `bPrintAll`  
 Specifies whether the entire document is to be printed.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocObjectItem Class](../vs140/COleDocObjectItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocObjectItem::OnPreparePrinting](../vs140/COleDocObjectItem--OnPreparePrinting.md)