---
title: "CPropertyPage::OnWizardNext"
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
ms.assetid: 33878416-2554-4d78-8262-5c77444401bc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage::OnWizardNext
This member function is called by the framework when the user clicks on the Next button in a wizard.  
  
## Syntax  
  
```  
  
virtual LRESULT OnWizardNext();  
  
```  
  
## Return Value  
 0 to automatically advance to the next page; –1 to prevent the page from changing. To jump to a page other than the next one, return the identifier of the dialog to be displayed.  
  
## Remarks  
 Override this member function to specify some action the user must take when the Next button is pressed.  
  
 For more information on how to make a wizard-type property sheet, see [CPropertySheet::SetWizardMode](../vs140/CPropertySheet--SetWizardMode.md).  
  
## Example  
 [!CODE [NVC_MFCDocView#123](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#123)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet::SetWizardMode](../vs140/CPropertySheet--SetWizardMode.md)