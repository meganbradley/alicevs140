---
title: "CEdit::GetLimitText"
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
ms.assetid: 50192248-8d98-4aae-923d-4c8b1149563b
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::GetLimitText
Call this member function to get the text limit for this `CEdit` object.  
  
## Syntax  
  
```  
  
UINT GetLimitText( ) const;  
  
```  
  
## Return Value  
 The current text limit, in bytes, for this `CEdit` object.  
  
## Remarks  
 The text limit is the maximum amount of text, in bytes, that the edit control can accept.  
  
> [!NOTE]
>  This member function is available beginning with Windows 95 and Windows NT 4.0.  
  
 For more information, see [EM_GETLIMITTEXT](http://msdn.microsoft.com/library/windows/desktop/bb761582) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#11)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::SetLimitText](../vs140/CEdit--SetLimitText.md)   
 [CEdit::LimitText](../vs140/CEdit--LimitText.md)