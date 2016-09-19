---
title: "CIPAddressCtrl::Create"
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
ms.assetid: 8ef6254c-7594-4d0a-8e73-377c0db85e08
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CIPAddressCtrl::Create
Creates an IP Address Control and attaches it to a `CIPAddressCtrl` object.  
  
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
 The IP Address control's style. Apply a combination of window styles. You must include the **WS_CHILD** style because the control must be a child window. See [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) in the[!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a list of windows styles.  
  
 `rect`  
 A reference to the IP Address Control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
 `pParentWnd`  
 A pointer to the IP Address Control's parent window. It must not be **NULL.**  
  
 `nID`  
 The IP Address Control's ID.  
  
## Return Value  
 Nonzero if initialization was successful; otherwise 0.  
  
## Remarks  
 You construct a `CIPAddressCtrl` object in two steps.  
  
1.  Call the constructor, which creates the `CIPAddressCtrl` object.  
  
2.  Call **Create**, which creates the IP Address Control.  
  
 If you want to use extended windows styles with your control, call [CreateEx](../vs140/CIPAddressCtrl--CreateEx.md) instead of **Create**.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CIPAddressCtrl Class](../vs140/CIPAddressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CIPAddressCtrl::CIPAddressCtrl](../vs140/CIPAddressCtrl--CIPAddressCtrl.md)