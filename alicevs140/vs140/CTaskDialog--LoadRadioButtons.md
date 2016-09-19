---
title: "CTaskDialog::LoadRadioButtons"
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
ms.assetid: ed035c7b-8736-4144-8c73-ba03205ca58d
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::LoadRadioButtons
Adds radio button controls by using data from the string table.  
  
## Syntax  
  
```  
void LoadRadioButtons(  
   int nIDRadioButtonsFirst,  
   int nIDRadioButtonsLast  
);  
```  
  
#### Parameters  
 [in] `nIDRadioButtonsFirst`  
 The string ID of the first radio button.  
  
 [in] `nIDRadioButtonsLast`  
 The string ID of the last radio button.  
  
## Remarks  
 This method creates radio buttons by using data from the resource file of your application. The string table in the resource file has several strings with associated string IDs. New radio buttons added by using this method use the string for the radio button's caption and the string ID for the radio button's ID. The range of strings selected is provided by `nIDRadioButtonsFirst` and `nRadioButtonsLast`, inclusive. If there is an empty entry in the range, the method does not add a radio button for that entry.  
  
 By default, new radio buttons are enabled.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#3)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::AddRadioButton](../vs140/CTaskDialog--AddRadioButton.md)   
 [CTaskDialog::SetRadioButtonOptions](../vs140/CTaskDialog--SetRadioButtonOptions.md)   
 [CTaskDialog::RemoveAllRadioButtons](../vs140/CTaskDialog--RemoveAllRadioButtons.md)