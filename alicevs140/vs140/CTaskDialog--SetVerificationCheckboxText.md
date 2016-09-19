---
title: "CTaskDialog::SetVerificationCheckboxText"
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
ms.assetid: 6659cfc7-1e00-41fc-bb4f-9b0b1f1feff8
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetVerificationCheckboxText
Sets the text that is displayed to the right of the verification check box.  
  
## Syntax  
  
```  
void SetVerificationCheckboxText(  
   CString& strVerificationText  
);  
```  
  
#### Parameters  
 [in] `strVerificationText`  
 The text that this method displays next to the verification check box.  
  
## Remarks  
 This method throws an exception with the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro if this instance of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md) is already displayed.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#5)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetVerificationCheckbox](../vs140/CTaskDialog--SetVerificationCheckbox.md)