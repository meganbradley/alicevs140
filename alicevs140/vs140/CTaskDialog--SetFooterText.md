---
title: "CTaskDialog::SetFooterText"
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
ms.assetid: c3101e6b-fbb8-4670-8fa4-5c9abd7548a7
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetFooterText
Updates the text on the footer of the `CTaskDialog`.  
  
## Syntax  
  
```  
void SetFooterText(  
   const CString& strFooterText  
);  
```  
  
#### Parameters  
 [in] `strFooterText`  
 The new text for the footer.  
  
## Remarks  
 The footer icon appears next to the footer text on the bottom of the `CTaskDialog`. You can change the footer icon with [CTaskDialog::SetFooterIcon](../vs140/CTaskDialog--SetFooterIcon.md).  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#7)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetFooterIcon](../vs140/CTaskDialog--SetFooterIcon.md)