---
title: "CEdit::GetLine"
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
ms.assetid: 56f1a1c3-7ee8-4378-ace5-e34992c58987
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::GetLine
Call this function to retrieve a line of text from an edit control and places it in `lpszBuffer`.  
  
## Syntax  
  
```  
  
      int GetLine(  
   int nIndex,  
   LPTSTR lpszBuffer   
) const;  
int GetLine(  
   int nIndex,  
   LPTSTR lpszBuffer,  
   int nMaxLength   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the line number to retrieve from a multiple-line edit control. Line numbers are zero-based; a value of 0 specifies the first line. This parameter is ignored by a single-line edit control.  
  
 `lpszBuffer`  
 Points to the buffer that receives a copy of the line. The first word of the buffer must specify the maximum number of characters that can be copied to the buffer.  
  
 `nMaxLength`  
 Specifies the maximum number of bytes that can be copied to the buffer. `GetLine` places this value in the first word of `lpszBuffer` before making the call to Windows.  
  
## Return Value  
 The number of bytes actually copied. The return value is 0 if the line number specified by `nIndex` is greater than the number of lines in the edit control.  
  
## Remarks  
 The copied line does not contain a null-termination character.  
  
 For more information, see [EM_GETLINE](http://msdn.microsoft.com/library/windows/desktop/bb761584) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEdit::GetLineCount](../vs140/CEdit--GetLineCount.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::LineLength](../vs140/CEdit--LineLength.md)   
 [CWnd::GetWindowText](../vs140/CWnd--GetWindowText.md)