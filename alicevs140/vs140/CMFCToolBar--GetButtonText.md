---
title: "CMFCToolBar::GetButtonText"
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
ms.assetid: 553e172e-7ddc-4a13-ae59-bbf659ad0824
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetButtonText
Returns the text label of a button that has a specified index.  
  
## Syntax  
  
```  
CString GetButtonText(  
   int nIndex   
) const;  
void GetButtonText(  
   int nIndex,  
   CString& rString   
) const;  
```  
  
#### Parameters  
 [in] `nIndex`  
 The index of a toolbar button.  
  
 [out] `rString`  
 The label text of the toolbar button.  
  
## Return Value  
 The label text of the toolbar button.  
  
## Remarks  
 Call [CMFCToolBar::SetButtonText](../vs140/CMFCToolBar--SetButtonText.md) or [CMFCToolBar::SetToolBarBtnText](../vs140/CMFCToolBar--SetToolBarBtnText.md) to set the text label.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)