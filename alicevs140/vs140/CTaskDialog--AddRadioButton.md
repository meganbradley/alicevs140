---
title: "CTaskDialog::AddRadioButton"
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
ms.assetid: df67d201-5d67-423f-9798-d57ef1fccba9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::AddRadioButton
Adds a radio button to the `CTaskDialog`.  
  
## Syntax  
  
```  
void CTaskDialog::AddRadioButton(  
   int nRadioButtonID,  
   const CString& strCaption,  
   BOOL bEnabled = TRUE  
);  
```  
  
#### Parameters  
 [in] `nRadioButtonID`  
 The identification number of the radio button.  
  
 [in] `strCaption`  
 The string that the `CTaskDialog` displays next to the radio button.  
  
 [in] `bEnabled`  
 A Boolean parameter that indicates whether the radio button is enabled.  
  
## Remarks  
 The radio buttons for the [CTaskDialog Class](../vs140/CTaskDialog-Class.md) enable you to gather information from the user. Use the function [CTaskDialog::GetSelectedRadioButtonID](../vs140/CTaskDialog--GetSelectedRadioButtonID.md) to determine which radio button is selected.  
  
 The `CTaskDialog` does not require that the `nRadioButtonID` parameters are unique for each radio button. However, you may experience unexpected behavior if you do not use a distinct identifier for each radio button.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#3)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::GetSelectedRadioButtonID](../vs140/CTaskDialog--GetSelectedRadioButtonID.md)   
 [CTaskDialog::LoadRadioButtons](../vs140/CTaskDialog--LoadRadioButtons.md)   
 [CTaskDialog::IsRadioButtonEnabled](../vs140/CTaskDialog--IsRadioButtonEnabled.md)   
 [CTaskDialog::SetRadioButtonOptions](../vs140/CTaskDialog--SetRadioButtonOptions.md)   
 [CTaskDialog::ClickRadioButton](../vs140/CTaskDialog--ClickRadioButton.md)   
 [CTaskDialog::RemoveAllRadioButtons](../vs140/CTaskDialog--RemoveAllRadioButtons.md)