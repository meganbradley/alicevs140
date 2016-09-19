---
title: "CToolTipCtrl::CreateEx"
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
ms.assetid: f971dd00-3e08-4f75-b246-89847f4e81ec
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::CreateEx
Creates a control (a child window) and associate it with the `CToolTipCtrl` object.  
  
## Syntax  
  
```  
  
      virtual BOOL CreateEx(   
   CWnd* pParentWnd,   
   DWORD dwStyle = 0,   
   DWORD dwStyleEx = 0    
);  
```  
  
#### Parameters  
 `pParentWnd`  
 A pointer to the window that is the control's parent.  
  
 `dwStyle`  
 Specifies the tool tip control's style. See the **Remarks** section of [Create](../vs140/CToolTipCtrl--Create.md) for more information.  
  
 *dwStyleEx*  
 Specifies the extended style of the control being created. For a list of extended Windows styles, see the `dwExStyle` parameter for [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if successful otherwise 0.  
  
## Remarks  
 Use `CreateEx` instead of **Create** to apply extended Windows styles, specified by the Windows extended style preface **WS_EX_**.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::CToolTipCtrl](../vs140/CToolTipCtrl--CToolTipCtrl.md)