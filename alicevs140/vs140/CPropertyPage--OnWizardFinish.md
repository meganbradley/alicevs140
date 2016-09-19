---
title: "CPropertyPage::OnWizardFinish"
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
ms.assetid: 933318e6-f4dd-401c-9ed2-fd2964a2e419
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::OnWizardFinish
This member function is called by the framework when the user clicks on the Finish button in a wizard.  
  
## Syntax  
  
```  
  
virtual BOOL OnWizardFinish( );  
  
```  
  
## Return Value  
 Nonzero if the property sheet is destroyed when the wizard finishes; otherwise zero.  
  
## Remarks  
 When a user clicks the **Finish** button in a wizard, the framework calls this function; when `OnWizardFinish` returns **TRUE** (a nonzero value), the property sheet is able to be destroyed (but is not actually destroyed). Call `DestroyWindow` to destroy the property sheet. Do not call `DestroyWindow` from `OnWizardFinish`; doing so will cause heap corruption or other errors.  
  
 You can override this member function to specify some action the user must take when the Finish button is pressed. When overriding this function, return **FALSE** to prevent the property sheet from being destroyed.  
  
 For more information about notification messages sent when the user presses the Finish button in a wizard property sheet, see [PSN_WIZFINISH](http://msdn.microsoft.com/library/windows/desktop/bb774571) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information on how to make a wizard-type property sheet, see [CPropertySheet::SetWizardMode](../vs140/CPropertySheet--SetWizardMode.md).  
  
## Example  
 [!CODE [NVC_MFCDocView#119](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#119)]  
  
 [!CODE [NVC_MFCDocView#120](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#120)]  
  
 [!CODE [NVC_MFCDocView#121](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#121)]  
  
 [!CODE [NVC_MFCDocView#122](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#122)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::SetWizardMode](../vs140/CPropertySheet--SetWizardMode.md)