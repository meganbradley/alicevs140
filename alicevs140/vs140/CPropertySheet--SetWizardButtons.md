---
title: "CPropertySheet::SetWizardButtons"
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
ms.assetid: 97484c08-23b6-4033-a441-22f3734be0c2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::SetWizardButtons
Enables or disables the Back, Next, or Finish button in a wizard property sheet.  
  
## Syntax  
  
```  
  
      void SetWizardButtons(  
   DWORD dwFlags   
);  
```  
  
#### Parameters  
 `dwFlags`  
 A set of flags that customize the function and appearance of the wizard buttons. This parameter can be a combination of the following values:  
  
-   **PSWIZB_BACK** Back button  
  
-   **PSWIZB_NEXT** Next button  
  
-   **PSWIZB_FINISH** Finish button  
  
-   **PSWIZB_DISABLEDFINISH** Disabled Finish button  
  
## Remarks  
 Call `SetWizardButtons` only after the dialog is open; you can't call `SetWizardButtons` before you call [DoModal](../vs140/CPropertySheet--DoModal.md). Typically, you should call `SetWizardButtons` from [CPropertyPage::OnSetActive](../vs140/CPropertyPage--OnSetActive.md).  
  
 If you want to change the text on the Finish button or hide the Next and Back buttons once the user has completed the wizard, call [SetFinishText](../vs140/CPropertySheet--SetFinishText.md). Note that the same button is shared for Finish and Next. You can display a Finish or a Next button at one time, but not both.  
  
## Example  
 A `CPropertySheet` has three wizard property pages: `CStylePage`, `CColorPage`, and `CShapePage`.  The code fragment below shows how to enable and disable the **Back** and **Next** buttons on the wizard property page.  
  
 [!CODE [NVC_MFCDocView#140](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#140)]  
  
 [!CODE [NVC_MFCDocView#141](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#141)]  
  
 [!CODE [NVC_MFCDocView#138](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#138)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)