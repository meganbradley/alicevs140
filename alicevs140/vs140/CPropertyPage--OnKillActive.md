---
title: "CPropertyPage::OnKillActive"
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
ms.assetid: 966ff914-0a85-4100-9d12-c703ea5e5ca9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::OnKillActive
This member function is called by the framework when the page is no longer the active page.  
  
## Syntax  
  
```  
  
virtual BOOL OnKillActive( );  
```  
  
## Return Value  
 Nonzero if data was updated successfully, otherwise 0.  
  
## Remarks  
 Override this member function to perform special data validation tasks.  
  
 The default implementation of this member function copies settings from the controls in the property page to the member variables of the property page. If the data was not updated successfully due to a dialog data validation (DDV) error, the page retains focus.  
  
 After this member function returns successfully, the framework will call the page's [OnOK](../vs140/CPropertyPage--OnOK.md) function.  
  
## Example  
 [!CODE [NVC_MFCDocView#115](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#115)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::UpdateData](../vs140/CWnd--UpdateData.md)   
 [CPropertyPage::OnOK](../vs140/CPropertyPage--OnOK.md)   
 [CPropertyPage::OnSetActive](../vs140/CPropertyPage--OnSetActive.md)