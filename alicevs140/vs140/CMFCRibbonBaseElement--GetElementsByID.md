---
title: "CMFCRibbonBaseElement::GetElementsByID"
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
ms.assetid: 55a2fb87-e13f-4efd-a593-fcaaa8cf32e3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::GetElementsByID
Adds the current ribbon element to the specified array if the current ribbon element contains the specified command ID.  
  
## Syntax  
  
```  
virtual void GetElementsByID(  
   UINT uiCmdID,  
   CArray<CMFCRibbonBaseElement*, CMFCRibbonBaseElement*>& arElements  
);  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 Command ID of a ribbon element.  
  
 [in] `arElements`  
 An array of ribbon elements.  
  
## Remarks  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)