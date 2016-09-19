---
title: "CLinkCtrl::CreateEx"
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
ms.assetid: 22b553e3-342a-4c6d-9043-c6e67bb57277
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::CreateEx
Creates a link control with extended styles and attaches it to a `CLinkCtrl` object.  
  
## Syntax  
  
```  
virtual BOOL CreateEx(  
   LPCTSTR lpszLinkMarkup,   
   DWORD dwExStyle,  
   DWORD dwStyle,   
   const RECT& rect,   
   CWnd* pParentWnd,   
   UINT nID  
);  
virtual BOOL CreateEx(  
DWORDdwExStyle,  
DWORDdwStyle,  
const RECT&rect,  
CWnd*pParentWnd,  
UINTnID  
);  
```  
  
#### Parameters  
 `lpszLinkMarkup`  
 Pointer to a zero-terminated string that contains the marked up text to display. For more information, see the section "Markup and Link Access" in the topic [Overview of SysLink Controls](http://msdn.microsoft.com/library/windows/desktop/bb760706) in the [MSDN Library](http://go.microsoft.com/fwlink/?linkid=556).  
  
 `dwExStyle`  
 Specifies the extended style of the link control. For a list of extended Windows styles, see the `dwExStyle` parameter for [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `dwStyle`  
 Specifies the link control's style. Apply any combination of control styles. For more information, see [Common Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb775498) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `rect`  
 Specifies the link control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](../vs140/RECT-Structure.md) structure.  
  
 `pParentWnd`  
 Specifies the link control's parent window. It must not be `NULL`.  
  
 `nID`  
 Specifies the link control's ID.  
  
## Return Value  
 `true` if initialization was successful; otherwise `false`.  
  
## Remarks  
 Use `CreateEx` instead of [Create](../vs140/CLinkCtrl--Create.md) to apply extended Windows style constants.  
  
 The second form of the `CreateEx` method is deprecated. Use the first form that specifies the `lpszLinkMarkup` parameter.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CLinkCtrl::Create](../vs140/CLinkCtrl--Create.md)