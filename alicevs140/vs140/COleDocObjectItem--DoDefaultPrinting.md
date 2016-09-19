---
title: "COleDocObjectItem::DoDefaultPrinting"
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
ms.assetid: ac4bcfa0-9f4e-4cac-8c6a-e1adfa47ae9b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocObjectItem::DoDefaultPrinting
Called by the framework to a document using the default settings.  
  
## Syntax  
  
```  
  
      static HRESULT DoDefaultPrinting(  
   CView *pCaller,  
   CPrintInfo *pInfo  
);  
```  
  
#### Parameters  
 `pCaller`  
 A pointer to a [CView](../vs140/CView-Class.md) object that is sending the print command.  
  
 `pInfo`  
 A pointer to a [CPrintInfo](../vs140/CPrintInfo-Structure.md) object that describes the job to be printed.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocObjectItem Class](../vs140/COleDocObjectItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)