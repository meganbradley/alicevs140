---
title: "CToolBarCtrl::Create"
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
ms.assetid: 380788be-0f0d-4a81-9cee-52bafe6c8235
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::Create
Creates a toolbar control and attaches it to a `CToolBarCtrl` object.  
  
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
 Specifies the toolbar control's style. Toolbars must always have the **WS_CHILD** style. In addition, you can specify any combination of toolbar styles and window styles as described under **Remarks**.  
  
 `rect`  
 Optionally specifies the toolbar control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
 `pParentWnd`  
 Specifies the toolbar control's parent window. It must not be **NULL**.  
  
 `nID`  
 Specifies the toolbar control's ID.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 You construct a `CToolBarCtrl` in two steps. First, call the constructor, and then call **Create**, which creates the toolbar control and attaches it to the `CToolBarCtrl` object. Apply the following window styles to a toolbar control.  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
 See [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a description of window styles.  
  
 Optionally, apply a combination of [common control styles](http://msdn.microsoft.com/library/windows/desktop/bb775498), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 Apply a combination of toolbar styles to either the control or the buttons themselves. The styles are described in the topic [Toolbar Control and Button Styles](http://msdn.microsoft.com/library/windows/desktop/bb760439) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 To use extended toolbar styles, call [SetExtendedStyle](../vs140/CToolBarCtrl--SetExtendedStyle.md) after you call **Create**. To create a toolbar with extended window styles, call [CToolBarCtrl::CreateEx](../vs140/CToolBarCtrl--CreateEx.md) instead of **Create**.  
  
 The toolbar control automatically sets the size and position of the toolbar window. The height is based on the height of the buttons in the toolbar. The width is the same as the width of the parent window's client area. The `CCS_TOP` and `CCS_BOTTOM` styles determine whether the toolbar is positioned along the top or bottom of the client area. By default, a toolbar has the `CCS_TOP` style.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::CToolBarCtrl](../vs140/CToolBarCtrl--CToolBarCtrl.md)   
 [CToolBarCtrl::SetButtonStructSize](../vs140/CToolBarCtrl--SetButtonStructSize.md)