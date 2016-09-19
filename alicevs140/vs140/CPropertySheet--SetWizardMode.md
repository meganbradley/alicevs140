---
title: "CPropertySheet::SetWizardMode"
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
ms.assetid: 31746ad9-0678-4eac-9eac-ab1bf20a51c9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::SetWizardMode
Establishes a property page as a wizard.  
  
## Syntax  
  
```  
  
void SetWizardMode( );  
  
```  
  
## Remarks  
 A key characteristic of a wizard property page is that the user navigates using Next or Finish, Back, and Cancel buttons instead of tabs.  
  
 Call `SetWizardMode` before calling [DoModal](../vs140/CPropertySheet--DoModal.md). After you call `SetWizardMode`, `DoModal` will return either **ID_WIZFINISH** (if the user closes with the Finish button) or **IDCANCEL**.  
  
 `SetWizardMode` sets the PSH_WIZARD flag.  
  
## Example  
 [!CODE [NVC_MFCDocView#142](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#142)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::DoModal](../vs140/CPropertySheet--DoModal.md)