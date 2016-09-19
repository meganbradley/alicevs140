---
title: "CTaskDialog::SetContent"
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
ms.assetid: b0a9f8ae-4972-45d2-be91-61e01cf58724
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetContent
Updates the content of the `CTaskDialog`.  
  
## Syntax  
  
```  
void SetContent(  
   const CString& strContent  
);  
```  
  
#### Parameters  
 [in] `strContent`  
 The string to display to the user.  
  
## Remarks  
 The content of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md) is the text that is displayed to the user in the main section of the dialog box.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#7)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetWindowTitle](../vs140/CTaskDialog--SetWindowTitle.md)   
 [CTaskDialog::SetMainInstruction](../vs140/CTaskDialog--SetMainInstruction.md)   
 [CTaskDialog::SetFooterText](../vs140/CTaskDialog--SetFooterText.md)   
 [CTaskDialog::SetExpansionArea](../vs140/CTaskDialog--SetExpansionArea.md)   
 [CTaskDialog::SetMainIcon](../vs140/CTaskDialog--SetMainIcon.md)   
 [CTaskDialog::SetFooterIcon](../vs140/CTaskDialog--SetFooterIcon.md)