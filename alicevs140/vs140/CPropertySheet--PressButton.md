---
title: "CPropertySheet::PressButton"
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
ms.assetid: 4c62da59-da6e-46af-9115-816e67ddd032
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::PressButton
Simulates the choice of the specified button in a property sheet.  
  
## Syntax  
  
```  
  
      void PressButton(  
   int nButton   
);  
```  
  
#### Parameters  
 `nButton`  
 nButton : Identifies the button to be pressed. This parameter can be one of the following values:  
  
-   **PSBTN_BACK** Chooses the Back button.  
  
-   **PSBTN_NEXT** Chooses the Next button.  
  
-   **PSBTN_FINISH** Chooses the Finish button.  
  
-   **PSBTN_OK** Chooses the OK button.  
  
-   **PSBTN_APPLYNOW** Chooses the Apply Now button.  
  
-   **PSBTN_CANCEL** Chooses the Cancel button.  
  
-   **PSBTN_HELP** Chooses the Help button.  
  
## Remarks  
 See [PSM_PRESSBUTTON](http://msdn.microsoft.com/library/windows/desktop/bb774597) for more information about the Windows SDK Pressbutton message.  
  
 A call to `PressButton` will not send the [PSN_APPLY](http://msdn.microsoft.com/library/windows/desktop/bb774552) notification from a property page to the framework. To send this notification, call [CPropertyPage::OnOK](../vs140/CPropertyPage--OnOK.md).  
  
## Example  
 [!CODE [NVC_MFCDocView#137](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#137)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)