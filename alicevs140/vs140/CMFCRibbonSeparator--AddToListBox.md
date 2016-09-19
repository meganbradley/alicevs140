---
title: "CMFCRibbonSeparator::AddToListBox"
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
ms.assetid: dd2e39ff-bc09-4188-902a-57631bf52080
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonSeparator::AddToListBox
Adds a separator to the **Commands** list in the **Customize** dialog box.  
  
## Syntax  
  
```  
virtual int AddToListBox(  
   CMFCRibbonCommandsListBox* pWndListBox,  
   BOOL bDeep  
);  
```  
  
#### Parameters  
 [in] `pWndListBox`  
 A pointer to the **Commands** list where the separator is added.  
  
 [in] `bDeep`  
 Ignored.  
  
## Return Value  
 Zero-based index to the string in the list box specified by `pWndListBox`.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonSeparator Class](../vs140/CMFCRibbonSeparator-Class.md)