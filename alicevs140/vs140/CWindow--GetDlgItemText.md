---
title: "CWindow::GetDlgItemText"
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
ms.assetid: df2e1f60-6a57-46b3-b78c-5588c634a69d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetDlgItemText
Retrieves a control's text.  
  
## Syntax  
  
```  
  
      UINT GetDlgItemText(  
   int nID,  
   LPTSTR lpStr,  
   int nMaxCount   
) const throw();  
BOOL GetDlgItemText(  
   int nID,  
   BSTR& bstrText   
) const throw();  
```  
  
## Remarks  
 See [GetDlgItemText](http://msdn.microsoft.com/library/windows/desktop/ms645489) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 The second version of this method allows you to copy the control's text to a `BSTR`. This version returns **TRUE** if the text is successfully copied; otherwise, **FALSE**.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetDlgItemText](../vs140/CWindow--SetDlgItemText.md)   
 [CWindow::GetDlgItem](../vs140/CWindow--GetDlgItem.md)