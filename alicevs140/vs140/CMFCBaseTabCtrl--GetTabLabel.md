---
title: "CMFCBaseTabCtrl::GetTabLabel"
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
ms.assetid: b7069046-c598-40da-ac2a-1cdeee7d75ad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabLabel
Retrieves the text of a tab label.  
  
## Syntax  
  
```  
virtual BOOL GetTabLabel(  
   int iTab,  
   CString& strLabel  
) const;  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of the tab.  
  
 [out] `strLabel`  
 A reference to a `CString` object. This method stores the label of the tab in this parameter.  
  
## Return Value  
 `TRUE` if successful; `FALSE` otherwise.  
  
## Remarks  
 This method fails if the index `iTab` is invalid.  
  
 You set the label for a tab when you create the tab by using [CMFCBaseTabCtrl::AddTab](../vs140/CMFCBaseTabCtrl--AddTab.md). You can also change the label after creation with the method [CMFCBaseTabCtrl::SetTabLabel](../vs140/CMFCBaseTabCtrl--SetTabLabel.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::SetTabLabel](../vs140/CMFCBaseTabCtrl--SetTabLabel.md)