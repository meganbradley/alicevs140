---
title: "CTaskDialog::GetSelectedCommandControlID"
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
ms.assetid: ee405234-7f6f-44d7-9aa2-63c6e7d6020f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::GetSelectedCommandControlID
Returns the selected command button control.  
  
## Syntax  
  
```  
int GetSelectedCommandControlID() const;  
```  
  
## Return Value  
 The ID of the currently selected command button control.  
  
## Remarks  
 You do not have to use this method to retrieve the ID of the command button that the user selected. That ID is returned by either [CTaskDialog::DoModal](../vs140/CTaskDialog--DoModal.md) or [CTaskDialog::ShowDialog](../vs140/CTaskDialog--ShowDialog.md).  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#2)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::AddCommandControl](../vs140/CTaskDialog--AddCommandControl.md)   
 [CTaskDialog::SetCommandControlOptions](../vs140/CTaskDialog--SetCommandControlOptions.md)   
 [CTaskDialog::IsCommandControlEnabled](../vs140/CTaskDialog--IsCommandControlEnabled.md)   
 [CTaskDialog::SetDefaultCommandControl](../vs140/CTaskDialog--SetDefaultCommandControl.md)   
 [CTaskDialog::RemoveAllCommandControls](../vs140/CTaskDialog--RemoveAllCommandControls.md)