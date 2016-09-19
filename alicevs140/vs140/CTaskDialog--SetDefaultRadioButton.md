---
title: "CTaskDialog::SetDefaultRadioButton"
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
ms.assetid: ce5115fb-4bbc-4214-bd19-5c63a4b1b93b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetDefaultRadioButton
Specifies the default radio button.  
  
## Syntax  
  
```  
void SetDefaultRadioButton(  
   int nRadioButtonID  
);  
```  
  
#### Parameters  
 [in] `nRadioButtonID`  
 The ID of the radio button to be the default.  
  
## Remarks  
 The default radio button is the button that is selected when the `CTaskDialog` is first displayed to the user.  
  
 This method throws an exception if it cannot find the radio button specified by `nRadioButtonID`.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#3)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::AddRadioButton](../vs140/CTaskDialog--AddRadioButton.md)   
 [CTaskDialog::SetRadioButtonOptions](../vs140/CTaskDialog--SetRadioButtonOptions.md)   
 [CTaskDialog::GetSelectedRadioButtonID](../vs140/CTaskDialog--GetSelectedRadioButtonID.md)   
 [CTaskDialog::IsRadioButtonEnabled](../vs140/CTaskDialog--IsRadioButtonEnabled.md)   
 [CTaskDialog::RemoveAllRadioButtons](../vs140/CTaskDialog--RemoveAllRadioButtons.md)