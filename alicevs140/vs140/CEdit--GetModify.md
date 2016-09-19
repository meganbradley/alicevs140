---
title: "CEdit::GetModify"
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
ms.assetid: e6925dcd-71ed-47bc-9133-502c49e43dd9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::GetModify
Call this function to determine whether the contents of an edit control have been modified.  
  
## Syntax  
  
```  
  
BOOL GetModify( ) const;  
```  
  
## Return Value  
 Nonzero if the edit-control contents have been modified; 0 if they have remained unchanged.  
  
## Remarks  
 Windows maintains an internal flag indicating whether the contents of the edit control have been changed. This flag is cleared when the edit control is first created and may also be cleared by calling the [SetModify](../vs140/CEdit--SetModify.md) member function.  
  
 For more information, see [EM_GETMODIFY](http://msdn.microsoft.com/library/windows/desktop/bb761592) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#13)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::SetModify](../vs140/CEdit--SetModify.md)