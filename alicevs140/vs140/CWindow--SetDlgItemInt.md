---
title: "CWindow::SetDlgItemInt"
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
ms.assetid: c91d662b-de56-4f15-a6b5-a8bdf226d4c0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetDlgItemInt
Changes a control's text to the string representation of an integer value.  
  
## Syntax  
  
```  
  
      BOOL SetDlgItemInt(  
   int nID,  
   UINT nValue,  
   BOOL bSigned = TRUE   
) throw();  
```  
  
## Remarks  
 See [SetDlgItemInt](http://msdn.microsoft.com/library/windows/desktop/ms645518) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetDlgItemInt](../vs140/CWindow--GetDlgItemInt.md)   
 [CWindow::SetDlgItemText](../vs140/CWindow--SetDlgItemText.md)