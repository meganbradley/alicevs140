---
title: "CEdit::SetLimitText"
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
ms.assetid: 71a587f2-075a-4bba-b500-7ce4e72246f2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::SetLimitText
Call this member function to set the text limit for this `CEdit` object.  
  
## Syntax  
  
```  
  
      void SetLimitText(  
   UINT nMax   
);  
```  
  
#### Parameters  
 `nMax`  
 The new text limit, in characters.  
  
## Remarks  
 The text limit is the maximum amount of text, in characters, that the edit control can accept.  
  
 Changing the text limit restricts only the text the user can enter. It has no effect on any text already in the edit control, nor does it affect the length of the text copied to the edit control by the [SetWindowText](../vs140/CWnd--SetWindowText.md) member function in `CWnd`. If an application uses the `SetWindowText` function to place more text into an edit control than is specified in the call to `LimitText`, the user can delete any of the text within the edit control. However, the text limit will prevent the user from replacing the existing text with new text, unless deleting the current selection causes the text to fall below the text limit.  
  
 This function replaces [LimitText](../vs140/CEdit--LimitText.md) in Win32.  
  
 For more information, see [EM_SETLIMITTEXT](http://msdn.microsoft.com/library/windows/desktop/bb761647) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEditView::GetEditCtrl](../vs140/CEditView--GetEditCtrl.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::GetLimitText](../vs140/CEdit--GetLimitText.md)   
 [CEdit::LimitText](../vs140/CEdit--LimitText.md)