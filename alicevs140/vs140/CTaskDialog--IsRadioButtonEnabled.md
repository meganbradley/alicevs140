---
title: "CTaskDialog::IsRadioButtonEnabled"
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
ms.assetid: 53ba6e89-ccde-4531-9133-7578f9b77055
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::IsRadioButtonEnabled
Determines whether a radio button is enabled.  
  
## Syntax  
  
```  
BOOL IsRadioButtonEnabled(  
   int nRadioButtonID  
) const;  
```  
  
#### Parameters  
 [in] `nRadioButtonID`  
 The ID of the radio button to test.  
  
## Return Value  
 `TRUE` if the radio button is enabled, `FALSE` if it is not.  
  
## Remarks  
 If `nRadioButtonID` is not a valid identifier for a radio button, this method throws an exception.  
  
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
 [CTaskDialog::SetDefaultRadioButton](../vs140/CTaskDialog--SetDefaultRadioButton.md)   
 [CTaskDialog::RemoveAllRadioButtons](../vs140/CTaskDialog--RemoveAllRadioButtons.md)