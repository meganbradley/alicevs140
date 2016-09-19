---
title: "CTaskDialog::SetMainInstruction"
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
ms.assetid: a5283297-2a64-4b94-8e72-cf17e7056a27
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetMainInstruction
Updates the main instruction of the `CTaskDialog`.  
  
## Syntax  
  
```  
void SetMainInstruction(  
   const CString& strInstructions  
);  
```  
  
#### Parameters  
 [in] `strInstructions`  
 The new main instruction.  
  
## Remarks  
 The main instruction of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md) is text displayed to the user in a large bold font. It is located in the dialog box underneath the title bar.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#7)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)