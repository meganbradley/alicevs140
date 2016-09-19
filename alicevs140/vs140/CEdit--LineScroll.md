---
title: "CEdit::LineScroll"
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
ms.assetid: 4f1e6fa1-8bff-4ebc-8ff2-5a4446a3f6c1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::LineScroll
Call this function to scroll the text of a multiple-line edit control.  
  
## Syntax  
  
```  
  
      void LineScroll(  
   int nLines,  
   int nChars = 0   
);  
```  
  
#### Parameters  
 `nLines`  
 Specifies the number of lines to scroll vertically.  
  
 `nChars`  
 Specifies the number of character positions to scroll horizontally. This value is ignored if the edit control has either the **ES_RIGHT** or **ES_CENTER** style.  
  
## Remarks  
 This member function is processed only by multiple-line edit controls.  
  
 The edit control does not scroll vertically past the last line of text in the edit control. If the current line plus the number of lines specified by `nLines` exceeds the total number of lines in the edit control, the value is adjusted so that the last line of the edit control is scrolled to the top of the edit-control window.  
  
 `LineScroll` can be used to scroll horizontally past the last character of any line.  
  
 For more information, see [EM_LINESCROLL](http://msdn.microsoft.com/library/windows/desktop/bb761615) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEdit::GetFirstVisibleLine](../vs140/CEdit--GetFirstVisibleLine.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::LineIndex](../vs140/CEdit--LineIndex.md)