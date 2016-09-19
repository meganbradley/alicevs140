---
title: "CEdit::GetSel"
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
ms.assetid: 62059750-6ac6-47fb-8c17-46b082d14797
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::GetSel
Call this function to get the starting and ending character positions of the current selection (if any) in an edit control, using either the return value or the parameters.  
  
## Syntax  
  
```  
  
      DWORD GetSel( ) const;  
void GetSel(  
   int& nStartChar,  
   int& nEndChar   
) const;  
```  
  
#### Parameters  
 `nStartChar`  
 Reference to an integer that will receive the position of the first character in the current selection.  
  
 `nEndChar`  
 Reference to an integer that will receive the position of the first nonselected character past the end of the current selection.  
  
## Return Value  
 The version that returns a `DWORD` returns a value that contains the starting position in the low-order word and the position of the first nonselected character after the end of the selection in the high-order word.  
  
## Remarks  
 For more information, see [EM_GETSEL](http://msdn.microsoft.com/library/windows/desktop/bb761598) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#15)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::SetSel](../vs140/CEdit--SetSel.md)