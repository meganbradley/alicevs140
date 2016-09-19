---
title: "CEdit::FmtLines"
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
ms.assetid: 0b7a2c23-5770-46ae-ae4a-8af18e00a7f9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::FmtLines
Call this function to set the inclusion of soft line-break characters on or off within a multiple-line edit control.  
  
## Syntax  
  
```  
  
      BOOL FmtLines(  
   BOOL bAddEOL   
);  
```  
  
#### Parameters  
 *bAddEOL*  
 Specifies whether soft line-break characters are to be inserted. A value of **TRUE** inserts the characters; a value of **FALSE** removes them.  
  
## Return Value  
 Nonzero if any formatting occurs; otherwise 0.  
  
## Remarks  
 A soft line break consists of two carriage returns and a linefeed inserted at the end of a line that is broken because of word wrapping. A hard line break consists of one carriage return and a linefeed. Lines that end with a hard line break are not affected by `FmtLines`.  
  
 Windows will only respond if the `CEdit` object is a multiple-line edit control.  
  
 `FmtLines` only affects the buffer returned by [GetHandle](../vs140/CEdit--GetHandle.md) and the text returned by [WM_GETTEXT](http://msdn.microsoft.com/library/windows/desktop/ms632627). It has no impact on the display of the text within the edit control.  
  
 For more information, see [EM_FMTLINES](http://msdn.microsoft.com/library/windows/desktop/bb761570) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#8)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::GetHandle](../vs140/CEdit--GetHandle.md)   
 [CWnd::GetWindowText](../vs140/CWnd--GetWindowText.md)