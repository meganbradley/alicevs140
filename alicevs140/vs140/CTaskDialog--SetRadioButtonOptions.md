---
title: "CTaskDialog::SetRadioButtonOptions"
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
ms.assetid: 688066a5-6067-490b-a634-2d098f61bc5e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetRadioButtonOptions
Enables or disables a radio button.  
  
## Syntax  
  
```  
void SetRadioButtonOptions(  
   int nRadioButtonID,  
   BOOL bEnabled  
);  
```  
  
#### Parameters  
 [in] `nRadioButtonID`  
 The ID of the radio button control.  
  
 [in] `bEnabled`  
 `TRUE` to enable the radio button; `FALSE` to disable the radio button.  
  
## Remarks  
 This method throws an exception with the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro if `nRadioButtonID` is not a valid ID for a radio button.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#3)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::AddRadioButton](../vs140/CTaskDialog--AddRadioButton.md)   
 [CTaskDialog::GetSelectedRadioButtonID](../vs140/CTaskDialog--GetSelectedRadioButtonID.md)   
 [CTaskDialog::IsRadioButtonEnabled](../vs140/CTaskDialog--IsRadioButtonEnabled.md)   
 [CTaskDialog::SetDefaultRadioButton](../vs140/CTaskDialog--SetDefaultRadioButton.md)   
 [CTaskDialog::RemoveAllRadioButtons](../vs140/CTaskDialog--RemoveAllRadioButtons.md)