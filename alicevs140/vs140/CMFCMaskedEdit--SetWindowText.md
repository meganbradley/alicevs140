---
title: "CMFCMaskedEdit::SetWindowText"
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
ms.assetid: eb16eb91-884a-4d12-baaa-f761e5741134
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMaskedEdit::SetWindowText
Displays a prompt in the masked edit control.  
  
## Syntax  
  
```  
void SetWindowText(  
   LPCTSTR lpszString   
);  
```  
  
#### Parameters  
 [in] `lpszString`  
 Points to a null-terminated string that will be used as a prompt.  
  
## Remarks  
 This method sets the control text.  
  
 This method redefines [CWnd::SetWindowText](../vs140/CWnd--SetWindowText.md).  
  
## Requirements  
 **Header:** afxmaskededit.h  
  
## See Also  
 [CMFCMaskedEdit Class](../vs140/CMFCMaskedEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)