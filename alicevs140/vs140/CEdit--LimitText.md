---
title: "CEdit::LimitText"
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
ms.assetid: e0176cc1-c2b6-4573-a3e4-8aac2b32fe43
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::LimitText
Call this function to limit the length of the text that the user may enter into an edit control.  
  
## Syntax  
  
```  
  
      void LimitText(  
   int nChars = 0   
);  
```  
  
#### Parameters  
 `nChars`  
 Specifies the length (in bytes) of the text that the user can enter. If this parameter is 0, the text length is set to **UINT_MAX** bytes. This is the default behavior.  
  
## Remarks  
 Changing the text limit restricts only the text the user can enter. It has no effect on any text already in the edit control, nor does it affect the length of the text copied to the edit control by the [SetWindowText](../vs140/CWnd--SetWindowText.md) member function in `CWnd`. If an application uses the `SetWindowText` function to place more text into an edit control than is specified in the call to `LimitText`, the user can delete any of the text within the edit control. However, the text limit will prevent the user from replacing the existing text with new text, unless deleting the current selection causes the text to fall below the text limit.  
  
> [!NOTE]
>  In Win32 (Windows NT and Windows 95/98), [SetLimitText](../vs140/CEdit--SetLimitText.md) replaces this function.  
  
 For more information, see [EM_LIMITTEXT](http://msdn.microsoft.com/library/windows/desktop/bb761607) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#17)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetWindowText](../vs140/CWnd--SetWindowText.md)   
 [CEdit::GetLimitText](../vs140/CEdit--GetLimitText.md)   
 [CEdit::SetLimitText](../vs140/CEdit--SetLimitText.md)