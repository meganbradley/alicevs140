---
title: "CToolBarCtrl::GetExtendedStyle"
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
ms.assetid: af2f850d-9d3c-4066-8861-9f29551e6bdc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetExtendedStyle
Retrieves the extended styles for a toolbar control.  
  
## Syntax  
  
```  
  
DWORD GetExtendedStyle( ) const;  
  
```  
  
## Return Value  
 A `DWORD` that represents the extended styles currently in use for the toolbar control. For a list of styles, see [Toolbar Extended Styles](http://msdn.microsoft.com/library/windows/desktop/bb760430), in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETEXTENDEDSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb787331), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetExtendedStyle](../vs140/CToolBarCtrl--SetExtendedStyle.md)