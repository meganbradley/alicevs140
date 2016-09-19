---
title: "CMFCRibbonBar::GetElementsByID"
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
ms.assetid: 52368660-9367-4953-8ec3-3417aa971827
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::GetElementsByID
Retrieves an array of pointers to all ribbon elements that have a specific command ID.  
  
## Syntax  
  
```  
void GetElementsByID(  
   UINT uiCmdID,  
   CArray<CMFCRibbonBaseElement* ,CMFCRibbonBaseElement*>& arButtons   
);  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 Command ID of a ribbon element.  
  
 [out] `arButtons`  
 An array of pointers to ribbon elements.  
  
## Remarks  
 Multiple ribbon elements can have the same command ID because some ribbon elements can be copied to the quick access toolbar.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)