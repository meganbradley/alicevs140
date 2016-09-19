---
title: "CMFCRibbonBar::GetContextName"
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
ms.assetid: 7c1fe738-6310-4b11-a48c-187d15ea3b87
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::GetContextName
Retrieves the name of the context category caption specified by a context ID.  
  
## Syntax  
  
```  
BOOL GetContextName(  
   UINT uiContextID,  
   CString& strName   
) const;  
```  
  
#### Parameters  
 [in] `uiContextID`  
 A ribbon category context ID.  
  
 [out] `strName`  
 The name of a context category caption.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise, `FALSE` if `uiContextID` was zero or the context category caption was not found.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)