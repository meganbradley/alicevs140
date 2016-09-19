---
title: "CTaskDialog::GetVerificationCheckboxState"
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
ms.assetid: cb78596a-a2a2-4d2b-89b8-7f4e067f82ba
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::GetVerificationCheckboxState
Retrieves the state of the verification check box.  
  
## Syntax  
  
```  
BOOL GetVerificationCheckboxState() const;  
```  
  
## Return Value  
 `TRUE` if the check box is checked, `FALSE` if it is not.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#5)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetVerificationCheckbox](../vs140/CTaskDialog--SetVerificationCheckbox.md)   
 [CTaskDialog::SetVerificationCheckboxText](../vs140/CTaskDialog--SetVerificationCheckboxText.md)