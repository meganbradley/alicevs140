---
title: "CAnimateCtrl::Create"
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
ms.assetid: 52cdcfeb-06bf-4b61-ac59-1a44aa55f7d1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimateCtrl::Create
Creates an animation control and attaches it to a `CAnimateCtrl` object.  
  
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
 Specifies the animation control's style. Apply any combination of the windows styles described in the Remarks section below and the animation control styles described in [Animation Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb761886) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `rect`  
 Specifies the animation control's position and size. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](../vs140/RECT-Structure.md) structure.  
  
 `pParentWnd`  
 Specifies the animation control's parent window, usually a `CDialog`. It must not be **NULL.**  
  
 `nID`  
 Specifies the animation control's ID.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 You construct a `CAnimateCtrl` in two steps. First, call the constructor, and then call **Create**, which creates the animation control and attaches it to the `CAnimateCtrl` object.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to an animation control.  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
 If you want to use extended windows styles with your animation control, call [CreateEx](../vs140/CAnimateCtrl--CreateEx.md) instead of **Create**.  
  
 In addition to the window styles listed above, you may want to apply one or more of the animation control styles to an animation control. See the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information on [animation control styles](http://msdn.microsoft.com/library/windows/desktop/bb761886).  
  
## Example  
 See the example for [CAnimateCtrl::CAnimateCtrl](../vs140/CAnimateCtrl--CAnimateCtrl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CAnimateCtrl Class](../vs140/CAnimateCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAnimateCtrl::CAnimateCtrl](../vs140/CAnimateCtrl--CAnimateCtrl.md)   
 [CAnimateCtrl::Open](../vs140/CAnimateCtrl--Open.md)   
 [CAnimateCtrl::Play](../vs140/CAnimateCtrl--Play.md)   
 [CAnimateCtrl::Seek](../vs140/CAnimateCtrl--Seek.md)