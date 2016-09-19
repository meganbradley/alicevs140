---
title: "CReBarCtrl::GetColorScheme"
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
ms.assetid: 7f6b1480-6782-4aee-9119-3b71965fa310
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetColorScheme
Retrieves the [COLORSCHEME](http://msdn.microsoft.com/library/windows/desktop/bb775502) structure for the rebar control.  
  
## Syntax  
  
```  
  
BOOL GetColorScheme( COLORSCHEME*   
lpcs  
 );  
  
```  
  
#### Parameters  
 `lpcs`  
 A pointer to a [COLORSCHEME](http://msdn.microsoft.com/library/windows/desktop/bb775502) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The **COLORSCHEME** structure includes the button highlight color and the button shadow color.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::SetColorScheme](../vs140/CReBarCtrl--SetColorScheme.md)