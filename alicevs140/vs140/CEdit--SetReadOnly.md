---
title: "CEdit::SetReadOnly"
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
ms.assetid: 88d3547e-f4aa-4ec7-b41c-54f132fa5b05
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::SetReadOnly
Calls this function to set the read-only state of an edit control.  
  
## Syntax  
  
```  
  
      BOOL SetReadOnly(  
   BOOL bReadOnly = TRUE   
);  
```  
  
#### Parameters  
 `bReadOnly`  
 Specifies whether to set or remove the read-only state of the edit control. A value of **TRUE** sets the state to read-only; a value of **FALSE** sets the state to read/write.  
  
## Return Value  
 Nonzero if the operation is successful, or 0 if an error occurs.  
  
## Remarks  
 The current setting can be found by testing the [ES_READONLY](../vs140/Edit-Styles.md) flag in the return value of [CWnd::GetStyle](../vs140/CWnd--GetStyle.md).  
  
 For more information, see [EM_SETREADONLY](http://msdn.microsoft.com/library/windows/desktop/bb761655) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#23)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetStyle](../vs140/CWnd--GetStyle.md)