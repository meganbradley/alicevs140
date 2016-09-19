---
title: "CMFCRibbonBar::SetElementKeys"
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
ms.assetid: 36e72f90-6ebb-4cb4-af0c-a34fba239b1d
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::SetElementKeys
Sets the keytips for all ribbon elements that have the specified command ID.  
  
## Syntax  
  
```  
BOOL SetElementKeys(  
   UINT uiCmdID,  
   LPCTSTR lpszKeys,  
   LPCTSTR lpszMenuKeys = NULL   
);  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 The command ID of a ribbon element.  
  
 [in] `lpszKeys`  
 The keytip.  
  
 [in] `lpszMenuKeys`  
 The menu keytip.  
  
## Return Value  
 `TRUE` if the keytips of at least one ribbon element are set; otherwise `FALSE`.  
  
## Remarks  
 The optional menu keytip is for ribbon elements with a split button that opens a popup menu.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)