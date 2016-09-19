---
title: "CTaskDialog::SetVerificationCheckbox"
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
ms.assetid: 2248d37d-7cf3-4e3c-89ef-dc9bb2e2a9d0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetVerificationCheckbox
Sets the checked state of the verification check box.  
  
## Syntax  
  
```  
void SetVerificationCheckbox(  
   BOOL bChecked  
);  
```  
  
#### Parameters  
 [in] `bChecked`  
 `TRUE` to have the verification check box selected when the `CTaskDialog` is displayed; `FALSE` to have the verification check box unselected when the `CTaskDialog` is displayed.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#5)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetVerificationCheckboxText](../vs140/CTaskDialog--SetVerificationCheckboxText.md)