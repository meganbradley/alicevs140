---
title: "CPropertyPage::OnOK"
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
ms.assetid: a1f1e74b-2dc0-426d-9fed-bad120bdc521
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::OnOK
This member function is called by the framework when the user chooses either the OK or the Apply Now button, immediately after the framework calls [OnKillActive](../vs140/CPropertyPage--OnKillActive.md).  
  
## Syntax  
  
```  
  
virtual void OnOK( );  
```  
  
## Remarks  
 When the user chooses either the OK or the Apply Now button, the framework receives the [PSN_APPLY](http://msdn.microsoft.com/library/windows/desktop/bb774552) notification from the property page. The call to `OnOK` won't be made if you call [CPropertySheet::PressButton](../vs140/CPropertySheet--PressButton.md) because the property page does not send the notification in that case.  
  
 Override this member function to implement additional behavior specific to the currently active page when user dismisses the entire property sheet.  
  
 The default implementation of this member function marks the page as "clean" to reflect that the data was updated in the `OnKillActive` function.  
  
## Example  
 [!CODE [NVC_MFCDocView#116](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#116)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::OnOK](../vs140/CDialog--OnOK.md)   
 [CPropertyPage::OnKillActive](../vs140/CPropertyPage--OnKillActive.md)