---
title: "CMFCRibbonBaseElement::FindByData"
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
ms.assetid: b7f5c6fc-3a61-475f-acb2-55da1629aa32
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::FindByData
Retrieves a pointer to the ribbon element if it contains the specified data.  
  
## Syntax  
  
```  
virtual CMFCRibbonBaseElement* FindByData(  
   DWORD_PTR dwData  
);  
```  
  
#### Parameters  
 [in] `dwData`  
 The data associated with a ribbon element.  
  
## Return Value  
 A pointer to the ribbon element if it contains the specified data; otherwise `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)