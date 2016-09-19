---
title: "CRichEditCtrl::GetTextMode"
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
ms.assetid: ab1cf392-8770-4bb6-91d6-1410523595ab
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetTextMode
Retrieves the current text mode and undo level of a rich edit control.  
  
## Syntax  
  
```  
  
UINT GetTextMode( ) const;  
  
```  
  
## Return Value  
 A set of bit flags from the [TEXTMODE](http://msdn.microsoft.com/library/windows/desktop/bb774364) enumeration type, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The flags indicate the current text mode and undo level of the control.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::SetTextMode](../vs140/CRichEditCtrl--SetTextMode.md)