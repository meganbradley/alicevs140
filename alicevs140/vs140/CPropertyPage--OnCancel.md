---
title: "CPropertyPage::OnCancel"
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
ms.assetid: dd40bd2b-7782-46da-938f-ddf16a42decc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::OnCancel
This member function is called by the framework when the Cancel button is selected.  
  
## Syntax  
  
```  
  
virtual void OnCancel( );  
```  
  
## Remarks  
 Override this member function to perform Cancel button actions. The default negates any changes that have been made.  
  
## Example  
 [!CODE [NVC_MFCDocView#114](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#114)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertyPage::OnApply](../vs140/CPropertyPage--OnApply.md)   
 [CDialog::OnCancel](../vs140/CDialog--OnCancel.md)   
 [CPropertyPage::OnOK](../vs140/CPropertyPage--OnOK.md)