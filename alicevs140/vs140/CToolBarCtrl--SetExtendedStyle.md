---
title: "CToolBarCtrl::SetExtendedStyle"
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
ms.assetid: fa0dd69b-b51a-452f-8191-bfcb29047f77
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetExtendedStyle
Sets the extended styles for a toolbar control.  
  
## Syntax  
  
```  
  
      DWORD SetExtendedStyle(  
   DWORD dwExStyle   
);  
```  
  
#### Parameters  
 `dwExStyle`  
 A value specifying the new extended styles. This parameter can be a combination of the toolbar extended styles.  
  
## Return Value  
 A `DWORD` that represents the previous extended styles. For a list of styles, see [Toolbar Extended Styles](http://msdn.microsoft.com/library/windows/desktop/bb760430), in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_SETEXTENDEDSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb787427), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetExtendedStyle](../vs140/CToolBarCtrl--GetExtendedStyle.md)