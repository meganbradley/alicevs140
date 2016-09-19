---
title: "CHotKeyCtrl::Create"
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
ms.assetid: 6e08916c-a0bd-4905-9ddd-9c90d768e30e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHotKeyCtrl::Create
Creates a hot key control and attaches it to a `CHotKeyCtrl` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID   
);  
```  
  
#### Parameters  
 `dwStyle`  
 Specifies the hot key control's style. Apply any combination of control styles. See [Common Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb775498) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
 `rect`  
 Specifies the hot key control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](../vs140/RECT-Structure.md) structure.  
  
 `pParentWnd`  
 Specifies the hot key control's parent window, usually a [CDialog](../vs140/CDialog-Class.md). It must not be **NULL**.  
  
 `nID`  
 Specifies the hot key control's ID.  
  
## Return Value  
 Nonzero, if initialization was successful; otherwise 0.  
  
## Remarks  
 You construct a `CHotKeyCtrl` object in two steps. First, call the constructor and then call **Create**, which creates the hot key control and attaches it to the `CHotKeyCtrl` object.  
  
 If you want to use extended windows styles with your control, call [CreateEx](../vs140/CHotKeyCtrl--CreateEx.md) instead of **Create**.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHotKeyCtrl Class](../vs140/CHotKeyCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHotKeyCtrl::CHotKeyCtrl](../vs140/CHotKeyCtrl--CHotKeyCtrl.md)