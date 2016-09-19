---
title: "CMFCMaskedEdit::GetWindowText"
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
ms.assetid: d8b07704-8dda-4021-a91f-4de611a7f2a3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMaskedEdit::GetWindowText
Retrieves validated text from the masked edit control.  
  
## Syntax  
  
```  
int GetWindowText(  
   LPTSTR lpszStringBuf,  
   int nMaxCount   
) const;  
void GetWindowText(  
   CString& rstrString   
) const;  
```  
  
#### Parameters  
 [out] `lpszStringBuf`  
 A pointer to a buffer that receives the text from the edit control.  
  
 [in] `nMaxCount`  
 The maximum number of characters to receive.  
  
 [out] `rstrString`  
 A reference to the string object that receives the text from the edit control.  
  
## Return Value  
 The first method overload returns the number of bytes of the string that is copied to the `lpszStringBuf` parameter buffer; 0 if the masked edit control has no text.  
  
## Remarks  
 This method copies the text from the masked edit control to the `lpszStringBuf` buffer or the `rstrString` string.  
  
 This method redefines [CWnd::GetWindowText](../vs140/CWnd--GetWindowText.md).  
  
## Requirements  
 **Header:** afxmaskededit.h  
  
## See Also  
 [CMFCMaskedEdit Class](../vs140/CMFCMaskedEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)