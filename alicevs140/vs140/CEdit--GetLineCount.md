---
title: "CEdit::GetLineCount"
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
ms.assetid: d892c86d-deb0-416d-beec-45694911dae9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::GetLineCount
Call this function to retrieve the number of lines in a multiple-line edit control.  
  
## Syntax  
  
```  
  
int GetLineCount( ) const;  
```  
  
## Return Value  
 An integer containing the number of lines in the multiple-line edit control. If no text has been entered into the edit control, the return value is 1.  
  
## Remarks  
 `GetLineCount` is only processed by multiple-line edit controls.  
  
 For more information, see [EM_GETLINECOUNT](http://msdn.microsoft.com/library/windows/desktop/bb761586) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#12)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)