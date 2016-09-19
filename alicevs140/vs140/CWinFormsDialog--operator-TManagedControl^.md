---
title: "CWinFormsDialog::operator TManagedControl^"
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
ms.assetid: 9ff688f2-92dc-4342-958f-4c8f6e2e1fff
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinFormsDialog::operator TManagedControl^
Casts a type as a reference to a Windows Forms user control.  
  
## Syntax  
  
```  
inline operator TManagedControl^( ) const throw( );  
```  
  
## Remarks  
 This operator casts a type as a reference to a <xref:System.Windows.Forms.UserControl?qualifyHint=False> control. It is used to pass a `CWinFormsDialog<``TManagedControl``>` dialog box to functions that accept a pointer to a Windows Forms user control object.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 <xref:System.Windows.Forms.UserControl?qualifyHint=False>   
 <xref:System.Windows.Forms.Form?qualifyHint=False>   
 [CWinFormsDialog Overview](../Topic/CWinFormsDialog%20Class.md)