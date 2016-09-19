---
title: "CTaskDialog::GetSelectedRadioButtonID"
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
ms.assetid: 84aa343a-8a6f-4d4a-b9ae-d242d0f640eb
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::GetSelectedRadioButtonID
Returns the selected radio button.  
  
## Syntax  
  
```  
int GetSelectedRadioButtonID() const;  
```  
  
## Return Value  
 The ID of the selected radio button.  
  
## Remarks  
 You can use this method after the user closes the dialog box to retrieve the selected radio button.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#3)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::AddRadioButton](../vs140/CTaskDialog--AddRadioButton.md)   
 [CTaskDialog::SetRadioButtonOptions](../vs140/CTaskDialog--SetRadioButtonOptions.md)   
 [CTaskDialog::IsRadioButtonEnabled](../vs140/CTaskDialog--IsRadioButtonEnabled.md)   
 [CTaskDialog::SetDefaultRadioButton](../vs140/CTaskDialog--SetDefaultRadioButton.md)   
 [CTaskDialog::RemoveAllRadioButtons](../vs140/CTaskDialog--RemoveAllRadioButtons.md)