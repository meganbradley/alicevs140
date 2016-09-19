---
title: "CWindow::GetDlgItemInt"
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
ms.assetid: e5dcc47a-cca2-4219-b428-1c3f05b6e7df
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetDlgItemInt
Translates a control's text to an integer.  
  
## Syntax  
  
```  
  
      UINT GetDlgItemInt(  
   int nID,  
   BOOL* lpTrans = NULL,  
   BOOL bSigned = TRUE   
) const throw();  
```  
  
## Remarks  
 See [GetDlgItemInt](http://msdn.microsoft.com/library/windows/desktop/ms645485) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetDlgItemInt](../vs140/CWindow--SetDlgItemInt.md)   
 [CWindow::GetDlgItemText](../vs140/CWindow--GetDlgItemText.md)