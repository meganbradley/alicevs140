---
title: "CEdit::SetPasswordChar"
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
ms.assetid: 9c31a1d7-1d00-4844-9368-82735b16bcff
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::SetPasswordChar
Call this function to set or remove a password character displayed in an edit control when the user types text.  
  
## Syntax  
  
```  
  
      void SetPasswordChar(  
   TCHAR ch   
);  
```  
  
#### Parameters  
 *ch*  
 Specifies the character to be displayed in place of the character typed by the user. If *ch* is 0, the actual characters typed by the user are displayed.  
  
## Remarks  
 When a password character is set, that character is displayed for each character the user types.  
  
 This member function has no effect on a multiple-line edit control.  
  
 When the `SetPasswordChar` member function is called, `CEdit` will redraw all visible characters using the character specified by *ch*.  
  
 If the edit control is created with the [ES_PASSWORD](../vs140/Edit-Styles.md) style, the default password character is set to an asterisk (**\***). This style is removed if `SetPasswordChar` is called with *ch* set to 0.  
  
 For more information, see [EM_SETPASSWORDCHAR](http://msdn.microsoft.com/library/windows/desktop/bb761653) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#16)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::GetPasswordChar](../vs140/CEdit--GetPasswordChar.md)