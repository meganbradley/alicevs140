---
title: "CWindow::SetWindowText"
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
ms.assetid: 99740ae8-9799-44e3-b640-c5b0e1f6071b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetWindowText
Changes the window's text.  
  
## Syntax  
  
```  
  
      BOOL SetWindowText(  
   LPCTSTR lpszString   
) throw();  
```  
  
## Remarks  
 See [SetWindowText](http://msdn.microsoft.com/library/windows/desktop/ms633546) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#34](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#34)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetWindowText](../vs140/CWindow--GetWindowText.md)