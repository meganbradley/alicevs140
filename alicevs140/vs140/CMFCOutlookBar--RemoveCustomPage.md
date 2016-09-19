---
title: "CMFCOutlookBar::RemoveCustomPage"
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
ms.assetid: 7df12d3d-d3c4-4c69-aa4c-ef15baf28026
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::RemoveCustomPage
Removes a custom Outlook bar tab page.  
  
## Syntax  
  
```  
BOOL RemoveCustomPage(  
   UINT uiPage,  
   CMFCOutlookBarTabCtrl* pTargetWnd   
);  
```  
  
#### Parameters  
 [in] `uiPage`  
 Zero-based index of the page in the parent Outlook window.  
  
 [in] `pTargetWnd`  
 Pointerto the parent Outlook window.  
  
## Return Value  
 Nonzero if the custom page has been removed successfully; otherwise 0.  
  
## Remarks  
 Call this function to delete custom pages. When the page is removed its control ID is returned to the pool of available IDs.  
  
 You must provide a pointer to [CMFCOutlookBarTabCtrl Class](../vs140/CMFCOutlookBarTabCtrl-Class.md) object in which the page to be removed currently resides. Note that a user can move detachable pages between different Outlook bars, but the information about a custom page resides in the Outlook bar object for which you have called [CMFCOutlookBar::CreateCustomPage](../vs140/CMFCOutlookBar--CreateCustomPage.md).  
  
 Use [CBaseTabbedPane::GetUnderlyingWindow](../vs140/CBaseTabbedPane--GetUnderlyingWindow.md) to obtain a pointer to the Outlook window.  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)