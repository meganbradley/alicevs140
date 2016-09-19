---
title: "CEdit::LineIndex"
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
ms.assetid: 1ef73eff-200a-4509-8e0e-ce4e603e679f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::LineIndex
Call this function to retrieve the character index of a line within a multiple-line edit control.  
  
## Syntax  
  
```  
  
      int LineIndex(  
   int nLine = -1   
) const;  
```  
  
#### Parameters  
 `nLine`  
 Contains the index value for the desired line in the text of the edit control, or contains –1. If `nLine` is –1, it specifies the current line, that is, the line that contains the caret.  
  
## Return Value  
 The character index of the line specified in `nLine` or –1 if the specified line number is greater than the number of lines in the edit control.  
  
## Remarks  
 The character index is the number of characters from the beginning of the edit control to the specified line.  
  
 This member function is only processed by multiple-line edit controls.  
  
 For more information, see [EM_LINEINDEX](http://msdn.microsoft.com/library/windows/desktop/bb761611) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#19)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::LineFromChar](../vs140/CEdit--LineFromChar.md)